---
description: Gibt an, ob eine Verbindung mit einem verborgenen Netzwerk hergestellt werden soll.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Nonbroadcast-Element (ssidconfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355557"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="5abf5-103">Nonbroadcast-Element (ssidconfig)</span><span class="sxs-lookup"><span data-stu-id="5abf5-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="5abf5-104">Das Nonbroadcast (ssidconfig)-Element gibt an, ob eine Verbindung mit einem verborgenen Netzwerk hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5abf5-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="5abf5-105">Wenn ein Netzwerk seine SSID nicht überträgt, wird es als ausgeblendetes Netzwerk bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5abf5-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="5abf5-106">Wenn mehrere SSIDs innerhalb des Profils festgelegt sind, müssen alle den gleichen nicht Broadcast Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5abf5-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="5abf5-107">Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf **ESS** festgelegt ist, kann dieser Wert entweder "true" oder "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="5abf5-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="5abf5-108">Wenn dieses Element nicht vorhanden ist, ist der Standardwert "false".</span><span class="sxs-lookup"><span data-stu-id="5abf5-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="5abf5-109">Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf **IBSS** festgelegt ist, muss dieser Wert "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="5abf5-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="5abf5-110">Wenn dieses Element nicht vorhanden ist, ist der Standardwert "false".</span><span class="sxs-lookup"><span data-stu-id="5abf5-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="5abf5-111">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5abf5-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="5abf5-112">Das-Element wird durch das [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="5abf5-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="5abf5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5abf5-113">Examples</span></span>

<span data-ttu-id="5abf5-114">Ein Beispiel Profil, das das **Nonbroadcast** -Element verwendet, finden Sie unter [Beispiel für nicht-Broadcast profile](non-broadcast-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5abf5-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5abf5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5abf5-115">Requirements</span></span>



| <span data-ttu-id="5abf5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5abf5-116">Requirement</span></span> | <span data-ttu-id="5abf5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5abf5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5abf5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5abf5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5abf5-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5abf5-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5abf5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5abf5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5abf5-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5abf5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5abf5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5abf5-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="5abf5-123">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="5abf5-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5abf5-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="5abf5-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="5abf5-125">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="5abf5-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5abf5-126">**Ssidconfig (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="5abf5-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




