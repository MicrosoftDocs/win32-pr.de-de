---
description: Wird verwendet, um eine Verbindung mit einem Netzwerk herzustellen, das Sicherheitseinstellungen erfordert, die dem FIPS 140-2-Standard (Federal Information Processing Standards) entsprechen.
ms.assetid: 169df4a3-e8b9-4f05-874f-a7eef6658d01
title: FIPS-Profilbeispiel
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 688a5811407d8a0d48963a54db9fc0d717b75a719ba8879ba20f1e83cbf7012e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801290"
---
# <a name="fips-profile-sample"></a>FIPS-Profilbeispiel

Das FIPS-Profilbeispiel kann verwendet werden, um eine Verbindung mit einem Netzwerk herzustellen, das Sicherheitseinstellungen erfordert, die dem FIPS 140-2-Standard (Federal Information Processing Standards) entsprechen. Weitere Informationen zu FIPS finden Sie unter [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).

**Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten:** Änderungen werden auf Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird in "false" auf Windows 7 und Windows Server 2008 R2 mit installierter Wlan-Dienst geändert. Die Standardeinstellung war "true" auf Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der Beschreibung des [**Schemaelements autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Das [**untergeordnete Name-Element**](wlan-profileschema-name-wlanprofile-element.md) [**des WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Im Profilspeicher gespeicherte Name des Profils [](wlan-profileschema-name-ssid-element.md) wird vom untergeordneten Namen des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet. Das [**FIPSMode-Element**](wlan-profileschema-fipsmode-authencryption-element.md) wird nicht unterstützt.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>FIPS_TEST</name>
    <SSIDConfig>
        <SSID>
            <hex>464950535F54455354</hex>
            <name>FIPS_TEST</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
                <FIPSMode xmlns="https://www.microsoft.com/networking/WLAN/profile/v2">true</FIPSMode>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig">
                    <EapMethod>
                        <Type xmlns="https://www.microsoft.com/provisioning/EapCommon">25</Type>
                        <VendorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorId>
                        <VendorType xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorType>
                        <AuthorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</AuthorId>
                    </EapMethod>
                    <ConfigBlob></ConfigBlob>
                    </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Drahtlosprofile](wireless-profile-samples.md)
</dt> </dl>

 

 



