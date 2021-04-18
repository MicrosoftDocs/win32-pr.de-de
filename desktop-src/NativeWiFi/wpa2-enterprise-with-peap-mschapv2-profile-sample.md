---
description: Verwendet das Protected Extensible Authentication Protocol mit dem Microsoft Challenge Handshake Authentication-Protokollversion 2 (Peer Version 2, Peer Version 2) mit Benutzername/Kennwort, um sich beim Netzwerk zu authentifizieren.
ms.assetid: fcbc74a6-1990-45a0-af2e-1c343a84497a
title: Beispiel für WPA2-Enterprise mit PEAP-MSCHAPv2 Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43363be10a6d7d77d445e188b1c3084f71ce3b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352271"
---
# <a name="wpa2-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="02b61-103">Beispiel für WPA2-Enterprise mit PEAP-MSCHAPv2 Profil</span><span class="sxs-lookup"><span data-stu-id="02b61-103">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="02b61-104">In diesem Beispiel Profil wird das geschützte Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol Version 2 (PAP-MSCHAPv2) mit \* username \* **/** _Password_ verwendet, um sich beim Netzwerk zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="02b61-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="02b61-105">Der Benutzer wird aufgefordert, Anmelde Informationen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="02b61-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="02b61-106">Dieses Beispiel ist für die Verwendung Wi-Fi geschützten Zugriffs 2-Sicherheit konfiguriert, die im Unternehmens Modus (WPA2-Enterprise) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02b61-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="02b61-107">Der WPA2-Enterprise-Sicherheitstyp verwendet 802.1 x für den Authentifizierungs Austausch beim Back-End.</span><span class="sxs-lookup"><span data-stu-id="02b61-107">The WPA2-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="02b61-108">Der Advanced Encryption Standard (AES)-Chiffre Typ wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="02b61-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="02b61-109">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="02b61-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="02b61-110">Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="02b61-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
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

## <a name="related-topics"></a><span data-ttu-id="02b61-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02b61-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b61-112">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="02b61-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



