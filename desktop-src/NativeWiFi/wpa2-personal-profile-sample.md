---
description: Verwendet einen vorinstallierten Schlüssel für die Netzwerk Authentifizierung.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Beispiel für WPA2-Personal Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0054bc28962113a85bb909d4e8cd173b3bc16974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348119"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="2076e-103">Beispiel für WPA2-Personal Profil</span><span class="sxs-lookup"><span data-stu-id="2076e-103">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="2076e-104">In diesem Beispiel Profil wird ein vorinstaltzter Schlüssel für die Netzwerk Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2076e-104">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="2076e-105">Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben.</span><span class="sxs-lookup"><span data-stu-id="2076e-105">The key is shared with the client and the access point.</span></span> <span data-ttu-id="2076e-106">Dieses Beispiel Profil ist für die Verwendung Wi-Fi geschützten Zugriffs 2-Sicherheit konfiguriert, die im persönlichen Modus (WPA2-Personal) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2076e-106">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="2076e-107">Der Advanced Encryption Standard (AES)-Chiffre Typ wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2076e-107">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="2076e-108">**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="2076e-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="2076e-109">Die Standardeinstellung für [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="2076e-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="2076e-110">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2076e-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="2076e-111">Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2076e-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="2076e-112">Weitere Informationen finden Sie in der Beschreibung des Schema Elements " [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) ".</span><span class="sxs-lookup"><span data-stu-id="2076e-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="2076e-113">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Der untergeordnete [**Name**](wlan-profileschema-name-wlanprofile-element.md) des [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Elements wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2076e-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="2076e-114">Der Name des Profils, wie er im Profil Speicher gespeichert ist, wird vom untergeordneten [**Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2076e-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="2076e-115">Der gemeinsam verwendete Schlüssel wurde in diesem Beispiel Profil ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="2076e-115">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="2076e-116">Wenn Sie versuchen, dieses Beispiel Profil zu verwenden, um eine Verbindung mit einem Netzwerk herzustellen, werden Sie zur Eingabe eines gemeinsam genutzten Schlüssels aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2076e-116">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="2076e-117">Sie können diese Eingabeaufforderung vermeiden, indem Sie dem [**Security**](wlan-profileschema-security-msm-element.md) -Element unmittelbar nach dem [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element ein untergeordnetes [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2076e-117">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="2076e-118">Der folgende Code Ausschnitt zeigt ein [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element, das einen unverschlüsselten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="2076e-118">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="2076e-119">Sie müssen den Kommentar `<!-- insert key here -->` durch den eigentlichen unverschlüsselten Schlüssel ersetzen, bevor Sie diesen Code Ausschnitt in einem Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="2076e-119">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="2076e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2076e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2076e-121">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="2076e-121">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



