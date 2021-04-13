---
title: clocktype (channelpublishingtype)-Element
description: Die zu verwendende Takt Auflösung, wenn der Zeitstempel für jedes Ereignis protokolliert wird.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- clocktype-Element EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391597"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="cdcfc-104">clocktype (channelpublishingtype)-Element</span><span class="sxs-lookup"><span data-stu-id="cdcfc-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="cdcfc-105">Die zu verwendende Takt Auflösung, wenn der Zeitstempel für jedes Ereignis protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="cdcfc-106">Das Element " **clocktype** " wird vom komplexen Typ " [**channelpublishingtype**](eventmanifestschema-channelpublishingtype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcfc-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdcfc-107">Requirements</span></span>



| <span data-ttu-id="cdcfc-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdcfc-108">Requirement</span></span> | <span data-ttu-id="cdcfc-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cdcfc-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cdcfc-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdcfc-110">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcfc-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdcfc-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdcfc-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdcfc-112">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcfc-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdcfc-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cdcfc-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdcfc-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="cdcfc-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="cdcfc-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="cdcfc-116">**Veröffentlichung (channelType)**</span><span class="sxs-lookup"><span data-stu-id="cdcfc-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





