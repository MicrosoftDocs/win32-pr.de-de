---
description: Verwendet protected Extensible Authentication Protocol mit Microsoft Challenge Handshake Authentication Protocol Version 2 mit WPA-Enterprise.
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: WPA-Enterprise mit PEAP-MSCHAPv2 Profilbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364cc7a9cc85e4c5e2ef908c0ac2a4726d6c5a96
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395045"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="73f62-103">WPA-Enterprise mit PEAP-MSCHAPv2 Profilbeispiel</span><span class="sxs-lookup"><span data-stu-id="73f62-103">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="73f62-104">Dieses Beispielprofil verwendet protected Extensible Authentication Protocol mit Microsoft Challenge Handshake Authentication Protocol Version 2 (PEAP-MSCHAPv2) mit *UserName* Password für die Authentifizierung **/**  beim Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="73f62-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="73f62-105">Der Benutzer wird aufgefordert, Anmeldeinformationen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="73f62-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="73f62-106">Dieses Beispiel ist so konfiguriert, dass die Wi-Fi geschützten Zugriff verwendet wird, die im Unternehmensmodus (WPA-Enterprise) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73f62-106">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="73f62-107">Der WPA-Enterprise verwendet 802.1X für den Authentifizierungsaustausch mit dem Back-End.</span><span class="sxs-lookup"><span data-stu-id="73f62-107">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="73f62-108">Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="73f62-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="73f62-109">**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Das [**untergeordnete Name-Element**](wlan-profileschema-name-wlanprofile-element.md) [**des WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="73f62-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="73f62-110">Der Im Profilspeicher gespeicherte Name des Profils [](wlan-profileschema-name-ssid-element.md) wird vom untergeordneten Namen des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="73f62-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="73f62-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73f62-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f62-112">Beispiele für Drahtlosprofile</span><span class="sxs-lookup"><span data-stu-id="73f62-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



