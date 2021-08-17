---
description: Verwendet protected Extensible Authentication Protocol mit Microsoft Challenge Handshake Authentication Protocol Version 2 mit WPA-Enterprise.
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: beispiel für WPA-Enterprise mit PEAP-MSCHAPv2 Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bd504f803795613b545c64025df3094346ea2478dd729b91ec8cec69f45c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797430"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a>beispiel für WPA-Enterprise mit PEAP-MSCHAPv2 Profil

Dieses Beispielprofil verwendet das Protected Extensible Authentication Protocol mit Microsoft Challenge Handshake Authentication Protocol Version 2 (PEAP-MSCHAPv2) mit **/** _*UserName*-Kennwort,_ um sich beim Netzwerk zu authentifizieren. Der Benutzer wird aufgefordert, Anmeldeinformationen einzugeben.

Dieses Beispiel ist so konfiguriert, dass Wi-Fi Geschützte Zugriffssicherheit verwendet wird, die im Enterprise Modus (WPA-Enterprise) ausgeführt wird. Der WPA-Enterprise Sicherheitstyp verwendet 802.1X für den Authentifizierungsaustausch mit dem Back-End. Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.

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

[Beispiele für Funkprofile](wireless-profile-samples.md)
</dt> </dl>

 

 



