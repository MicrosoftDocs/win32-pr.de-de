---
description: Gibt an, ob ein gemeinsam verwendeter Schlüssel verschlüsselt ist.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: geschütztes-Element (sharedkey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344059"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="48c81-103">geschütztes-Element (sharedkey)</span><span class="sxs-lookup"><span data-stu-id="48c81-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="48c81-104">Das geschützte (sharedkey)-Element gibt an, ob ein gemeinsam verwendeter Schlüssel verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="48c81-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="48c81-105">Das-Element wird durch das [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="48c81-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="48c81-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48c81-106">Remarks</span></span>

<span data-ttu-id="48c81-107">Für Windows Vista und Windows Server 2008 hat **Protected** immer den Wert true, wenn das Profil aus dem Profil Speicher abgerufen wurde (z. b. durch Aufrufen von [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span><span class="sxs-lookup"><span data-stu-id="48c81-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="48c81-108">Für Profile, die für die Verwendung unter Windows XP mit Service Pack 3 (SP3) oder der Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) vorgesehen sind, muss **Protected** den Wert false aufweisen.</span><span class="sxs-lookup"><span data-stu-id="48c81-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="48c81-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48c81-109">Examples</span></span>

<span data-ttu-id="48c81-110">Beispiel Profile, die das **geschützte** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="48c81-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48c81-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48c81-111">Requirements</span></span>



| <span data-ttu-id="48c81-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48c81-112">Requirement</span></span> | <span data-ttu-id="48c81-113">Wert</span><span class="sxs-lookup"><span data-stu-id="48c81-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="48c81-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48c81-114">Minimum supported client</span></span><br/> | <span data-ttu-id="48c81-115">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48c81-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48c81-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48c81-116">Minimum supported server</span></span><br/> | <span data-ttu-id="48c81-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48c81-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="48c81-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="48c81-118">Redistributable</span></span><br/>          | <span data-ttu-id="48c81-119">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="48c81-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="48c81-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48c81-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="48c81-121">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="48c81-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="48c81-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="48c81-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="48c81-123">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="48c81-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="48c81-124">**sharedkey (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="48c81-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




