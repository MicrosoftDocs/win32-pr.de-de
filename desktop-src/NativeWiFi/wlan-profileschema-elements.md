---
description: 'Das WLAN- \_ Profil Schema definiert die folgenden Elemente:'
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Schema Elemente WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752305"
---
# <a name="wlan_profile-schema-elements"></a>WLAN- \_ Profil Schema Elemente

Das WLAN- \_ Profil Schema definiert die folgenden Elemente: Die meisten-Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/WLAN/profile/v1` , mit Ausnahme von " [**fpsmode" (authencryption)**](wlan-profileschema-fipsmode-authencryption-element.md), die sich im-Namespace befindet `https://www.microsoft.com/networking/WLAN/profile/v2` .

In der folgenden Liste werden die definierten Elemente in der Reihenfolge angezeigt, in der die Elemente in einem Profil angezeigt werden. Die Reihenfolge der Elemente wird erzwungen. Nicht alle Elemente befinden sich in jedem Profil, da einige Elemente optional sind.

In dieser Liste werden nicht alle möglichen Elemente angezeigt, die in einem drahtlos Profil angezeigt werden können, da Elemente in **xs: beliebige** Einfügepunkte hinzugefügt werden können.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**Name (wlanprofile)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**Ssidconfig (wlanprofile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (ssidconfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**Hex (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**Name (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**nicht Broadcast (ssidconfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (wlanprofile)**](wlan-profileschema-hotspot2-element.md)
        -   [**Domain Name (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**Nairealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**Roamingconsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (wlanprofile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**ConnectionMode (wlanprofile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**autoswitch (wlanprofile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (wlanprofile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**Konnektivität (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phytype (Konnektivität)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**authencryption (Sicherheit)**](wlan-profileschema-authencryption-security-element.md)
                -   [**Authentifizierung (authencryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**Verschlüsselung (authencryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useonex (authencryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**"Fpsmode" (authencryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedkey (Sicherheit)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**KeyType (sharedkey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**geschützt (sharedkey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**Keymaterial (sharedkey)**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**KeyIndex (Sicherheit)**](wlan-profileschema-keyindex-security-element.md)
            -   [**Pmkcachemode (Sicherheit)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**Pmkcachettl (Sicherheit)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**Pmkcachesize (Sicherheit)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**preauthmode (Sicherheit)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**preauththrottle (Sicherheit)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (wlanprofile)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**Ouiheader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (ouiheader)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**Type (ouiheader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**Konnektivität (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**Sicherheit (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**usemsonex (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



