---
description: Verwendet einen vorinstallierten Schlüssel für die Netzwerkauthentifizierung. Dieses Beispielprofil verwendet Wi-Fi Geschützte Zugriffssicherheit, die im persönlichen Modus (WPA-Personal) ausgeführt wird.
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Beispiel für WPA-Personal-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d196a327672ae31cb52d275be79193860fd89fff29f169be63018f5b848a4268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797420"
---
# <a name="wpa-personal-profile-sample"></a>Beispiel für WPA-Personal-Profil

Dieses Beispielprofil verwendet einen vorinstallierten Schlüssel für die Netzwerkauthentifizierung. Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben. Dieses Beispielprofil ist so konfiguriert, dass Wi-Fi Geschützte Zugriffssicherheit verwendet wird, die im persönlichen Modus (WPA-Personal) ausgeführt wird. Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.

**Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst:** Änderungen werden auf Windows 7 und Windows Server 2008 R2 mit installiertem Wlan-Dienst implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird auf Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst in "false" geändert. Die Standardeinstellung war "true" auf Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der [**AutoSwitch-Schemaelementbeschreibung.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.

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

 

 



