---
description: Verwendet einen vorinstallierten Schlüssel für die Netzwerkauthentifizierung. In diesem Beispielprofil wird Wi-Fi Protected Access 2-Sicherheit verwendet, die im persönlichen Modus (WPA2-Personal) ausgeführt wird.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Beispiel für WPA2-Personal Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e0df238b83a27155e640d56fc81ed5606a76e3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394865"
---
# <a name="wpa2-personal-profile-sample"></a>Beispiel für WPA2-Personal Profil

Dieses Beispielprofil verwendet einen vorinstallierten Schlüssel für die Netzwerkauthentifizierung. Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben. Dieses Beispielprofil ist für die Verwendung Wi-Fi Protected Access 2-Sicherheit konfiguriert, die im persönlichen Modus (WPA2-Personal) ausgeführt wird. Der AES-Verschlüsselungstyp (Advanced Encryption Standard) wird für die Verschlüsselung verwendet.

**Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 mit installiertem Wlan-Dienst implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst in "false" geändert. Die Standardeinstellung war "true" unter Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der [**AutoSwitch-Schemaelementbeschreibung.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.

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

Der gemeinsam verwendete Schlüssel wurde in diesem Beispielprofil ausgelassen. Wenn Sie versuchen, dieses Beispielprofil zum Herstellen einer Verbindung mit einem Netzwerk zu verwenden, werden Sie aufgefordert, einen gemeinsam verwendeten Schlüssel einzugeben. Sie können diese Aufforderung vermeiden, indem Sie dem [**Sicherheitselement**](wlan-profileschema-security-msm-element.md) unmittelbar nach dem [**authEncryption-Element**](wlan-profileschema-authencryption-security-element.md) ein [**untergeordnetes sharedKey-Element**](wlan-profileschema-sharedkey-security-element.md) hinzufügen.

Der folgende Codeausschnitt zeigt ein [**sharedKey-Element,**](wlan-profileschema-sharedkey-security-element.md) das einen unverschlüsselten Schlüssel enthält. Sie müssen den Kommentar `<!-- insert key here -->` durch den eigentlichen unverschlüsselten Schlüssel ersetzen, bevor Sie diesen Codeausschnitt in einem Profil verwenden.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Funkprofile](wireless-profile-samples.md)
</dt> </dl>

 

 



