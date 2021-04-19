---
description: Definiert einen Algorithmus für die drahtlose LAN-Authentifizierung.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: DOT11_AUTH_ALGORITHM-Enumeration (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349921"
---
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="795ff-103">DOT11 \_ auth- \_ algorithmusenumeration</span><span class="sxs-lookup"><span data-stu-id="795ff-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="795ff-104">Der enumerierte Typ des **DOT11 \_ auth- \_ Algorithmus** definiert einen drahtlosen LAN-Authentifizierungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="795ff-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="795ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="795ff-105">Syntax</span></span>


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="795ff-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="795ff-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="795ff-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ auth \_ algo \_ 80211 \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="795ff-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-108">Gibt einen IEEE 802,11-Algorithmus für die Open-System Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="795ff-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ auth \_ algo \_ 80211 \_ gemeinsam verwendeter \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="795ff-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-110">Gibt einen 802,11-Algorithmus für die gemeinsame Schlüssel Authentifizierung an, der die Verwendung eines vorinstallierten WEP-Schlüssels (Wired Equivalent Privacy) für die 802,11-Authentifizierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="795ff-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ auth \_ algo \_ WPA**</span><span class="sxs-lookup"><span data-stu-id="795ff-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-112">Gibt einen WPA (Wi-Fi Protected Access)-Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="795ff-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="795ff-113">Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant-, Authenticator-und Authentifizierungsserver.</span><span class="sxs-lookup"><span data-stu-id="795ff-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="795ff-114">Verschlüsselungsschlüssel werden dynamisch durch den Authentifizierungsprozess abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="795ff-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="795ff-115">Dieser Algorithmus ist nur für BSS-Typen der Dot11 \_ BSS \_ - \_ typanfrastruktur gültig.</span><span class="sxs-lookup"><span data-stu-id="795ff-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="795ff-116">Wenn der WPA-Algorithmus aktiviert ist, wird die 802,11-Station nur mit einem Zugriffspunkt verknüpft, dessen Leucht-oder Test Antworten die Authentifizierungs Suite vom Typ 1 (802.1 x) im WPA Information-Element (IE) enthalten.</span><span class="sxs-lookup"><span data-stu-id="795ff-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="795ff-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ auth \_ algo \_ WPA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="795ff-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-118">Gibt einen WPA-Algorithmus an, der vorinstallierten Keys (PSK) verwendet.</span><span class="sxs-lookup"><span data-stu-id="795ff-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="795ff-119">Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant und Authentifikator.</span><span class="sxs-lookup"><span data-stu-id="795ff-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="795ff-120">Verschlüsselungsschlüssel werden dynamisch über einen vorinstallierten Schlüssel abgeleitet, der sowohl für den Supplicant als auch für den Authentifikator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795ff-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="795ff-121">Dieser Algorithmus ist nur für BSS-Typen der **Dot11 \_ BSS \_ - \_ typanfrastruktur** gültig.</span><span class="sxs-lookup"><span data-stu-id="795ff-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="795ff-122">Wenn der WPA-PSK-Algorithmus aktiviert ist, ordnet die 802,11-Station nur einem Zugriffspunkt zu, dessen Kenn Wort-oder Test Antworten die Authentifizierungs Suite vom Typ 2 (vorinstallierter Schlüssel) innerhalb der WPA-IE enthalten.</span><span class="sxs-lookup"><span data-stu-id="795ff-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ auth \_ algo \_ WPA \_ None**</span><span class="sxs-lookup"><span data-stu-id="795ff-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-124">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795ff-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ auth \_ algo- \_ RSNA**</span><span class="sxs-lookup"><span data-stu-id="795ff-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-126">Gibt einen robusten 802.11 i-RSNA (Security Network Association)-Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="795ff-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="795ff-127">WPA2 ist ein solcher Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="795ff-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="795ff-128">Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant-, Authenticator-und Authentifizierungsserver.</span><span class="sxs-lookup"><span data-stu-id="795ff-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="795ff-129">Verschlüsselungsschlüssel werden dynamisch durch den Authentifizierungsprozess abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="795ff-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="795ff-130">Dieser Algorithmus ist nur für BSS-Typen der **Dot11 \_ BSS \_ - \_ typanfrastruktur** gültig.</span><span class="sxs-lookup"><span data-stu-id="795ff-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="795ff-131">Wenn der RSNA-Algorithmus aktiviert ist, wird die 802,11-Station nur mit einem Zugriffspunkt verknüpft, dessen Leucht-oder Test Antworten die Authentifizierungs Suite vom Typ 1 (802.1 x) in der RSN IE enthalten.</span><span class="sxs-lookup"><span data-stu-id="795ff-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ auth \_ algo- \_ RSNA- \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="795ff-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-133">Gibt einen 802.11 i-RSNA-Algorithmus an, der PSK verwendet.</span><span class="sxs-lookup"><span data-stu-id="795ff-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="795ff-134">Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant und Authentifikator.</span><span class="sxs-lookup"><span data-stu-id="795ff-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="795ff-135">Verschlüsselungsschlüssel werden dynamisch über einen vorinstallierten Schlüssel abgeleitet, der sowohl für den Supplicant als auch für den Authentifikator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795ff-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="795ff-136">Dieser Algorithmus ist nur für BSS-Typen der **Dot11 \_ BSS \_ - \_ typanfrastruktur** gültig.</span><span class="sxs-lookup"><span data-stu-id="795ff-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="795ff-137">Wenn der RSNA-PSK-Algorithmus aktiviert ist, wird die 802,11-Station nur mit einem Zugriffspunkt verknüpft, dessen Leucht Schlag-oder Test Antworten die Authentifizierungs Suite vom Typ 2 (vorinstaltzter Schlüssel) in der RSN IE enthalten.</span><span class="sxs-lookup"><span data-stu-id="795ff-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ auth \_ algo \_ IHV \_ starten**</span><span class="sxs-lookup"><span data-stu-id="795ff-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-139">Gibt den Anfang des Bereichs an, der proprietäre Authentifizierungs Algorithmen angibt, die von einem IHV entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="795ff-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="795ff-140">Der **DOT11 \_ auth \_ algo \_ IHV- \_ Start** Enumerator ist nur gültig, wenn der Mini Port-Treiber im Extensible Station (extsta)-Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="795ff-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="795ff-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ auth \_ algo \_ IHV \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="795ff-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="795ff-142">Gibt das Ende des Bereichs an, der proprietäre Authentifizierungs Algorithmen angibt, die von einem IHV entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="795ff-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="795ff-143">Der **DOT11 \_ auth \_ algo \_ IHV \_ End** -Enumerator ist nur gültig, wenn der Mini Port-Treiber im extsta-Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="795ff-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="795ff-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="795ff-144">Requirements</span></span>



| <span data-ttu-id="795ff-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="795ff-145">Requirement</span></span> | <span data-ttu-id="795ff-146">Wert</span><span class="sxs-lookup"><span data-stu-id="795ff-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="795ff-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="795ff-147">Minimum supported client</span></span><br/> | <span data-ttu-id="795ff-148">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="795ff-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="795ff-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="795ff-149">Minimum supported server</span></span><br/> | <span data-ttu-id="795ff-150">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="795ff-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="795ff-151">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="795ff-151">Redistributable</span></span><br/>          | <span data-ttu-id="795ff-152">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="795ff-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="795ff-153">Header</span><span class="sxs-lookup"><span data-stu-id="795ff-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="795ff-154"><dt>Wlantypes. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="795ff-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795ff-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="795ff-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795ff-156">**DOT11 \_ auth- \_ Chiffre \_ paar**</span><span class="sxs-lookup"><span data-stu-id="795ff-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="795ff-157">**\_verfügbares WLAN- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="795ff-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="795ff-158">**WLAN- \_ Sicherheits \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="795ff-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




