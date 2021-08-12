---
description: Verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: Beispiel für WPA-Enterprise mit TLS-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9ebb9fa779c1a1d9a4e77c20d462f31fcafc9ec562e47ae106386b58c112a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619042"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>Beispiel für WPA-Enterprise mit TLS-Profil

In diesem Beispielprofil wird EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk verwendet.

Dieses Beispiel ist für die Verwendung Wi-Fi geschützten Zugriffs konfiguriert, die im Enterprise Modus (WPA-Enterprise) ausgeführt wird. Der WPA-Enterprise Sicherheitstyp verwendet 802.1X für den Authentifizierungsaustausch mit dem Back-End. Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.

Die EAP-TLS-Anmeldeinformationen werden aus dem Zertifikatspeicher abgerufen. Wenn die Authentifizierung basierend auf den Anmeldeinformationen im Zertifikatspeicher fehlschlägt, wird der Benutzer aufgefordert, gültige Anmeldeinformationen anzugeben. Wenn der erste Versuch fehlschlägt, werden keine alternativen Server, Stammzertifizierungsstellen oder Benutzernamen für die Authentifizierung verwendet.

Die in diesem Funkprofilbeispiel verwendete EAPHost-Konfiguration wurde aus dem Beispiel für [EAP-TLS-Verbindungseigenschaften](../eaphost/eap-tls-connection-properties.md) abgeleitet.

**Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst:** Änderungen werden auf Windows 7 und Windows Server 2008 R2 mit installiertem Wlan-Dienst implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren. Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert. Die Standardeinstellung wird auf Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst in "false" geändert. Die Standardeinstellung war "true" auf Windows Server 2008 und Windows Vista. Weitere Informationen finden Sie in der [**AutoSwitch-Schemaelementbeschreibung.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** EAP-TLS wird nicht unterstützt.

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

[Beispiele für Funkprofile](wireless-profile-samples.md)
</dt> </dl>

 

 
