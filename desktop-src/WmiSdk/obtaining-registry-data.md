---
description: Sie können Registrierungsdaten mithilfe der WMI-Klasse StdRegProv und deren Methoden abrufen oder ändern.
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
ms.openlocfilehash: b904316809a6949c6897e32127f85569e3b2ac13cb769db4739e61c164aa19fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050638"
---
# <a name="obtaining-registry-data"></a>Abrufen von Registrierungsdaten

Sie können Registrierungsdaten mithilfe der [**WMI-Klasse StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) und deren Methoden abrufen oder ändern. Während Sie das Regedit-Hilfsprogramm verwenden, um Registrierungswerte auf dem lokalen Computer anzuzeigen und zu ändern, ermöglicht **Ihnen StdRegProv** die Verwendung eines Skripts oder einer Anwendung, um solche Aktivitäten auf dem lokalen Computer und den Remotecomputern zu automatisieren.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) enthält Methoden für folgende Schritte:

-   Überprüfen der Zugriffsberechtigungen für einen Benutzer
-   Erstellen, Aufzählen und Löschen von Registrierungsschlüsseln
-   Erstellen, Aufzählen und Löschen von Unterschlüsseln oder benannten Werten
-   Lesen, Schreiben und Löschen von Datenwerten

Registrierungsdaten sind nach Unterstrukturen, Schlüsseln und Unterschlüsseln organisiert, die unter einem Schlüssel der obersten Ebene geschachtelt sind. Die tatsächlichen Datenwerte werden als Einträge oder benannte Werte bezeichnet.

Die Unterstrukturen umfassen Folgendes:

-   **HKEY \_ CLASSES \_ ROOT** (abgekürzt als **HKCR**)
-   **HKEY \_ AKTUELLER \_ BENUTZER** (**HKCU**)
-   **HKEY \_ LOKALER \_ COMPUTER** (**HKLM**)
-   **\_HKEY-BENUTZER**
-   **AKTUELLE \_ \_ HKEY-KONFIGURATION**

Im Registrierungseintrag **HKEY** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion** lautet die HKEY-Unterstruktur beispielsweise **SOFTWARE,** die Unterschlüssel **Sind Microsoft** und **DirectX,** und der benannte Werteintrag ist **InstalledVersion**.

Ein [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) tritt auf, wenn eine Änderung an einem bestimmten Schlüssel auftritt. Der Eintrag identifiziert jedoch weder, wie sich die Werte ändern, noch wird dieses Ereignis durch Änderungen unterhalb des angegebenen Schlüssels ausgelöst. Um Änderungen an einer beliebigen Stelle in einer hierarchischen Schlüsselstruktur zu identifizieren, verwenden Sie [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), das keine bestimmten Werte oder Schlüsseländerungen zurückgibt, die auftreten. Um eine bestimmte Änderung des Eintragswerts abzurufen, verwenden Sie [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), und lesen Sie dann den Eintrag, um einen Baselinewert abzurufen.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt nur über Methoden, die von C++ oder Skript aufgerufen werden können, die sich von der Win32-Klassenstruktur unterscheiden.

Das folgende Codebeispiel zeigt, wie Sie die [**StdRegProv.EnumKey-Methode**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) verwenden, um alle Microsoft-Softwareunterschlüssel unter dem Registrierungsschlüssel aufzulisten.

**HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft**


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





[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt über verschiedene Methoden zum Lesen der verschiedenen Datentypen für Registrierungseintragswerte. Wenn der Eintrag unbekannte Werte enthält, können Sie [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) aufrufen, um sie aufzulisten. In der folgenden Tabelle ist die Entsprechung zwischen **den StdRegProv-Methoden** und den Datentypen aufgeführt.



| Methode                                                                                  | Datentyp           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

In der folgenden Tabelle sind die entsprechenden Methoden zum Erstellen neuer Schlüssel oder Werte oder zum Ändern vorhandener Schlüssel oder Werte aufgeführt.



| Methode                                                                                  | Datentyp           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

Das folgende Beispiel zeigt, wie die Liste der Quellen für das Systemereignisprotokoll aus dem Registrierungsschlüssel gelesen wird.

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** Current \\ **Control Set** \\ **Services** \\ **Eventlog** \\ **System**

Beachten Sie, dass die Elemente im Multistringwert als Auflistung oder Array behandelt werden.


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



Der Registrierungsanbieter wird in LocalService gehostet, nicht im LocalSystem. Daher ist es nicht möglich, Informationen remote aus der Teilstruktur **HKEY \_ CURRENT \_ USER** zu erhalten. Skripts, die auf dem lokalen Computer ausgeführt werden, können jedoch weiterhin auf **HKEY \_ CURRENT \_ USER** zugreifen. Sie können das Hostingmodell auf einem Remotecomputer auf LocalSystem festlegen. Dies ist jedoch ein Sicherheitsrisiko, da die Registrierung auf dem Remotecomputer anfällig für schädlichen Zugriff ist. Weitere Informationen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

## <a name="examples"></a>Beispiele

Im [VbScript-Codebeispiel Lesen eines binären Registrierungswerts](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) im TechNet-Katalog wird WMI verwendet, um einen binären Registrierungswert zu lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Aufgaben: Registrierung](wmi-tasks--registry.md)
</dt> </dl>

 

 
