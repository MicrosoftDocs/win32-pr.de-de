---
title: Renderinginfo (EventType)-Element
description: Enthält die gerenderten Meldungs Zeichenfolgen für das Ereignis (einschließlich der Meldungs Zeichenfolge des Ereignisses und der Meldungs Zeichenfolgen für alle Eigenschaften des Ereignisses, z. b. Ebene, Aufgabe und OpCode).
ms.assetid: a0b2a21d-16a0-4c88-9d57-4c99706eeea1
keywords:
- Renderinginfo-Element EventLog
topic_type:
- apiref
api_name:
- RenderingInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 771901196c4988025cce203ffc3134450d38ed7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340297"
---
# <a name="renderinginfo-eventtype-element"></a><span data-ttu-id="fea1f-104">Renderinginfo (EventType)-Element</span><span class="sxs-lookup"><span data-stu-id="fea1f-104">RenderingInfo (EventType) Element</span></span>

<span data-ttu-id="fea1f-105">Enthält die gerenderten Meldungs Zeichenfolgen für das Ereignis (einschließlich der Meldungs Zeichenfolge des Ereignisses und der Meldungs Zeichenfolgen für alle Eigenschaften des Ereignisses, z. b. Ebene, Aufgabe und OpCode).</span><span class="sxs-lookup"><span data-stu-id="fea1f-105">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span>

``` syntax
<xs:element name="RenderingInfo"
    type="RenderingType"
 />
```

<span data-ttu-id="fea1f-106">Das **renderinginfo** -Element wird durch den komplexen [**eventType**](eventschema-eventtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="fea1f-106">The **RenderingInfo** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea1f-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fea1f-107">Requirements</span></span>



| <span data-ttu-id="fea1f-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fea1f-108">Requirement</span></span> | <span data-ttu-id="fea1f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="fea1f-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fea1f-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fea1f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fea1f-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea1f-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fea1f-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fea1f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fea1f-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea1f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fea1f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fea1f-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="fea1f-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="fea1f-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="fea1f-116">**event**</span><span class="sxs-lookup"><span data-stu-id="fea1f-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





