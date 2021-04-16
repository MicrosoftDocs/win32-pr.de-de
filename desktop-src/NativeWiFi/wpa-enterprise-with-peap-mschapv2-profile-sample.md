---
description: Verwendet das Protected Extensible Authentication Protocol mit dem Microsoft Challenge Handshake Authentication-Protokollversion 2 (Peer Version 2, Peer Version 2) mit Benutzername/Kennwort, um sich beim Netzwerk zu authentifizieren.
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: Beispiel für WPA-Enterprise mit PEAP-MSCHAPv2 Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787cc2e4652d3b588b49faf2f9215cd9bd1936e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485686"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a>Beispiel für WPA-Enterprise mit PEAP-MSCHAPv2 Profil

In diesem Beispiel Profil wird das geschützte Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol Version 2 (PAP-MSCHAPv2) mit * username * **/** _Password_ verwendet, um sich beim Netzwerk zu authentifizieren. Der Benutzer wird aufgefordert, Anmelde Informationen einzugeben.

Dieses Beispiel ist für die Verwendung Wi-Fi geschützten Zugriffssicherheit konfiguriert, die im Unternehmens Modus (WPA-Enterprise) ausgeführt wird. Der WPA-Enterprise-Sicherheitstyp verwendet 802.1 x für den Authentifizierungs Austausch beim Back-End. Das Temporale Schlüssel Integritäts Protokoll (TKIP) wird für die Verschlüsselung verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert. Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.

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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Funk profile](wireless-profile-samples.md)
</dt> </dl>

 

 



