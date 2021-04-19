---
description: Das-Objekt von "Swap DateTime" ist ein Hilfsobjekt zum Analysieren und Festlegen von Common Information Model (CIM)-DateTime-Werten.
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Taubemdatetime-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348061"
---
# <a name="swbemdatetime-object"></a>Taubemdatetime-Objekt

Das-Objekt von " **Swap DateTime** " ist ein Hilfsobjekt zum Analysieren und Festlegen von Common Information Model (CIM)- [DateTime](datetime.md) -Werten. Sie spielt eine Rolle ähnlich der von " [**errbemubjectpath**](swbemobjectpath.md)", die Unterstützung für das Formatieren und Interpretieren von Objekt Pfaden bietet. Sie können den VBScript-Aufruf von " [comateobject](/previous-versions//xzysf6hc(v=vs.85)) " verwenden, um das Objekt " **Swap DateTime** " zu erstellen.

Ein " **slibemdatetime** "-Objekt kann mithilfe von Methoden für das-Objekt aus den Werten " **VT \_ Date** " oder " **FILETIME** " initialisiert und formatiert werden. Mithilfe der Eigenschaften des-Objekts kann der Wert in die Komponenten Jahr, Monat, Tag, Stunde, Minuten, Sekunden oder Mikrosekunden analysiert werden. Das Objekt " **taubemdatetime** " kann entweder in lokale oder koordinierte Weltzeit (UTC)-Werte formatiert werden. Weitere Informationen finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).

' **Swap DateTime** ' ist das einzige Windows-Verwaltungsinstrumentation (WMI)-Skript Objekt, das für die Initialisierung und Skripts, die auf HTML-Seiten in Internet Explorer ausgeführt werden, als sicher gekennzeichnet ist.

## <a name="members"></a>Member

