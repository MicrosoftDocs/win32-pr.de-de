---
description: Gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: usemsonex (IHV)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959974"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="b8369-103">usemsonex (IHV)-Element</span><span class="sxs-lookup"><span data-stu-id="b8369-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="b8369-104">Das **usemsonex** (IHV)-Element gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8369-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="b8369-105">Wenn **usemsonex** auf true festgelegt ist, verwenden die IHV-Sicherheitskomponenten von Microsoft definierte 802.1 x-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b8369-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="b8369-106">Wenn **usemsonex** den Wert false hat, verwenden IHV-Sicherheitskomponenten vom Hersteller bereitgestellte 802.1 x-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b8369-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="b8369-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8369-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="b8369-108">Das-Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="b8369-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8369-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8369-109">Requirements</span></span>



| <span data-ttu-id="b8369-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8369-110">Requirement</span></span> | <span data-ttu-id="b8369-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b8369-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8369-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8369-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b8369-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8369-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8369-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8369-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b8369-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8369-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8369-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8369-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8369-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="b8369-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b8369-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="b8369-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="b8369-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="b8369-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b8369-120">**IHV (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b8369-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




