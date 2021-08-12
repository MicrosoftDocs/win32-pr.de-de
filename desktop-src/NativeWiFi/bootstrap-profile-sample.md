---
description: Wird verwendet, um sich zum ersten Mal bei einem Drahtlosnetzwerk zu authentifizieren, bevor der Computer einer Domäne beigetreten ist.
ms.assetid: e1a5ce76-9761-4c65-8b26-a44bf2eb1835
title: Bootstrap-Profilbeispiel
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4aa83aa04ce4a442351485c25fbc7f4c6d252f923f6777cfe807abf9ba527a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620217"
---
# <a name="bootstrap-profile-sample"></a>Bootstrap-Profilbeispiel

Das Bootstrap-Profilbeispiel kann verwendet werden, um sich zum ersten Mal bei einem Drahtlosnetzwerk zu authentifizieren, bevor der Computer einer Domäne beigetreten ist.

Dieses Profil überprüft nicht die vom RADIUS-Server (Remote Authentication Dial-In User Service) angezeigten Zertifikate und sollte nicht verwendet werden, nachdem der Computer in eine Domäne eingebunden wurde.

Dieses Beispiel ist so konfiguriert, dass Wi-Fi Protected Access 2-Sicherheit verwendet wird, die im Enterprise Modus (WPA2-Enterprise) ausgeführt wird. Andere Sicherheitstypen können verwendet werden, solange die Authentifizierungsmethode PEAP-MSCHAPv2 ist.

**Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst:** Änderungen werden auf Windows 7 und Windows Server 2008 R2 mit installiertem Wlan-Dienst implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird auf Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst in "false" geändert. Die Standardeinstellung war "true" auf Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der [**AutoSwitch-Schemaelementbeschreibung.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert. Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet. Die untergeordneten [**Elemente cacheUserData,**](onexschema-cacheuserdata-onex-element.md) [**authMode**](onexschema-authmode-onex-element.md)und [**singleSignOn**](onexschema-singlesignon-onex-element.md) des [**OneX-Elements**](onexschema-onex-element.md) werden nicht unterstützt und sollten vor der Verwendung aus dem Profil entfernt werden.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleBootstrap</name>
    <SSIDConfig>
        <SSID>
            <name>SampleBootstrap</name>
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
                <authMode>machineOrUser</authMode>
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
               </EAPConfig>
           </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele für Funkprofile](wireless-profile-samples.md)
</dt> <dt>

[Verknüpfen eines Windows Vista Wireless Client mit einer Domäne](https://www.microsoft.com/technet/network/wifi/vista_bootstrap_wireless.mspx)
</dt> </dl>

 

 



