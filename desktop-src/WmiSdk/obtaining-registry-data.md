---
description: Sie können Registrierungsdaten abrufen oder ändern, indem Sie die WMI-Klasse "StdRegProv" und deren Methoden verwenden.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Abrufen von Registrierungsdaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346673"
---
# <a name="obtaining-registry-data"></a>Abrufen von Registrierungsdaten

Sie können Registrierungsdaten abrufen oder ändern, indem Sie die WMI-Klasse " [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) " und deren Methoden verwenden. Wenn Sie das Hilfsprogramm regedit verwenden, um Registrierungs Werte auf dem lokalen Computer anzuzeigen und zu ändern, können Sie mit **StdRegProv** ein Skript oder eine Anwendung verwenden, um solche Aktivitäten auf dem lokalen Computer und auf Remote Computern zu automatisieren.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) enthält Methoden für folgende Aufgaben:

-   Überprüfen der Zugriffsberechtigungen für einen Benutzer
-   Erstellen, auflisten und Löschen von Registrierungs Schlüsseln
-   Erstellen, aufzählen und Löschen von unter Schlüsseln oder benannten Werten
-   Lesen, schreiben und Löschen von Datenwerten

Registrierungsdaten werden nach Teil Strukturen, Schlüsseln und unter Schlüsseln organisiert, die unter einem Schlüssel der obersten Ebene gruppiert sind. Die tatsächlichen Datenwerte werden als Einträge oder benannte Werte bezeichnet.

Die Unterstrukturen umfassen Folgendes:

-   **HKEY \_ Klassen \_** Stamm (abgekürzt als **HKCR**)
-   **HKEY \_ aktueller \_ Benutzer** (**HKCU**)
-   **HKEY \_ lokaler \_ Computer** (**HKLM**)
-   **HKEY- \_ Benutzer**
-   **aktuelle HKEY- \_ \_ Konfiguration**

Im Registrierungs Eintrag **HKEY** \\ **Software** \\ **Microsoft** \\ **DirectX** \\ **installedversion** lautet die HKEY-Unterstruktur beispielsweise **Software**. die Unterschlüssel sind **Microsoft** und **DirectX**, und der benannte Wert Eintrag ist **installedversion**.

Ein [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) tritt auf, wenn eine Änderung an einem bestimmten Schlüssel auftritt, aber der Eintrag nicht identifiziert, wie sich die Werte ändern, und dass dieses Ereignis nicht durch Änderungen unter dem angegebenen Schlüssel ausgelöst wird. Um Änderungen an beliebiger Stelle in einer hierarchischen Schlüsselstruktur zu identifizieren, verwenden Sie das [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), das keine bestimmten Werte oder Schlüssel Änderungen zurückgibt, die auftreten. Um einen bestimmten Wert für den Einstiegs Wert zu erhalten, verwenden Sie das [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), und lesen Sie dann den Eintrag, um einen Baselinewert zu erhalten.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt nur über Methoden, die von C++ oder Skript aufgerufen werden können. Dies unterscheidet sich von der Win32-Klassenstruktur.

Im folgenden Codebeispiel wird gezeigt, wie die [**StdRegProv. EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) -Methode verwendet wird, um alle Microsoft-Software Unterschlüssel unter dem Registrierungsschlüssel aufzulisten.

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft**


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt über verschiedene Methoden zum Lesen der verschiedenen Datentypen von Registrierungs Eintrags Werten. Wenn der Eintrag unbekannte Werte enthält, können Sie [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) zum Auflisten der Werte abrufen. In der folgenden Tabelle werden die Entsprechungen zwischen **StdRegProv** -Methoden und den-Datentypen aufgelistet.



| Methode                                                                                  | Datentyp           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG- \_ Binärdatei**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ Expand \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ \_ MultiSZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG- \_ SZ**         |



 

In der folgenden Tabelle werden die entsprechenden Methoden zum Erstellen neuer Schlüssel oder Werte oder zum Ändern vorhandener-Werte aufgelistet.



| Methode                                                                                  | Datentyp           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG- \_ Binärdatei**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**"Abtexpandedstringvalue"**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ Expand \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ \_ MultiSZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG- \_ SZ**         |



 

Im folgenden Beispiel wird gezeigt, wie die Liste der Quellen für das System Ereignisprotokoll aus dem Registrierungsschlüssel gelesen wird.

**HKEY \_ \_** \\ **System** \\ **Aktuelles System Steuerungs Satz** \\ **Dienste**- \\ **Ereignisprotokoll** \\ **System** des lokalen Computers

Beachten Sie, dass die Elemente im mehrteiligen Zeichen folgen Wert als Sammlung oder Array behandelt werden.


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



Der Registrierungs Anbieter wird in LocalService gehostet – nicht in LocalSystem. Aus diesem Grund ist das Abrufen von Informationen aus der Unterstruktur **HKEY \_ aktueller \_ Benutzer** nicht möglich. Skripts, die auf dem lokalen Computer ausgeführt werden, können jedoch weiterhin auf den **aktuellen HKEY- \_ \_ Benutzer** zugreifen. Sie können das Hostingmodell auf einem Remote Computer auf "LocalSystem" festlegen, dies ist jedoch ein Sicherheitsrisiko, da die Registrierung auf dem Remote Computer anfällig für feindlichen Zugriff ist. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

## <a name="examples"></a>Beispiele

Der Code zum [Lesen eines binären Registrierungs Werts](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript in der TechNet Gallery verwendet WMI, um einen binären Registrierungs Wert zu lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Tasks: Registrierung](wmi-tasks--registry.md)
</dt> </dl>

 

 
