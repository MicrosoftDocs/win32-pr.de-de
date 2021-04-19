---
description: Wird verwendet, um eine Verbindung mit Netzwerken herzustellen, die nicht Ihren Netzwerknamen oder Ihre SSID übertragen.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Beispiel für nicht-Broadcast Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362204"
---
# <a name="non-broadcast-profile-sample"></a><span data-ttu-id="295d4-103">Beispiel für nicht-Broadcast Profil</span><span class="sxs-lookup"><span data-stu-id="295d4-103">Non-Broadcast Profile Sample</span></span>

<span data-ttu-id="295d4-104">Das nicht-Broadcast Profil Beispiel kann verwendet werden, um eine Verbindung mit Netzwerken herzustellen, die nicht Ihren Netzwerknamen oder Ihre SSID übertragen.</span><span class="sxs-lookup"><span data-stu-id="295d4-104">The non-broadcast profile sample can be used to connect to networks which do not broadcast their network name or SSID.</span></span>

<span data-ttu-id="295d4-105">Dieses Beispiel Profil ist für die Verwendung Wi-Fi geschützten Zugriffssicherheit konfiguriert, die im persönlichen Modus (WPA-Personal) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="295d4-105">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="295d4-106">Das Temporale Schlüssel Integritäts Protokoll (TKIP) wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="295d4-106">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span> <span data-ttu-id="295d4-107">Profile, die andere Sicherheits-und Chiffre Typen verwenden, können auch als nicht-Broadcast-Profile konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="295d4-107">Profiles that use other security and cipher types can also be configured as non-broadcast profiles.</span></span>

<span data-ttu-id="295d4-108">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="295d4-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="295d4-109">Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="295d4-109">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

<span data-ttu-id="295d4-110">Der gemeinsam verwendete Schlüssel wurde in diesem Beispiel Profil ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="295d4-110">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="295d4-111">Wenn Sie versuchen, dieses Beispiel Profil zu verwenden, um eine Verbindung mit einem Netzwerk herzustellen, werden Sie zur Eingabe eines gemeinsam genutzten Schlüssels aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="295d4-111">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="295d4-112">Sie können diese Eingabeaufforderung vermeiden, indem Sie dem [**Security**](wlan-profileschema-security-msm-element.md) -Element unmittelbar nach dem [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element ein untergeordnetes [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="295d4-112">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="295d4-113">Der folgende Code Ausschnitt zeigt ein [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element, das einen unverschlüsselten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="295d4-113">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="295d4-114">Sie müssen den Kommentar `<!-- insert key here -->` durch den eigentlichen unverschlüsselten Schlüssel ersetzen, bevor Sie diesen Code Ausschnitt in einem Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="295d4-114">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="295d4-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="295d4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="295d4-116">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="295d4-116">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



