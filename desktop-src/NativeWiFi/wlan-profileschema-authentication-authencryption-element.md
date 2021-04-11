---
description: Gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: authentication-Element (authencryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214995"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="2a3ac-103">authentication-Element (authencryption)</span><span class="sxs-lookup"><span data-stu-id="2a3ac-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="2a3ac-104">Das authentication-Element (authencryption) gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="2a3ac-105">Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3ac-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a3ac-106">Remarks</span></span>

<span data-ttu-id="2a3ac-107">In der folgenden Tabelle werden die-Enumerationswerte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="2a3ac-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2a3ac-108">Value</span></span>   | <span data-ttu-id="2a3ac-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a3ac-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="2a3ac-110">open</span><span class="sxs-lookup"><span data-stu-id="2a3ac-110">open</span></span>    | <span data-ttu-id="2a3ac-111">Öffnen Sie 802,11-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="2a3ac-112">Freigegeben</span><span class="sxs-lookup"><span data-stu-id="2a3ac-112">shared</span></span>  | <span data-ttu-id="2a3ac-113">Shared 802,11-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="2a3ac-114">WPA</span><span class="sxs-lookup"><span data-stu-id="2a3ac-114">WPA</span></span>     | <span data-ttu-id="2a3ac-115">WPA-Enterprise 802,11-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="2a3ac-116">WPAPSK</span><span class="sxs-lookup"><span data-stu-id="2a3ac-116">WPAPSK</span></span>  | <span data-ttu-id="2a3ac-117">WPA-Personal 802,11-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="2a3ac-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="2a3ac-118">WPA2</span></span>    | <span data-ttu-id="2a3ac-119">WPA2-Enterprise 802,11-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="2a3ac-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="2a3ac-120">WPA2PSK</span></span> | <span data-ttu-id="2a3ac-121">WPA2-Personal 802,11-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2a3ac-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="2a3ac-122">Weitere Informationen zu 802,11-Authentifizierungsmethoden finden Sie in den Spezifikationen [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)und [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="2a3ac-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="2a3ac-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a3ac-123">Examples</span></span>

<span data-ttu-id="2a3ac-124">Beispiel Profile, die das- **Authentifizierungs** Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2a3ac-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3ac-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a3ac-125">Requirements</span></span>



| <span data-ttu-id="2a3ac-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a3ac-126">Requirement</span></span> | <span data-ttu-id="2a3ac-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2a3ac-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2a3ac-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a3ac-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3ac-129">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a3ac-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2a3ac-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a3ac-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3ac-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a3ac-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="2a3ac-132">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2a3ac-132">Redistributable</span></span><br/>          | <span data-ttu-id="2a3ac-133">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="2a3ac-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2a3ac-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a3ac-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a3ac-135">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="2a3ac-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2a3ac-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="2a3ac-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="2a3ac-137">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="2a3ac-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2a3ac-138">**authencryption (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="2a3ac-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




