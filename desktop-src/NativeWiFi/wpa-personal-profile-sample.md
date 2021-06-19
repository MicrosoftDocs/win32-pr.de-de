---
description: Verwendet einen vorinstallten Schlüssel für die Netzwerkauthentifizierung. In diesem Beispielprofil wird Wi-Fi Protected Access-Sicherheit verwendet, die im persönlichen Modus (WPA-Personal) ausgeführt wird.
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: WPA-Personal Profilbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334076d4b0cf10372ed845265a1fff652f0879b9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395025"
---
# <a name="wpa-personal-profile-sample"></a><span data-ttu-id="6778a-104">WPA-Personal Profilbeispiel</span><span class="sxs-lookup"><span data-stu-id="6778a-104">WPA-Personal Profile Sample</span></span>

<span data-ttu-id="6778a-105">Dieses Beispielprofil verwendet einen vorinstallten Schlüssel für die Netzwerkauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="6778a-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="6778a-106">Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben.</span><span class="sxs-lookup"><span data-stu-id="6778a-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="6778a-107">Dieses Beispielprofil ist für die Verwendung Wi-Fi geschützten Zugriffssicherheit konfiguriert, die im persönlichen Modus (WPA-Personal) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6778a-107">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="6778a-108">Das Temporal Key Integrity Protocol (TKIP) wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6778a-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="6778a-109">**Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 mit installierten Wlan-Diensten implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="6778a-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="6778a-110">Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="6778a-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="6778a-111">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 mit installierten WLAN-Diensten in "false" geändert.</span><span class="sxs-lookup"><span data-stu-id="6778a-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="6778a-112">Die Standardeinstellung war "true" unter Windows Server 2008 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6778a-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="6778a-113">Weitere Informationen finden Sie in der Beschreibung des [**Schemaelements autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="6778a-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="6778a-114">**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Das [**untergeordnete Name-Element**](wlan-profileschema-name-wlanprofile-element.md) [**des WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6778a-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="6778a-115">Der Im Profilspeicher gespeicherte Name des Profils [](wlan-profileschema-name-ssid-element.md) wird vom untergeordneten Namen des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6778a-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="6778a-116">Der gemeinsam genutzte Schlüssel wurde in diesem Beispielprofil ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6778a-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="6778a-117">Wenn Sie versuchen, dieses Beispielprofil zum Herstellen einer Verbindung mit einem Netzwerk zu verwenden, werden Sie aufgefordert, einen gemeinsam genutzten Schlüssel ein geben.</span><span class="sxs-lookup"><span data-stu-id="6778a-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="6778a-118">Sie können diese Aufforderung vermeiden, indem Sie [](wlan-profileschema-security-msm-element.md) dem Security-Element unmittelbar nach dem [**authEncryption-Element ein**](wlan-profileschema-authencryption-security-element.md) untergeordnetes [**sharedKey-Element**](wlan-profileschema-sharedkey-security-element.md) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6778a-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="6778a-119">Der folgende Codeausschnitt zeigt ein [**sharedKey-Element,**](wlan-profileschema-sharedkey-security-element.md) das einen unverschlüsselten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="6778a-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="6778a-120">Sie müssen den Kommentar durch den tatsächlich unverschlüsselten Schlüssel ersetzen, bevor Sie diesen `<!-- insert key here -->` Codeausschnitt in einem Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="6778a-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="6778a-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6778a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6778a-122">Beispiele für Drahtlosprofile</span><span class="sxs-lookup"><span data-stu-id="6778a-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



