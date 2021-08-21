---
description: Das SWbemDateTime-Objekt ist ein Hilfsobjekt zum Analysieren und Festlegen Common Information Model (CIM) datetime-Werte.
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: SWbemDateTime-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 25f8b04aa8c581d8d7e40ab1d52162d305c97d0d8ce3f7d626cb3d29e7262666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050088"
---
# <a name="swbemdatetime-object"></a>SWbemDateTime-Objekt

Das **SWbemDateTime-Objekt** ist ein Hilfsobjekt zum Analysieren und Festlegen Common Information Model (CIM) [datetime-Werte.](datetime.md) Sie spielt eine ähnliche Rolle wie [**SWbemObjectPath,**](swbemobjectpath.md)die Unterstützung beim Formatieren und Interpretieren von Objektpfaden bietet. Sie können den VBScript [CreateObject-Aufruf](/previous-versions//xzysf6hc(v=vs.85)) verwenden, um das **SWbemDateTime-Objekt zu** erstellen.

Ein **SWbemDateTime-Objekt** kann mithilfe von Methoden für das Objekt initialisiert und in **VT \_ DATE-** oder **FILETIME-Werten** formatiert werden. Mithilfe der Eigenschaften des -Objekts kann der Wert in Komponentenjahr, Monat, Tag, Stunde, Minuten, Sekunden oder Mikrosekunden analysiert werden. Das **SWbemDateTime-Objekt** kann entweder in lokale oder koordinierte Weltzeit (UTC) formatiert werden. Weitere Informationen finden Sie unter [Datums- und Uhrzeitformat.](date-and-time-format.md)

**SWbemDateTime** ist das einzige WMI-Skriptobjekt (Windows Management Instrumentation), das als sicher für die Initialisierung und Skripts markiert ist, die auf HTML-Seiten in Internet Explorer.

## <a name="members"></a>Member

Das **SWbemDateTime-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemDateTime-Objekt** verfügt über diese Methoden.



| Methode                                           | Beschreibung                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetFileTime**](swbemdatetime-getfiletime.md) | Konvertiert ein **FILETIME-Datum** und eine FILETIME-Uhrzeit, ausgedrückt als **BSTR,** in ein WMI-DATETIME-Format. [](datetime.md)<br/> |
| [**GetVarDate**](swbemdatetime-getvardate.md)   | Konvertiert einen datums- und [uhrzeitformatierten](datetime.md) WMI DATETIME-Wert in einen **VT \_ DATE-Wert.**<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | Konvertiert ein [WMI-DATETIME-Format](datetime.md) in ein **FILETIME-Datum** und eine FILETIME-Uhrzeit, ausgedrückt als **BSTR.**<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | Konvertiert ein Datum und eine **Uhrzeit im VT \_ DATE-Format** in einen WMI-DATETIME-. [](datetime.md)<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemDateTime-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | Beschreibung                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Tag**](swbemdatetime-day.md)<br/>                                     | Lesen/Schreiben<br/> | Die Tageskomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                           |
| [**DaySpecified**](swbemdatetime-dayspecified.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob der Tag als Platzhalter angegeben oder verlassen wird.<br/>                                                        |
| [**Stunden**](swbemdatetime-hours.md)<br/>                                 | Lesen/Schreiben<br/> | Die Stunden der Tageskomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                              |
| [**HoursSpecified**](swbemdatetime-hoursspecified.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob die Stunde als Platzhalter angegeben oder übrig gelassen wird.<br/>                                                       |
| [**IsInterval**](swbemdatetime-isinterval.md)<br/>                       | Lesen/Schreiben<br/> | Gibt an, dass mindestens eine Komponente von CIM [datetime](datetime.md) ein Intervall und kein Datum darstellt.<br/> |
| [**Mikrosekunden**](swbemdatetime-microseconds.md)<br/>                   | Lesen/Schreiben<br/> | Die Mikrosekundenkomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                  |
| [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob die Mikrosekundenkomponente als Platzhalter angegeben oder übrig gelassen wird.<br/>                                     |
| [**Minuten**](swbemdatetime-minutes.md)<br/>                             | Lesen/Schreiben<br/> | Die Minutenkomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                       |
| [**MinutesSpecified**](swbemdatetime-minutesspecified.md)<br/>           | Lesen/Schreiben<br/> | Gibt an, ob die Minutenkomponente als Platzhalter angegeben oder übrig gelassen wird.<br/>                                          |
| [**Monat**](swbemdatetime-month.md)<br/>                                 | Lesen/Schreiben<br/> | Die Monatskomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                         |
| [**MonthSpecified**](swbemdatetime-monthspecified.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob der Monat als Platzhalter angegeben oder übrig gelassen wird.<br/>                                                      |
| [**Sekunden**](swbemdatetime-seconds.md)<br/>                             | Lesen/Schreiben<br/> | Die Sekundenkomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                       |
| [**SecondsSpecified**](swbemdatetime-secondsspecified.md)<br/>           | Lesen/Schreiben<br/> | Gibt an, ob die Sekundenkomponente als Platzhalter angegeben oder übrig gelassen wird.<br/>                                          |
| [**Utc**](swbemdatetime-utc.md)<br/>                                     | Lesen/Schreiben<br/> | Die UTC-Komponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                           |
| [**UTCSpecified**](swbemdatetime-utcspecified.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob die UTC-Komponente als Platzhalter angegeben oder verlassen wird.<br/>                                              |
| [**Wert**](swbemdatetime-value.md)<br/>                                 | Lesen/Schreiben<br/> | Der vollständige [DATETIME-Wert.](datetime.md)<br/>                                                                         |
| [**Jahr**](swbemdatetime-year.md)<br/>                                   | Lesen/Schreiben<br/> | Die Jahreskomponente eines [CIM-datetime-Werts.](datetime.md)<br/>                                                          |
| [**YearSpecified**](swbemdatetime-yearspecified.md)<br/>                 | Lesen/Schreiben<br/> | Gibt an, ob das Jahr als Platzhalter angegeben oder übrig gelassen wird.<br/>                                                |



 

## <a name="remarks"></a>Hinweise

WMI zeichnet Zeitstempel im UTC-Format (Universal Time Coordinate) auf. UTC ist nicht das Format, das die meisten Entwickler und IT-Administratoren verwenden. Daher besteht ein häufiges Problem in der Bestimmung, wie UTC in etwas besser lesbares übersetzt wird. Weitere Informationen zum Arbeiten mit UTC finden Sie unter [WMI Tasks: Dates and Times (WMI-Aufgaben:](wmi-tasks--dates-and-times.md) Datums- und Zeitangaben) und Working with Dates and Times using WMI (Arbeiten mit [Datums- und Zeitangaben mit WMI).](/previous-versions/tn-archive/ee198928(v=technet.10)) Weitere Informationen finden Sie auch in den Blogbeiträgen It [es About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) und How Can I Subtract a Specified Number of Days from a UTC Value? (Wie kann ich eine angegebene Anzahl von Tagen von einem UTC-Wert subtrahieren?). [](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx)

Jedes numerische Feld kann einen Platzhalterwert haben, wenn die [**IsInterval-Eigenschaft**](swbemdatetime-isinterval.md) auf **FALSE festgelegt ist.** Felder mit Platzhalterwerten enthalten Sternchen im gesamten Feld.

Jede Eigenschaft, z. [**B. Day,**](swbemdatetime-day.md)verfügt über einen entsprechenden angegebenen booleschen Wert, z. B. [**DaySpecified.**](swbemdatetime-dayspecified.md) Wenn **DaySpecified** **auf FALSE festgelegt** ist, wird der Wert als Intervall und nicht als Zahl zwischen 01 und 31 interpretiert. Wenn ein Intervall an einer beliebigen Stelle im [DATETIME-Wert](datetime.md) von CIM verwendet wird, wird [**IsInterval**](swbemdatetime-isinterval.md) ebenfalls auf **TRUE festgelegt.** Der Standardwert ist, dass ein CIM-datetime-Wert ein Datum statt eines oder mehrere Intervalle enthält.

Wenn [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) beispielsweise **TRUE** ist, enthält [**SWbemDateTime.Value**](swbemdatetime-value.md) den aktuellen Wert [**von SWbemDateTime.Day,**](swbemdatetime-day.md)andernfalls handelt es sich um einen Platzhalterwert. Die [**IsInterval-Eigenschaft**](swbemdatetime-isinterval.md) ist in **beiden** Fällen FALSE.

## <a name="examples"></a>Beispiele

Das folgende Skriptcodebeispiel zeigt, wie Sie ein **SWbemDateTime-Objekt** verwenden, um einen datetime-Eigenschaftswert zu analysieren, der aus dem WMI-Repository gelesen wird, der **InstallDate-Eigenschaft** in [**Win32 \_ OperatingSystem.**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



Das folgende Beispiel zeigt, wie Sie ein **SWbemDateTime-Objekt** erstellen, einen Datumswert im -Objekt speichern, das Datum als lokal und koordinierte Weltzeit (UTC) anzeigen und den Wert in einer neu erstellten Klasse und Eigenschaft speichern. Weitere Informationen zur Konstante **wbemCimtypeDatetime** finden Sie unter [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



Das folgende Skriptcodebeispiel zeigt, wie Sie ein **SWbemDateTime-Objekt** verwenden, um einen Intervallwert für eine Eigenschaft zu ändern, die aus dem WMI-Repository gelesen wird.


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



Das folgende Skriptcodebeispiel zeigt, wie ein **SWbemDate-Objekt** zum Lesen eines **FILETIME-Werts** verwendet wird.


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



Der folgende PowerShell-Code erstellt eine Instanz eines SWbemDateTime-Objekts, ruft das Installationsdatum des Betriebssystems ab und konvertiert das Datum in ein anderes Format.


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



Der folgende PowerShell-Code übersetzt den Code in ein Format, das von einem CIM-Anbieter verwendet werden kann.


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[Datetime](datetime.md)
</dt> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

