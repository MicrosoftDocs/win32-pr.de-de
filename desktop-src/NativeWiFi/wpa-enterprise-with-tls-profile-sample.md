---
description: Verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk.
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: Beispiel für WPA-Enterprise mit TLS-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5300f8886d55ac713b0206b45f20857f22b2772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960554"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="05052-103">Beispiel für WPA-Enterprise mit TLS-Profil</span><span class="sxs-lookup"><span data-stu-id="05052-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="05052-104">Dieses Beispiel Profil verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="05052-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="05052-105">Dieses Beispiel ist für die Verwendung Wi-Fi geschützten Zugriffssicherheit konfiguriert, die im Unternehmens Modus (WPA-Enterprise) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05052-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="05052-106">Der WPA-Enterprise-Sicherheitstyp verwendet 802.1 x für den Authentifizierungs Austausch beim Back-End.</span><span class="sxs-lookup"><span data-stu-id="05052-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="05052-107">Das Temporale Schlüssel Integritäts Protokoll (TKIP) wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="05052-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="05052-108">Die EAP-TLS-Anmelde Informationen werden aus dem Zertifikat Speicher abgerufen.</span><span class="sxs-lookup"><span data-stu-id="05052-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="05052-109">Wenn die Authentifizierung auf der Grundlage der Anmelde Informationen im Zertifikat Speicher fehlschlägt, wird der Benutzer aufgefordert, gültige Anmelde Informationen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="05052-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="05052-110">Wenn der erste Versuch fehlschlägt, werden keine alternativen Server, Stamm Zertifizierungsstellen oder Benutzernamen für die Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="05052-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="05052-111">Die in diesem drahtlos Profil Beispiel verwendete EAPHost-Konfiguration wurde aus dem Beispiel der [EAP-TLS-Verbindungs Eigenschaften](../eaphost/eap-tls-connection-properties.md) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05052-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="05052-112">**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="05052-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="05052-113">Die Standardeinstellung für [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="05052-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="05052-114">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="05052-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="05052-115">Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05052-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="05052-116">Weitere Informationen finden Sie in der Beschreibung des Schema Elements " [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) ".</span><span class="sxs-lookup"><span data-stu-id="05052-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="05052-117">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** EAP-TLS wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05052-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="05052-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05052-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05052-119">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="05052-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
