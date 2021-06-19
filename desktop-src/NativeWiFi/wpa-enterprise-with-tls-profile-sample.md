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
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="0378e-103">WPA-Enterprise mit TLS-Profilbeispiel</span><span class="sxs-lookup"><span data-stu-id="0378e-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="0378e-104">Dieses Beispielprofil verwendet EAP-TLS (Extensible Authentication Protocol Transport Level Security) mit Zertifikaten für die Authentifizierung beim Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0378e-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="0378e-105">Dieses Beispiel ist so konfiguriert, dass die Wi-Fi geschützten Zugriff verwendet wird, die im Unternehmensmodus (WPA-Enterprise) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0378e-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="0378e-106">Der WPA-Enterprise verwendet 802.1X für den Authentifizierungsaustausch mit dem Back-End.</span><span class="sxs-lookup"><span data-stu-id="0378e-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="0378e-107">Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0378e-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="0378e-108">Die EAP-TLS-Anmeldeinformationen werden aus dem Zertifikatspeicher erhalten.</span><span class="sxs-lookup"><span data-stu-id="0378e-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="0378e-109">Wenn die Authentifizierung basierend auf den Anmeldeinformationen im Zertifikatspeicher fehlschlägt, wird der Benutzer aufgefordert, gültige Anmeldeinformationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0378e-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="0378e-110">Für die Authentifizierung werden keine alternativen Server, Stammzertifizierungsstellen oder Benutzernamen verwendet, wenn der erste Versuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0378e-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="0378e-111">Die in diesem Funkprofilbeispiel verwendete EAPHost-Konfiguration wurde aus dem [Beispiel für EAP-TLS-Verbindungseigenschaften](../eaphost/eap-tls-connection-properties.md) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0378e-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="0378e-112">**Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="0378e-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="0378e-113">Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="0378e-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="0378e-114">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 mit installierten WLAN-Diensten in "false" geändert.</span><span class="sxs-lookup"><span data-stu-id="0378e-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="0378e-115">Die Standardeinstellung war "true" unter Windows Server 2008 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0378e-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="0378e-116">Weitere Informationen finden Sie in der Beschreibung des [**Schemaelements autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="0378e-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="0378e-117">**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** EAP-TLS wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0378e-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0378e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0378e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0378e-119">Beispiele für Drahtlosprofile</span><span class="sxs-lookup"><span data-stu-id="0378e-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
