---
description: 'Die System Registry Provider-Klasse StdRegProv für WMI verfügt über Methoden, die folgende Schritte ausführen:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Ändern von Registrierungsdaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32258fb64e075889a6e423e2b6a3fa2e7b0fdeb0ee5a80e2f45436674ba79c4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556945"
---
# <a name="changing-registry-data"></a>Ändern von Registrierungsdaten

Die [System Registry Provider-Klasse](/previous-versions/windows/desktop/regprov/system-registry-provider) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) für WMI verfügt über Methoden, die folgende Schritte ausführen:

-   Erstellen oder Löschen von Registrierungsschlüsseln.

    Verwenden Sie [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) oder [**DeleteKey.**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)

-   Erstellen oder löschen Sie benannte Werte, die als Einträge bezeichnet werden, wenn sie sich unter Schlüsseln befinden.

    Verwenden Sie den Namen eines neuen Werts und [**SetBinaryValue,**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) [**SetDWORDValue,**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) [**SetExpandedStringValue,**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)oder [**SetStringValue,**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) um einen benannten Wert zu erstellen. Verwenden Sie [**DeleteValue,**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) um einen benannten Wert zu löschen.

-   Ändern sie benannte Werte.

    Verwenden Sie den Namen eines Werts und die Set-Methoden (im vorherigen Aufzählungselement identifiziert), um vorhandene benannte Werte unter einem Schlüssel zu ändern. Sie müssen den Namen eines Werts kennen, um ihn zu ändern. Wenn Sie die Wertnamen unter einem Schlüssel nicht kennen, verwenden Sie die [**EnumValues-Methode,**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) um die Namen abzurufen.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Erstellen eines Registrierungsschlüssels mit VBScript](#creating-a-registry-key-using-vbscript)
-   [Erstellen eines benannten Registrierungswerts mit powerShell und VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Erstellen eines Registrierungsschlüssels mit VBScript

Da es sich bei der Registrierung um die zentrale Konfigurationsdatenbank für das Betriebssystem, die Anwendungen und die Dienste handelt, sollten Sie beim Schreiben von Änderungen an Registrierungswerten oder Löschen von Schlüsseln vorsichtshalber vorgehen.

> [!Note]  
> Sie können den **HKEY \_ CLASSES \_ ROOT-Unterschlüssel** von **HKEY \_ CURRENT \_ USER(HKCU)** nicht überwachen. Die Überwachung von **\_ HKEY-BENUTZERN** wird nicht empfohlen, da die Unterschlüssel angezeigt werden und ausgeblendet werden, wenn Hives geladen werden.

 

Die folgenden Codebeispiele zeigen, wie Sie einen neuen Registrierungsschlüssel und einen Unterschlüssel erstellen.


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Erstellen eines benannten Registrierungswerts mit powerShell und VBScript

Das folgende Codebeispiel zeigt, wie Sie einen benannten Wert namens **MultiStringValue** unter dem **Schlüssel HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **MyKey** \\ **MySubKey** erstellen, den das vorherige Skript erstellt. Das Skript ruft [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) auf, um Zeichenfolgenwerte in einen neuen benannten Wert zu schreiben.


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

Mithilfe von WMI können Sie die Zugriffssicherheit für einen Registrierungsschlüssel nicht festlegen. Die [**StdRegProv.CheckAccess-Methode**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) vergleicht jedoch die Sicherheitseinstellungen des aktuellen Benutzers mit der Sicherheitsbeschreibung für einen Registrierungsschlüssel, um festzustellen, ob der Benutzer über eine bestimmte Berechtigung verfügt, z. B. **KEY SET \_ \_ VALUE**.
