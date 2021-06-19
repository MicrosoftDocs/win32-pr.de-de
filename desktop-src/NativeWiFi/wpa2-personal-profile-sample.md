---
description: Verwendet einen vorinstallierten Schlüssel für die Netzwerkauthentifizierung. In diesem Beispielprofil wird Wi-Fi Protected Access 2-Sicherheit verwendet, die im persönlichen Modus (WPA2-Personal) ausgeführt wird.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Beispiel für WPA2-Personal Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e0df238b83a27155e640d56fc81ed5606a76e3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394865"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="d8859-104">Beispiel für WPA2-Personal Profil</span><span class="sxs-lookup"><span data-stu-id="d8859-104">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="d8859-105">Dieses Beispielprofil verwendet einen vorinstallierten Schlüssel für die Netzwerkauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="d8859-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="d8859-106">Der Schlüssel wird für den Client und den Zugriffspunkt freigegeben.</span><span class="sxs-lookup"><span data-stu-id="d8859-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="d8859-107">Dieses Beispielprofil ist für die Verwendung Wi-Fi Protected Access 2-Sicherheit konfiguriert, die im persönlichen Modus (WPA2-Personal) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8859-107">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="d8859-108">Der AES-Verschlüsselungstyp (Advanced Encryption Standard) wird für die Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8859-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="d8859-109">**Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 mit installiertem Wlan-Dienst implementiert, um die Leistung von Drahtlosnetzwerken zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="d8859-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="d8859-110">Die Standardeinstellung für [**autoSwitch,**](wlan-profileschema-autoswitch-wlanprofile-element.md) wenn dieses Element nicht in einem WLAN-Profil festgelegt ist, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="d8859-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="d8859-111">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst in "false" geändert.</span><span class="sxs-lookup"><span data-stu-id="d8859-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="d8859-112">Die Standardeinstellung war "true" unter Windows Server 2008 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8859-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="d8859-113">Weitere Informationen finden Sie in der [**AutoSwitch-Schemaelementbeschreibung.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="d8859-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="d8859-114">**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Der [**untergeordnete Name**](wlan-profileschema-name-wlanprofile-element.md) des [**WLANProfile-Elements**](wlan-profileschema-wlanprofile-element.md) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d8859-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="d8859-115">Der Name des Profils, wie er im Profilspeicher gespeichert ist, wird vom [**untergeordneten Namen**](wlan-profileschema-name-ssid-element.md) des [**SSID-Elements**](wlan-profileschema-ssid-ssidconfig-element.md) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8859-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="d8859-116">Der gemeinsam verwendete Schlüssel wurde in diesem Beispielprofil ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="d8859-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="d8859-117">Wenn Sie versuchen, dieses Beispielprofil zum Herstellen einer Verbindung mit einem Netzwerk zu verwenden, werden Sie aufgefordert, einen gemeinsam verwendeten Schlüssel einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d8859-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="d8859-118">Sie können diese Aufforderung vermeiden, indem Sie dem [**Sicherheitselement**](wlan-profileschema-security-msm-element.md) unmittelbar nach dem [**authEncryption-Element**](wlan-profileschema-authencryption-security-element.md) ein [**untergeordnetes sharedKey-Element**](wlan-profileschema-sharedkey-security-element.md) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8859-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="d8859-119">Der folgende Codeausschnitt zeigt ein [**sharedKey-Element,**](wlan-profileschema-sharedkey-security-element.md) das einen unverschlüsselten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="d8859-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="d8859-120">Sie müssen den Kommentar `<!-- insert key here -->` durch den eigentlichen unverschlüsselten Schlüssel ersetzen, bevor Sie diesen Codeausschnitt in einem Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8859-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="d8859-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8859-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8859-122">Beispiele für Funkprofile</span><span class="sxs-lookup"><span data-stu-id="d8859-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