Das Objekt " **waybemdatetime** " enthält diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **Swap DateTime** " verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**' GetFileTime '**](swbemdatetime-getfiletime.md) | Konvertiert ein Datum und eine Uhrzeit der **FILETIME** , ausgedrückt als **BSTR**, in ein WMI- [DateTime](datetime.md) -Format.<br/> |
| [**GetVarDate**](swbemdatetime-getvardate.md)   | Konvertiert einen Datums-und Uhrzeitwert für ein WMI- [DateTime-Format](datetime.md) in ein **VT- \_ Datum**.<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | Konvertiert ein WMI- [DateTime](datetime.md) -Format in ein Datum und eine Uhrzeit der **FILETIME** , ausgedrückt als **BSTR**.<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | Konvertiert ein Datum und eine Uhrzeit im Format " **VT \_ Date** " in einen WMI- [DateTime](datetime.md)-Wert.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Swap DateTime** " verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Tag**](swbemdatetime-day.md)<br/>                                     | Lesen/Schreiben<br/> | Die Tages Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                           |
| [**Dayangegeben**](swbemdatetime-dayspecified.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob der Tag angegeben oder als Platzhalter belassen wird.<br/>                                                        |
| [**Stunden**](swbemdatetime-hours.md)<br/>                                 | Lesen/Schreiben<br/> | Die Stunden der Tages Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                              |
| [**Sansangegeben**](swbemdatetime-hoursspecified.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob die Stunde angegeben oder als Platzhalter belassen wird.<br/>                                                       |
| [**Isinterval**](swbemdatetime-isinterval.md)<br/>                       | Lesen/Schreiben<br/> | Gibt an, dass mindestens eine Komponente von CIM [DateTime](datetime.md) ein Intervall und kein Datum darstellt.<br/> |
| [**Mikrosekunden**](swbemdatetime-microseconds.md)<br/>                   | Lesen/Schreiben<br/> | Die Mikrosekunden Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                  |
| [**' Mikroseconds' angegeben**](swbemdatetime-microsecondsspecified.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob die Mikrosekunden Komponente angegeben oder als Platzhalter belassen wird.<br/>                                     |
| [**Minuten**](swbemdatetime-minutes.md)<br/>                             | Lesen/Schreiben<br/> | Die Minuten Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                       |
| [**Minutesangegeben**](swbemdatetime-minutesspecified.md)<br/>           | Lesen/Schreiben<br/> | Gibt an, ob die Minuten Komponente angegeben oder als Platzhalter belassen wird.<br/>                                          |
| [**Ges**](swbemdatetime-month.md)<br/>                                 | Lesen/Schreiben<br/> | Die Monats Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                         |
| [**Monthspezifiziert**](swbemdatetime-monthspecified.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob der Monat angegeben oder als Platzhalter belassen wird.<br/>                                                      |
| [**Sekunden**](swbemdatetime-seconds.md)<br/>                             | Lesen/Schreiben<br/> | Die Sekunden Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                       |
| [**Secondsspezifiziert**](swbemdatetime-secondsspecified.md)<br/>           | Lesen/Schreiben<br/> | Gibt an, ob die Sekunden Komponente angegeben oder als Platzhalter belassen wird.<br/>                                          |
| [**UTC**](swbemdatetime-utc.md)<br/>                                     | Lesen/Schreiben<br/> | Die UTC-Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                           |
| [**Utcangegeben**](swbemdatetime-utcspecified.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob die UTC-Komponente angegeben oder als Platzhalter belassen wird.<br/>                                              |
| [**Wert**](swbemdatetime-value.md)<br/>                                 | Lesen/Schreiben<br/> | Der vollständige CIM- [DateTime](datetime.md) -Wert.<br/>                                                                         |
| [**Jährigen**](swbemdatetime-year.md)<br/>                                   | Lesen/Schreiben<br/> | Die Jahres Komponente eines CIM- [DateTime](datetime.md) -Werts.<br/>                                                          |
| [**Yearfest gelegt**](swbemdatetime-yearspecified.md)<br/>                 | Lesen/Schreiben<br/> | Gibt an, ob das Jahr angegeben oder als Platzhalter belassen wird.<br/>                                                |



 

## <a name="remarks"></a>Bemerkungen

WMI zeichnet Zeitstempel im UTC-Format (Universal Time Koordinate) auf. UTC ist nicht das Format, das von den meisten Entwicklern und IT-Administratoren verwendet wird. Daher besteht ein häufiges Problem darin, zu bestimmen, wie UTC in etwas lesbares übersetzt werden soll. Weitere Informationen zum Arbeiten mit UTC finden Sie unter [WMI-Tasks: Datums-und Uhrzeitwerte](wmi-tasks--dates-and-times.md) und [Arbeiten mit Datums-und Uhrzeitwerten mithilfe von WMI](/previous-versions/tn-archive/ee198928(v=technet.10)). Sie können auch die Informationen zu [Zeit (Oh und zu Datumsangaben)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) lesen und [wie kann ich eine angegebene Anzahl von Tagen von einem UTC-Wert subtrahieren?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) in Blogbeiträgen finden Sie weitere Informationen.

Alle numerischen Felder können einen Platzhalter Wert aufweisen, wenn die [**isinterval**](swbemdatetime-isinterval.md) -Eigenschaft auf **false** festgelegt ist. Felder mit Platzhalterwerten enthalten Sternchen im gesamten Feld.

Jede Eigenschaft, z. b. [**Day**](swbemdatetime-day.md), verfügt über einen entsprechenden festgelegten booleschen Wert, z. b. [**dayangegeben**](swbemdatetime-dayspecified.md). Wenn **dayangegebene** den Wert **false** hat, wird der Wert als Intervall und nicht als Zahl zwischen 01 und 31 interpretiert. Wenn ein Intervall an einer beliebigen Stelle im CIM- [DateTime](datetime.md) -Wert verwendet wird, wird [**isinterval**](swbemdatetime-isinterval.md) ebenfalls auf " **true**" festgelegt. Der Standardwert ist, dass ein CIM-DateTime-Wert ein Datum anstelle eines oder mehrerer Intervalle enthält.

Wenn z. b. " [**skibemdatetime. dayangegebene**](swbemdatetime-dayspecified.md) " den Wert " **true**" hat, enthält " [**taubemdatetime. Value**](swbemdatetime-value.md) " den aktuellen Wert von " [**taubemdatetime. Day**](swbemdatetime-day.md)"; Andernfalls ist es ein Platzhalter Wert. Die [**isinterval**](swbemdatetime-isinterval.md) -Eigenschaft ist in beiden Fällen **false** .

## <a name="examples"></a>Beispiele

Im folgenden Skriptcode Beispiel wird gezeigt, wie ein " **slibemdatetime** "-Objekt verwendet wird, um einen DateTime-Eigenschafts Wert zu analysieren, der aus dem WMI-Repository gelesen wird, die **InstallDate** -Eigenschaft im [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)


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



Im folgenden Beispiel wird gezeigt, wie Sie ein " **slibemdatetime** "-Objekt erstellen, einen Datumswert im Objekt speichern, das Datum als lokale und koordinierte Weltzeit (UTC) anzeigen und den Wert in einer neu erstellten Klasse und Eigenschaft speichern. Weitere Informationen zur Konstanten **wbemcimtypedatetime** finden Sie unter [wbemcimtypeenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


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



Im folgenden Skriptcode Beispiel wird veranschaulicht, wie Sie ein-Objekt mit einem " **Swap DateTime** "-Objekt für eine Eigenschaft ändern, die aus dem WMI-Repository gelesen wird.


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



Im folgenden Skriptcode Beispiel wird gezeigt, wie ein " **slibemdate** "-Objekt verwendet wird, um einen **FILETIME** -Wert zu lesen.


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



Mit dem folgenden PowerShell-Code wird eine Instanz eines SWbemDateTime-Objekts erstellt, das Installationsdatum des Betriebssystems abgerufen und das Datum in ein anderes Format konvertiert.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-DateTime<br/>                                                         |
| IID<br/>                      | IID \_ iswbemdatetime<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wbemcimtypeerum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[DateTime](datetime.md)
</dt> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

