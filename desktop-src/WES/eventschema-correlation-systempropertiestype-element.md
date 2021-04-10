---
title: Korrelations Element (systempropertiestype)
description: Die Aktivitäts Bezeichner, mit denen Consumer verwandte Ereignisse gruppieren können.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Korrelations Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956917"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="913d5-104">Korrelations Element (systempropertiestype)</span><span class="sxs-lookup"><span data-stu-id="913d5-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="913d5-105">Die Aktivitäts Bezeichner, mit denen Consumer verwandte Ereignisse gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="913d5-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="913d5-106">Das **Korrelations** Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="913d5-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="913d5-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="913d5-107">Attributes</span></span>



| <span data-ttu-id="913d5-108">Name</span><span class="sxs-lookup"><span data-stu-id="913d5-108">Name</span></span>              | <span data-ttu-id="913d5-109">type</span><span class="sxs-lookup"><span data-stu-id="913d5-109">Type</span></span>                                                | <span data-ttu-id="913d5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="913d5-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913d5-111">Aktivitäts-ID</span><span class="sxs-lookup"><span data-stu-id="913d5-111">ActivityID</span></span>        | [<span data-ttu-id="913d5-112">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="913d5-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="913d5-113">Ein-Globally Unique Identifier, der die aktuelle Aktivität bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="913d5-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="913d5-114">Die mit diesem Bezeichner veröffentlichten Ereignisse sind Teil derselben Aktivität.</span><span class="sxs-lookup"><span data-stu-id="913d5-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="913d5-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="913d5-115">RelatedActivityID</span></span> | [<span data-ttu-id="913d5-116">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="913d5-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="913d5-117">Ein-Globally Unique Identifier, der die Aktivität identifiziert, an die das Steuerelement übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="913d5-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="913d5-118">Die zugehörigen Ereignisse haben dann diesen Bezeichner als ActivityId-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="913d5-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="913d5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="913d5-119">Requirements</span></span>



| <span data-ttu-id="913d5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="913d5-120">Requirement</span></span> | <span data-ttu-id="913d5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="913d5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="913d5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="913d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="913d5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="913d5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="913d5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="913d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="913d5-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="913d5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="913d5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="913d5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="913d5-127">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="913d5-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="913d5-128">**System (EventType)**</span><span class="sxs-lookup"><span data-stu-id="913d5-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





