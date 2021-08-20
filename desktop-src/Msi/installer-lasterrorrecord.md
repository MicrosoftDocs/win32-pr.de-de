---
description: Die LastErrorRecord-Methode des Installer-Objekts gibt ein Record-Objekt zurück, das Fehlerparameter für den letzten Fehler der Funktion enthält, die den Fehlerdatensatz erzeugt hat.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Installer.LastErrorRecord-Methode
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
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142109"
---
# <a name="installerlasterrorrecord-method"></a>Installer.LastErrorRecord-Methode

Die **LastErrorRecord-Methode** des [**Installer-Objekts**](installer-object.md) gibt ein [**Record-Objekt**](record-object.md) zurück, das Fehlerparameter für den letzten Fehler der Funktion enthält, die den Fehlerdatensatz erzeugt hat.

## <a name="syntax"></a>Syntax


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das [**Record-Objekt**](record-object.md) wird nach der Ausführung dieser Funktion einer Funktion zurückgesetzt, die einen Fehlerdatensatz generiert.

Nur die folgenden festgelegten Funktionen generieren einen Fehlerdatensatz:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Commit**](database-commit.md)
-   [**Openview**](database-openview.md)
-   [**Importieren**](database-import.md)
-   [**Exportieren**](database-export.md)
-   [**Zusammenführen**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Ausführen**](view-execute.md)
-   [**Ändern**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**Sourcepath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

Im folgenden Beispiel in VBScript wird ein Aufruf von [**OpenDatabase**](installer-opendatabase.md) verwendet, um zu zeigen, wie erweiterte Fehlerinformationen von einer der Methoden oder Eigenschaften, die die **LastErrorRecord-Methode** unterstützen, erhalten werden. Im Beispiel wird eine Fehlermeldung erstellt, wenn bei der **OpenDatabase-Methode** ein Fehler auftritt. Das **Err-Objekt** wird verwendet, um zu bestimmen, ob ein Fehler aufgetreten ist.


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
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




