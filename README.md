# mule4tips
Some tips to help in Mule4

# DataWeave2: get current server time


# DataWeave2: build date time in Json format
%dw 2.0
output application/java
var systemNow = now()
---
{
    "Date Time": (systemNow.year as String) ++ "-" ++ (systemNow.month as String) ++ "-" ++ (systemNow.day as String) ++ "T" ++ (systemNow.hour as String) ++ ":" ++ (systemNow.minutes as String) ++ ":" ++ (systemNow.seconds as String) ++ "." ++ (systemNow.milliseconds as String) ++ "Z"
}
