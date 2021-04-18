---
description: Identifiziert den eindeutigen Bezeichner des Profils.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Abonniert-Element (mbnprofile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526618"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="7fdc3-103">Abonniert-Element (mbnprofile)</span><span class="sxs-lookup"><span data-stu-id="7fdc3-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="7fdc3-104">Das **abonniert-Element (mbnprofile)** identifiziert den eindeutigen Bezeichner des Profils.</span><span class="sxs-lookup"><span data-stu-id="7fdc3-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="7fdc3-105">Bei einem GSM-Netzwerk sollte dies die IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte enthalten, die den minimalen (mobilen Identifikationsnummer) des Geräts enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7fdc3-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="7fdc3-106">Das-Element ist eine numerische Zeichenfolge mit einer maximalen Länge von 15 Ziffern.</span><span class="sxs-lookup"><span data-stu-id="7fdc3-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="7fdc3-107">Das-Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7fdc3-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="7fdc3-108">Das **abonniert** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="7fdc3-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fdc3-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fdc3-109">Requirements</span></span>



| <span data-ttu-id="7fdc3-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fdc3-110">Requirement</span></span> | <span data-ttu-id="7fdc3-111">Wert</span><span class="sxs-lookup"><span data-stu-id="7fdc3-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7fdc3-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fdc3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7fdc3-113">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7fdc3-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7fdc3-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fdc3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7fdc3-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fdc3-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="7fdc3-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fdc3-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="7fdc3-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="7fdc3-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7fdc3-118">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="7fdc3-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="7fdc3-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="7fdc3-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7fdc3-120">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="7fdc3-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




