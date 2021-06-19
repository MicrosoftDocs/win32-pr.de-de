---
description: Verwendet einen vorinstallten Schlüssel für die Netzwerkauthentifizierung. In diesem Beispielprofil wird Wi-Fi Protected Access-Sicherheit verwendet, die im persönlichen Modus (WPA-Personal) ausgeführt wird.
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: WPA-Personal Profilbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334076d4b0cf10372ed845265a1fff652f0879b9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395025"
---
# <a name="wpa-personal-profile-sample"></a>WPA-Personal Profilbeispiel

Dieses Beispielprofil verwendet einen vorinstallten Schlüssel für die Netzwerkauthentifizierung. Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben. Dieses Beispielprofil ist für die Verwendung Wi-Fi geschützten Zugriffssicherheit konfiguriert, die im persönlichen Modus (WPA-Personal) ausgeführt wird. Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.

**Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 mit installierten WLAN-Diensten in "false" geändert. Die Standardeinstellung war "true" unter Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der Beschreibung des [**Schemaelements autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Das [**untergeordnete Name-Element**](wlan-profileschema-name-wlanprofile-element.md) [**des WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Im Profilspeicher gespeicherte Name des Profils [](wlan-profileschema-name-ssid-element.md) wird vom untergeordneten Namen des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

Der gemeinsam genutzte Schlüssel wurde in diesem Beispielprofil ausgelassen. Wenn Sie versuchen, dieses Beispielprofil zum Herstellen einer Verbindung mit einem Netzwerk zu verwenden, werden Sie aufgefordert, einen gemeinsam genutzten Schlüssel ein geben. Sie können diese Aufforderung vermeiden, indem Sie [](wlan-profileschema-security-msm-element.md) dem Security-Element unmittelbar nach dem [**authEncryption-Element ein**](wlan-profileschema-authencryption-security-element.md) untergeordnetes [**sharedKey-Element**](wlan-profileschema-sharedkey-security-element.md) hinzufügen.

Der folgende Codeausschnitt zeigt ein [**sharedKey-Element,**](wlan-profileschema-sharedkey-security-element.md) das einen unverschlüsselten Schlüssel enthält. Sie müssen den Kommentar durch den tatsächlich unverschlüsselten Schlüssel ersetzen, bevor Sie diesen `<!-- insert key here -->` Codeausschnitt in einem Profil verwenden.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Drahtlosprofile](wireless-profile-samples.md)
</dt> </dl>

 

 



