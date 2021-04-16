---
description: Enthält den Namen eines drahtlosen LAN-Profils.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Name (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527788"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="6d594-103">Name (wlanprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="6d594-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="6d594-104">Das Elementname (wlanprofile) enthält den Namen eines drahtlosen LAN-Profils.</span><span class="sxs-lookup"><span data-stu-id="6d594-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="6d594-105">Das **Name** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="6d594-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d594-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d594-106">Remarks</span></span>

<span data-ttu-id="6d594-107">Bei Namen wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="6d594-107">Names are case-sensitive.</span></span>

<span data-ttu-id="6d594-108">Für Windows XP mit Service Pack 3 (SP3) und Wireless LAN API für Windows XP mit Service Pack 2 (SP2) wird das Name-Element ignoriert, wenn das Profil im Profil Speicher gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="6d594-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="6d594-109">Der Name des Profils wird von der SSID des Netzwerks abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6d594-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="6d594-110">Bei Infrastrukturnetzwerk Profilen ist der Name des Profils die SSID des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="6d594-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="6d594-111">Bei Ad-hoc-Netzwerk Profilen ist der Name des Profils die SSID des Ad-hoc-Netzwerks gefolgt von `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="6d594-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="6d594-112">XML-Escapezeichen, wie z. b. &, werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d594-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="6d594-113">Vermeiden Sie die Verwendung von XML-Escapezeichen in SSID-Namen für Profile, die unter Windows XP mit SP3 oder Wireless LAN API für Windows XP mit SP2 bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="6d594-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="6d594-114">Für alle Netzwerk Profile, die ausschließlich für Windows Vista oder Windows Server 2008 vorgesehen sind, kann der Name eine beliebige Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="6d594-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="6d594-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d594-115">Examples</span></span>

<span data-ttu-id="6d594-116">Beispiel Profile, die das **Name** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6d594-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d594-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d594-117">Requirements</span></span>



| <span data-ttu-id="6d594-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d594-118">Requirement</span></span> | <span data-ttu-id="6d594-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6d594-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6d594-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d594-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6d594-121">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d594-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6d594-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d594-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6d594-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d594-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6d594-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6d594-124">Redistributable</span></span><br/>          | <span data-ttu-id="6d594-125">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="6d594-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6d594-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d594-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d594-127">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="6d594-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6d594-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="6d594-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="6d594-129">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="6d594-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6d594-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="6d594-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




