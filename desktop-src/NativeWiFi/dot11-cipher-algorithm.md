---
description: Definiert einen Verschlüsselungsalgorithmus für die Verschlüsselung und Entschlüsselung von Daten.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: DOT11_CIPHER_ALGORITHM-Enumeration (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349297"
---
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="be19f-103">DOT11 \_ Chiffre \_ Algorithmus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="be19f-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="be19f-104">Der Enumerationstyp **DOT11 \_ Verschlüsselungs \_ Algorithmus** definiert einen Verschlüsselungsalgorithmus für die Verschlüsselung und Entschlüsselung von Daten.</span><span class="sxs-lookup"><span data-stu-id="be19f-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="be19f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be19f-105">Syntax</span></span>


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="be19f-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="be19f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="be19f-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ Cipher \_ algo \_ None**</span><span class="sxs-lookup"><span data-stu-id="be19f-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-108">Gibt an, dass kein Verschlüsselungsalgorithmus aktiviert oder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="be19f-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ Cipher \_ algo \_ WEP40**</span><span class="sxs-lookup"><span data-stu-id="be19f-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-110">Gibt einen drahtlosen WEP-Algorithmus (Wired Equivalent Privacy) an, bei dem es sich um den RC4-basierten Algorithmus handelt, der im 802.11-1999-Standard angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="be19f-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="be19f-111">Dieser Enumerator gibt den WEP-Verschlüsselungsalgorithmus mit einem 40-Bit-Chiffre Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="be19f-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ Cipher \_ algo \_ TKIP**</span><span class="sxs-lookup"><span data-stu-id="be19f-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-113">Gibt einen TKIP-Algorithmus (Temporal Key Integrity Protocol) an, bei dem es sich um die RC4-basierte Verschlüsselungs Sammlung handelt, die auf den in der WPA-Spezifikation definierten Algorithmen und dem IEEE 802.11 i-2004-Standard basiert.</span><span class="sxs-lookup"><span data-stu-id="be19f-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="be19f-114">Diese Chiffre verwendet auch den "Michael Message Integrity Code (MIC)"-Algorithmus für den Fälschungsschutz.</span><span class="sxs-lookup"><span data-stu-id="be19f-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ Cipher \_ algo \_ CCMP**</span><span class="sxs-lookup"><span data-stu-id="be19f-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-116">Gibt einen AES-CCMP-Algorithmus an, wie im IEEE 802.11 i-2004-Standard und in RFC 3610 angegeben.</span><span class="sxs-lookup"><span data-stu-id="be19f-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="be19f-117">Advanced Encryption Standard (AES) ist der Verschlüsselungsalgorithmus, der in der "fps pub 197" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="be19f-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ Cipher \_ algo \_ WEP104**</span><span class="sxs-lookup"><span data-stu-id="be19f-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-119">Gibt einen WEP-Verschlüsselungsalgorithmus mit einem 104-Bit-Chiffre Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="be19f-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ Cipher \_ algo \_ WPA \_ - \_ Gruppe verwenden**</span><span class="sxs-lookup"><span data-stu-id="be19f-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-121">Gibt einen Wi-Fi geschützten Zugriff (WPA) Gruppenschlüssel Verschlüsselungs Sammlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="be19f-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="be19f-122">Weitere Informationen zur Verwendung von Group Key Verschlüsselungs Suite finden Sie Unterklausel 7.3.2.25.1 of the IEEE 802.11 i-2004 Standard.</span><span class="sxs-lookup"><span data-stu-id="be19f-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ Cipher \_ algo- \_ RSN- \_ Verwendungs \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="be19f-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-124">Gibt ein stabiles Sicherheitsnetzwerk (RSN) mit Gruppenschlüssel Verschlüsselungs Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="be19f-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="be19f-125">Weitere Informationen zur Verwendung von Group Key Verschlüsselungs Suite finden Sie Unterklausel 7.3.2.25.1 of the IEEE 802.11 i-2004 Standard.</span><span class="sxs-lookup"><span data-stu-id="be19f-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ Cipher \_ algo \_ WEP**</span><span class="sxs-lookup"><span data-stu-id="be19f-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-127">Gibt einen WEP-Chiffre Algorithmus mit einem Verschlüsselungsschlüssel beliebiger Länge an.</span><span class="sxs-lookup"><span data-stu-id="be19f-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="be19f-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ Cipher \_ algo \_ IHV \_ starten**</span><span class="sxs-lookup"><span data-stu-id="be19f-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-129">Gibt den Anfang des Bereichs an, der verwendet wird, um proprietäre Verschlüsselungsalgorithmen zu definieren, die von einem unabhängigen Hardwarehersteller (IHV) entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="be19f-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="be19f-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ Cipher \_ algo \_ IHV \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="be19f-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="be19f-131">Gibt das Ende des Bereichs an, der verwendet wird, um proprietäre Verschlüsselungsalgorithmen zu definieren, die von einem IHV entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="be19f-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be19f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be19f-132">Requirements</span></span>



| <span data-ttu-id="be19f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be19f-133">Requirement</span></span> | <span data-ttu-id="be19f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="be19f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be19f-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be19f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="be19f-136">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be19f-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="be19f-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be19f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="be19f-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be19f-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="be19f-139">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="be19f-139">Redistributable</span></span><br/>          | <span data-ttu-id="be19f-140">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="be19f-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="be19f-141">Header</span><span class="sxs-lookup"><span data-stu-id="be19f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="be19f-142"><dt>Wlantypes. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be19f-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be19f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be19f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be19f-144">**DOT11 \_ auth- \_ Chiffre \_ paar**</span><span class="sxs-lookup"><span data-stu-id="be19f-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="be19f-145">**\_verfügbares WLAN- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="be19f-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="be19f-146">**WLAN- \_ Sicherheits \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="be19f-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




