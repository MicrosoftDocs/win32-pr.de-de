---
description: 'Die System Registrierungs Anbieter-Klasse StdRegProv für WMI verfügt über Methoden, die Folgendes ausführen:'
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
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373413"
---
# <a name="changing-registry-data"></a>Ändern von Registrierungsdaten

Die [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) -Klasse [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) für WMI verfügt über Methoden, die Folgendes ausführen:

-   Erstellen oder Löschen von Registrierungs Schlüsseln.

    Verwenden Sie " [**kreatekey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) " oder " [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)".

-   Erstellen oder löschen Sie benannte Werte, die als Einträge bezeichnet werden, wenn Sie sich Unterschlüssel befinden.

    Verwenden Sie den Namen eines neuen Werts und [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)oder [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) , um einen benannten Wert zu erstellen. Verwenden Sie [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) , um einen benannten Wert zu löschen.

-   Ändern benannter Werte.

    Verwenden Sie den Namen eines Werts und die Set-Methoden (im vorherigen aufzurufenen Element identifiziert), um vorhandene benannte Werte unter einem Schlüssel zu ändern. Sie müssen den Namen eines Werts kennen, um ihn zu ändern. Wenn Sie die Wertnamen unter einem Schlüssel nicht kennen, verwenden Sie die [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) -Methode, um die Namen abzurufen.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Erstellen eines Registrierungsschlüssels mit VBScript](#creating-a-registry-key-using-vbscript)
-   [Erstellen eines benannten Registrierungs Werts mithilfe von PowerShell und VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Erstellen eines Registrierungsschlüssels mit VBScript

Da es sich bei der Registrierung um die zentrale Konfigurations Datenbank für das Betriebssystem, Anwendungen und Dienste handelt, sollten Sie Vorsicht walten lassen, wenn Sie Änderungen an Registrierungs Werten schreiben oder Schlüssel löschen.

> [!Note]  
> Der Stamm Unterschlüssel **HKEY \_ - \_ Klassen** des HKEY **\_ Current \_ User (HKCU)** kann nicht überwacht werden. Das Überwachen von **HKEY- \_ Benutzern** wird nicht empfohlen, da die untergeordneten Schlüssel beim Laden von Strukturen angezeigt und ausgeblendet werden.

 

In den folgenden Codebeispielen wird gezeigt, wie ein neuer Registrierungsschlüssel und ein Unterschlüssel erstellt werden.


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Erstellen eines benannten Registrierungs Werts mithilfe von PowerShell und VBScript

Im folgenden Codebeispiel wird gezeigt, wie ein benannter Wert mit dem Namen " **multistringvalue** " unter der **HKEY \_ local \_ Machine** \\ **Software** \\ **myKey** \\ **MySubKey** -Schlüssel erstellt wird, den das vorherige Skript erstellt hat. Das Skript ruft [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) auf, um Zeichen folgen Werte in einen neuen benannten Wert zu schreiben.


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

Mit WMI können Sie die Zugriffssicherheit für einen Registrierungsschlüssel nicht festlegen. Allerdings vergleicht die [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) -Methode die Sicherheitseinstellungen des aktuellen Benutzers mit der Sicherheits Beschreibung eines Registrierungsschlüssels, um zu bestimmen, ob der Benutzer über eine bestimmte Berechtigung verfügt, z. b. einen **Schlüssel \_ Satz \_ Wert**.
