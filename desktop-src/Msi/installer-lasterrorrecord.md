---
description: Die lasterrorrecord-Methode des Installer-Objekts gibt ein Datensatz-Objekt zurück, das Fehler Parameter für den letzten Fehler der Funktion enthält, die den Fehler Daten Satz erzeugt hat.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Installer. lasterrorrecord-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353814"
---
# <a name="installerlasterrorrecord-method"></a>Installer. lasterrorrecord-Methode

Die **lasterrorrecord** -Methode des [**Installer**](installer-object.md) -Objekts gibt ein [**Datensatz**](record-object.md) -Objekt zurück, das Fehler Parameter für den letzten Fehler der Funktion enthält, die den Fehler Daten Satz erzeugt hat.

## <a name="syntax"></a>Syntax


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das [**Datensatz**](record-object.md) -Objekt wird nach der Ausführung dieser Funktion einer Funktion zurückgesetzt, die einen Fehler Daten Satz generiert.

Nur die folgenden vorgesehenen Funktionen generieren einen Fehler Daten Satz:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Einzusetzen**](database-commit.md)
-   [**OpenView –**](database-openview.md)
-   [**Importieren**](database-import.md)
-   [**Exportieren**](database-export.md)
-   [**Merge**](database-merge.md)
-   [**Gene Rate Transform**](database-generatetransform.md)
-   [**Applytransform**](database-applytransform.md)
-   [**Auszuführen**](view-execute.md)
-   [**Ändern**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**Componentcurrentstate**](session-componentcurrentstate.md)
-   [**Componentrequeststate**](session-componentrequeststate.md)
-   [**Featurecurrentstate**](session-featurecurrentstate.md)
-   [**Featurerequeststate**](session-featurerequeststate.md)
-   [**Featurecost**](session-featurecost.md)
-   [**Featurevalidstates**](session-featurevalidstates.md)
-   [**Setinstalllevel**](session-setinstalllevel.md)

Das folgende Beispiel in VBScript verwendet einen [**OpenDatabase**](installer-opendatabase.md) -Befehl, um anzuzeigen, wie erweiterte Fehlerinformationen von einer der Methoden oder Eigenschaften abgerufen werden, die die **lasterrorrecord** -Methode unterstützen. Das Beispiel erstellt eine Fehlermeldung, wenn die **OpenDatabase** -Methode fehlschlägt. Das **Err** -Objekt wird verwendet, um zu bestimmen, ob ein Fehler aufgetreten ist.


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




