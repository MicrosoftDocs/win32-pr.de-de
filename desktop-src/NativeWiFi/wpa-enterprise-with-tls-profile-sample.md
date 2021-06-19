---
description: Verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: WPA-Enterprise mit TLS-Profilbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d6f236429c94e9602e173c2d6c3eb1e3bc8111f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395035"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>WPA-Enterprise mit TLS-Profilbeispiel

Dieses Beispielprofil verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk.

Dieses Beispiel ist so konfiguriert, dass die Wi-Fi geschützten Zugriff verwendet wird, die im Unternehmensmodus (WPA-Enterprise) ausgeführt wird. Der WPA-Enterprise verwendet 802.1X für den Authentifizierungsaustausch mit dem Back-End. Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.

Die EAP-TLS-Anmeldeinformationen werden aus dem Zertifikatspeicher erhalten. Wenn die Authentifizierung basierend auf den Anmeldeinformationen im Zertifikatspeicher fehlschlägt, wird der Benutzer aufgefordert, gültige Anmeldeinformationen anzugeben. Für die Authentifizierung werden keine alternativen Server, Stammzertifizierungsstellen oder Benutzernamen verwendet, wenn der erste Versuch fehlschlägt.

Die in diesem Funkprofilbeispiel verwendete EAPHost-Konfiguration wurde aus dem [Beispiel für EAP-TLS-Verbindungseigenschaften](../eaphost/eap-tls-connection-properties.md) abgeleitet.

**Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 mit installierten WLAN-Diensten in "false" geändert. Die Standardeinstellung war "true" unter Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der Beschreibung des [**Schemaelements autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** EAP-TLS wird nicht unterstützt.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
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

[Beispiele für Drahtlosprofile](wireless-profile-samples.md)
</dt> </dl>

 

 
