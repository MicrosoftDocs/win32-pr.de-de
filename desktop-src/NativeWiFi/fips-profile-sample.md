---
description: Wird verwendet, um eine Verbindung mit einem Netzwerk herzustellen, das Sicherheitseinstellungen erfordert, die den Standardregeln von Federal Information Processing Standards (fps) 140-2 entsprechen.
ms.assetid: 169df4a3-e8b9-4f05-874f-a7eef6658d01
title: Beispiel für ein PPS-Profil
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6d24f82a815c752a662af5f093dd9a7c34de33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131836"
---
# <a name="fips-profile-sample"></a><span data-ttu-id="ed7fc-103">Beispiel für ein PPS-Profil</span><span class="sxs-lookup"><span data-stu-id="ed7fc-103">FIPS Profile Sample</span></span>

<span data-ttu-id="ed7fc-104">Das Beispiel für ein Beispiel für den PPS-Profil Modus kann verwendet werden, um eine Verbindung mit einem Netzwerk herzustellen, das Sicherheitseinstellungen erfordert, die den standardmäßigen Standards von Federal Information Processing Standards 140-2 (Standard</span><span class="sxs-lookup"><span data-stu-id="ed7fc-104">The FIPS profile sample can be used to connect to a network that requires security settings that comply with Federal Information Processing Standards (FIPS) 140-2 standard.</span></span> <span data-ttu-id="ed7fc-105">Weitere Informationen zu "fps" finden Sie unter " [**fpsmode**](wlan-profileschema-fipsmode-authencryption-element.md)".</span><span class="sxs-lookup"><span data-stu-id="ed7fc-105">For more information about FIPS, see [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).</span></span>

<span data-ttu-id="ed7fc-106">**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-106">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="ed7fc-107">Die Standardeinstellung für [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-107">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="ed7fc-108">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-108">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="ed7fc-109">Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-109">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="ed7fc-110">Weitere Informationen finden Sie in der Beschreibung des Schema Elements " [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) ".</span><span class="sxs-lookup"><span data-stu-id="ed7fc-110">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="ed7fc-111">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="ed7fc-112">Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-112">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="ed7fc-113">Das " [**ppsmode**](wlan-profileschema-fipsmode-authencryption-element.md) "-Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed7fc-113">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is not supported.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ed7fc-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed7fc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed7fc-115">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="ed7fc-115">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



