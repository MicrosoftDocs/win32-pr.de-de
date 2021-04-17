---
title: controlguid (channelpublishingtype)-Element
description: Gibt die Sitzungs-GUID für eine ETW-Sitzung an, die WPP-Ereignisse enthält.
ms.assetid: a9e86468-8a97-4689-a258-85d253debf55
keywords:
- controlguid-Element EventLog
topic_type:
- apiref
api_name:
- controlGuid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92d4f6e1d2985bc983c34552b2e7a973075c9989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391895"
---
# <a name="controlguid-channelpublishingtype-element"></a><span data-ttu-id="a1dbd-104">controlguid (channelpublishingtype)-Element</span><span class="sxs-lookup"><span data-stu-id="a1dbd-104">controlGuid (ChannelPublishingType) Element</span></span>

<span data-ttu-id="a1dbd-105">Gibt die Sitzungs-GUID für eine ETW-Sitzung an, die WPP-Ereignisse enthält.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-105">Identifies the session GUID for an ETW session that contains WPP events.</span></span>

``` syntax
<xs:element name="controlGuid"
    type="GUIDType"
 />
```

<span data-ttu-id="a1dbd-106">Das **controlguid** -Element wird durch den komplexen [**channelpublishingtype**](eventmanifestschema-channelpublishingtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-106">The **controlGuid** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1dbd-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1dbd-107">Requirements</span></span>



| <span data-ttu-id="a1dbd-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1dbd-108">Requirement</span></span> | <span data-ttu-id="a1dbd-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a1dbd-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1dbd-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1dbd-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a1dbd-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1dbd-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1dbd-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1dbd-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a1dbd-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1dbd-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1dbd-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1dbd-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1dbd-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="a1dbd-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a1dbd-116">**Veröffentlichung (channelType)**</span><span class="sxs-lookup"><span data-stu-id="a1dbd-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





