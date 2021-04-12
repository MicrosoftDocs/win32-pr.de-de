---
description: Verwendet einen vorinstallierten Schlüssel für die Netzwerk Authentifizierung.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Beispiel für WPA2-Personal Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0054bc28962113a85bb909d4e8cd173b3bc16974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348119"
---
# <a name="wpa2-personal-profile-sample"></a>Beispiel für WPA2-Personal Profil

In diesem Beispiel Profil wird ein vorinstaltzter Schlüssel für die Netzwerk Authentifizierung verwendet. Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben. Dieses Beispiel Profil ist für die Verwendung Wi-Fi geschützten Zugriffs 2-Sicherheit konfiguriert, die im persönlichen Modus (WPA2-Personal) ausgeführt wird. Der Advanced Encryption Standard (AES)-Chiffre Typ wird für die Verschlüsselung verwendet.

**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren. Die Standardeinstellung für [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert. Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist. Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt. Weitere Informationen finden Sie in der Beschreibung des Schema Elements " [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) ".

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert. Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

Der gemeinsam verwendete Schlüssel wurde in diesem Beispiel Profil ausgelassen. Wenn Sie versuchen, dieses Beispiel Profil zu verwenden, um eine Verbindung mit einem Netzwerk herzustellen, werden Sie zur Eingabe eines gemeinsam genutzten Schlüssels aufgefordert. Sie können diese Eingabeaufforderung vermeiden, indem Sie dem [**Security**](wlan-profileschema-security-msm-element.md) -Element unmittelbar nach dem [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element ein untergeordnetes [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element hinzufügen.

Der folgende Code Ausschnitt zeigt ein [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element, das einen unverschlüsselten Schlüssel enthält. Sie müssen den Kommentar `<!-- insert key here -->` durch den eigentlichen unverschlüsselten Schlüssel ersetzen, bevor Sie diesen Code Ausschnitt in einem Profil verwenden.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Funk profile](wireless-profile-samples.md)
</dt> </dl>

 

 



