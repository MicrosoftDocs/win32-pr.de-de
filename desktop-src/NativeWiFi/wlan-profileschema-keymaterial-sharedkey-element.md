---
description: Enthält einen Netzwerkschlüssel oder eine Passphrase.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Keymaterial (sharedkey)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216221"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="c93e0-103">Keymaterial (sharedkey)-Element</span><span class="sxs-lookup"><span data-stu-id="c93e0-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="c93e0-104">Das Keymaterial (sharedkey)-Element enthält einen Netzwerkschlüssel oder eine Passphrase.</span><span class="sxs-lookup"><span data-stu-id="c93e0-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="c93e0-105">Wenn das [**geschützte**](wlan-profileschema-protected-sharedkey-element.md) Element den Wert true aufweist, wird dieses Schlüsselmaterial verschlüsselt. Andernfalls ist das Schlüsselmaterial unverschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c93e0-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="c93e0-106">Verschlüsseltes Schlüsselmaterial wird in hexadezimaler Form ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c93e0-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="c93e0-107">Das-Element wird durch das [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="c93e0-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93e0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c93e0-108">Remarks</span></span>

<span data-ttu-id="c93e0-109">Der Bereich gültiger Werte für das Keymaterial-Element variiert je nach Art der Authentifizierung und Verschlüsselung, die von den [**Authentifizierungs**](wlan-profileschema-authentication-authencryption-element.md) -und [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Elementen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c93e0-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="c93e0-110">Sie variiert auch je nach [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).</span><span class="sxs-lookup"><span data-stu-id="c93e0-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="c93e0-111">In der folgenden Tabelle sind gültige **keymaterialwerte** für einige Authentifizierungs-und Verschlüsselungs Paare aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c93e0-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="c93e0-112">[**Authentifizierungs**](wlan-profileschema-authentication-authencryption-element.md) Wert</span><span class="sxs-lookup"><span data-stu-id="c93e0-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="c93e0-113">[**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Wert</span><span class="sxs-lookup"><span data-stu-id="c93e0-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="c93e0-114">[**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) -Wert</span><span class="sxs-lookup"><span data-stu-id="c93e0-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="c93e0-115">Gültige **keymaterialwerte**</span><span class="sxs-lookup"><span data-stu-id="c93e0-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93e0-116">Open oder Shared</span><span class="sxs-lookup"><span data-stu-id="c93e0-116">open or shared</span></span>                                                                           | <span data-ttu-id="c93e0-117">WEP</span><span class="sxs-lookup"><span data-stu-id="c93e0-117">WEP</span></span>                                                                              | <span data-ttu-id="c93e0-118">Network Key</span><span class="sxs-lookup"><span data-stu-id="c93e0-118">networkKey</span></span>                                                            | <span data-ttu-id="c93e0-119">Dieses Element enthält einen WEP-Schlüssel mit 5 oder 13 ANSI-Zeichen oder 10 oder 26 hexadezimal Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c93e0-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="c93e0-120">WPAPSK oder WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="c93e0-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="c93e0-121">TKIP oder AES</span><span class="sxs-lookup"><span data-stu-id="c93e0-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="c93e0-122">passPhrase</span><span class="sxs-lookup"><span data-stu-id="c93e0-122">passPhrase</span></span>                                                            | <span data-ttu-id="c93e0-123">Dieses Element enthält eine Passphrase von 8 bis 63 ASCII-Zeichen, d. h. 8 bis 63 ANSI-Zeichen im Bereich zwischen 32 und 126.</span><span class="sxs-lookup"><span data-stu-id="c93e0-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="c93e0-124">Schlüsselwerte müssen den in 802.11 i angegebenen Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c93e0-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="c93e0-125">WPAPSK oder WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="c93e0-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="c93e0-126">TKIP oder AES</span><span class="sxs-lookup"><span data-stu-id="c93e0-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="c93e0-127">Network Key</span><span class="sxs-lookup"><span data-stu-id="c93e0-127">networkKey</span></span>                                                            | <span data-ttu-id="c93e0-128">Dieses Element enthält einen Schlüssel mit 64 hexadezimalen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c93e0-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="c93e0-129">Unicode-Zeichen können eingegeben werden, wenn oben ANSI-oder ASCII-Zeichen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c93e0-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="c93e0-130">Wenn die angegebenen Unicode-Zeichen jedoch nicht ANSI-oder ASCII-Zeichen zugeordnet werden können, wird das angegebene Schlüsselmaterial abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="c93e0-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="c93e0-131">Das von [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) zurückgegebene Schlüsselmaterial ist immer verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c93e0-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="c93e0-132">Wenn nicht verschlüsseltes Schlüsselmaterial an [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)übermittelt wird, wird das Schlüsselmaterial auch automatisch verschlüsselt, bevor es im Profil Speicher gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c93e0-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="c93e0-133">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Das Schlüsselmaterial wird nie verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c93e0-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="c93e0-134">Wenn Ihr Prozess im Kontext des Kontos "LocalSystem" ausgeführt wird, können Sie das Schlüsselmaterial durch den Aufruf von [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c93e0-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="c93e0-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c93e0-135">Examples</span></span>

<span data-ttu-id="c93e0-136">Beispiel Profile, die das **Keymaterial** -Element verwenden, finden Sie unter Beispiel für [nicht-Broadcast profile](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md)und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c93e0-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c93e0-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c93e0-137">Requirements</span></span>



| <span data-ttu-id="c93e0-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c93e0-138">Requirement</span></span> | <span data-ttu-id="c93e0-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c93e0-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c93e0-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c93e0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c93e0-141">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c93e0-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c93e0-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c93e0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c93e0-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c93e0-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="c93e0-144">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c93e0-144">Redistributable</span></span><br/>          | <span data-ttu-id="c93e0-145">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="c93e0-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c93e0-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c93e0-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="c93e0-147">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="c93e0-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c93e0-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="c93e0-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="c93e0-149">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="c93e0-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c93e0-150">**sharedkey (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="c93e0-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
