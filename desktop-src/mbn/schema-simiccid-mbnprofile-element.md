---
description: Identifiziert die SIM-Identifikationsnummer für GSM-Geräte.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Simiccid (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345053"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="272a2-103">Simiccid (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="272a2-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="272a2-104">Das **simiccid (mbnprofile)-** Element identifiziert die SIM-Identifikationsnummer für GSM-Geräte.</span><span class="sxs-lookup"><span data-stu-id="272a2-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="272a2-105">Dieses Element ist optional und wird vom mobilen Breitbanddienst zur internen Verwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="272a2-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="272a2-106">Eine Anwendung sollte dieses Feld beim Erstellen oder Aktualisieren eines Profils nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="272a2-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="272a2-107">Das **simiccid-** Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="272a2-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="272a2-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="272a2-108">Requirements</span></span>



| <span data-ttu-id="272a2-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="272a2-109">Requirement</span></span> | <span data-ttu-id="272a2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="272a2-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="272a2-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="272a2-111">Minimum supported client</span></span><br/> | <span data-ttu-id="272a2-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="272a2-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="272a2-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="272a2-113">Minimum supported server</span></span><br/> | <span data-ttu-id="272a2-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="272a2-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="272a2-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="272a2-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="272a2-116">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="272a2-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="272a2-117">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="272a2-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="272a2-118">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="272a2-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="272a2-119">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="272a2-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




