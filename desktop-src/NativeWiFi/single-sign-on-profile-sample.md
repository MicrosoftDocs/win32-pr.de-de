---
description: Wird für Szenarien verwendet, die vor Windows Anmeldung eine 802.1X-Authentifizierung erfordern.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Beispiel für ein einzelnes Sign-On Profil
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f89f7e9c39123cd7bf55c8bc48ff69d007d150c086714c82c37619c477dd25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797955"
---
# <a name="single-sign-on-profile-sample"></a>Beispiel für ein einzelnes Sign-On Profil

Das Profilbeispiel für einmaliges Anmelden (Single Sign-On, SSO) kann für Szenarien verwendet werden, die vor Windows Anmeldung eine 802.1X-Authentifizierung erfordern.

Dieses Beispiel ist so konfiguriert, dass Wi-Fi Protected Access 2-Sicherheit verwendet wird, die im Enterprise Modus (WPA2-Enterprise) ausgeführt wird. Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol Version 2 (PEAP-MSCHAPv2) wird für die Netzwerkauthentifizierung verwendet. Die Windows Anmeldeinformationen werden für PEAP-MSCHAPv2 Authentifizierung verwendet.

Während dieses Beispiel für die Verwendung von WPA2-Enterprise und PEAP-MSCHAPv2 konfiguriert ist, können SSO-Profile mit anderen Sicherheits- und Authentifizierungstypen konfiguriert werden.

**Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst:** Änderungen werden auf Windows 7 und Windows Server 2008 R2 mit installiertem Wlan-Dienst implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird auf Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst in "false" geändert. Die Standardeinstellung war "true" auf Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der [**AutoSwitch-Schemaelementbeschreibung.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet. Die untergeordneten Elemente [**cacheUserData,**](onexschema-cacheuserdata-onex-element.md) [**maxAuthFailures,**](onexschema-maxauthfailures-onex-element.md) [**authMode**](onexschema-authmode-onex-element.md)und [**singleSignOn**](onexschema-singlesignon-onex-element.md) des [**OneX-Elements**](onexschema-onex-element.md) werden nicht unterstützt und sollten vor der Verwendung aus dem Profil entfernt werden.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleSingleSignOn</name>
    <SSIDConfig>
        <SSID>
            <name>SampleSingleSignOn</name>
        </SSID>
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
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <maxAuthFailures>3</maxAuthFailures>
                <authMode>user</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
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
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
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

 

 



