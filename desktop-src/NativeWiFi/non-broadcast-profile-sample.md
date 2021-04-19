---
description: Wird verwendet, um eine Verbindung mit Netzwerken herzustellen, die nicht Ihren Netzwerknamen oder Ihre SSID übertragen.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Beispiel für nicht-Broadcast Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362204"
---
# <a name="non-broadcast-profile-sample"></a>Beispiel für nicht-Broadcast Profil

Das nicht-Broadcast Profil Beispiel kann verwendet werden, um eine Verbindung mit Netzwerken herzustellen, die nicht Ihren Netzwerknamen oder Ihre SSID übertragen.

Dieses Beispiel Profil ist für die Verwendung Wi-Fi geschützten Zugriffssicherheit konfiguriert, die im persönlichen Modus (WPA-Personal) ausgeführt wird. Das Temporale Schlüssel Integritäts Protokoll (TKIP) wird für die Verschlüsselung verwendet. Profile, die andere Sicherheits-und Chiffre Typen verwenden, können auch als nicht-Broadcast-Profile konfiguriert werden.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert. Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

 

 



