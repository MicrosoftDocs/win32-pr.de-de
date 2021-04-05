---
description: Verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk.
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: Beispiel für WPA2-Enterprise mit TLS-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd85d30bed631a55f0e7e622aac4a8ade17ba3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041751"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a>Beispiel für WPA2-Enterprise mit TLS-Profil

Dieses Beispiel Profil verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk.

Dieses Beispiel ist für die Verwendung Wi-Fi geschützten Zugriffs 2-Sicherheit konfiguriert, die im Unternehmens Modus (WPA2-Enterprise) ausgeführt wird. Der WPA2-Enterprise-Sicherheitstyp verwendet 802.1 x für den Authentifizierungs Austausch beim Back-End. Der Advanced Encryption Standard (AES)-Chiffre Typ wird für die Verschlüsselung verwendet.

Die EAP-TLS-Anmelde Informationen werden aus dem Zertifikat Speicher abgerufen. Wenn die Authentifizierung auf der Grundlage der Anmelde Informationen im Zertifikat Speicher fehlschlägt, wird der Benutzer aufgefordert, gültige Anmelde Informationen einzugeben. Wenn der erste Versuch fehlschlägt, werden keine alternativen Server, Stamm Zertifizierungsstellen oder Benutzernamen für die Authentifizierung verwendet.

Die in diesem drahtlos Profil Beispiel verwendete EAPHost-Konfiguration wurde aus dem Beispiel der [EAP-TLS-Verbindungs Eigenschaften](../eaphost/eap-tls-connection-properties.md) abgeleitet.

**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren. Die Standardeinstellung für [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert. Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist. Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt. Weitere Informationen finden Sie in der Beschreibung des Schema Elements " [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) ".

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** EAP-TLS wird nicht unterstützt.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterpriseTLS</name>
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
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
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

 

 
