---
description: Verwendet protected Extensible Authentication Protocol mit Microsoft Challenge Handshake Authentication Protocol, Version 2, mit WPA2-Enterprise.
ms.assetid: fcbc74a6-1990-45a0-af2e-1c343a84497a
title: beispiel für WPA2-Enterprise mit PEAP-MSCHAPv2 Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd05ac34992244eedae08f9c76becd5b2c95564e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394805"
---
# <a name="wpa2-enterprise-with-peap-mschapv2-profile-sample"></a>beispiel für WPA2-Enterprise mit PEAP-MSCHAPv2 Profil

Dieses Beispielprofil verwendet das Protected Extensible Authentication-Protokoll mit Microsoft Challenge Handshake Authentication Protocol Version 2 (PEAP-MSCHAPv2) mit **/** _*UserName*-Kennwort,_ um sich beim Netzwerk zu authentifizieren. Der Benutzer wird aufgefordert, Anmeldeinformationen einzugeben.

Dieses Beispiel ist für die Verwendung Wi-Fi Protected Access 2-Sicherheit konfiguriert, die im Enterprise-Modus (WPA2-Enterprise) ausgeführt wird. Der WPA2-Enterprise Sicherheitstyp verwendet 802.1X für den Authentifizierungsaustausch mit dem Back-End. Der AES-Verschlüsselungstyp (Advanced Encryption Standard) wird für die Verschlüsselung verwendet.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.

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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Funkprofile](wireless-profile-samples.md)
</dt> </dl>

 

 



