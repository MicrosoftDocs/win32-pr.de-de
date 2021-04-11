---
title: Binary (eventdatatype)-Element
description: Ein binäres Daten-BLOB für Ereignisse, die mithilfe der Ereignisprotokollierung geschrieben werden.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Ereignisprotokoll für das binäre Element
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040118"
---
# <a name="binary-eventdatatype-element"></a><span data-ttu-id="94766-104">Binary (eventdatatype)-Element</span><span class="sxs-lookup"><span data-stu-id="94766-104">Binary (EventDataType) Element</span></span>

<span data-ttu-id="94766-105">Ein binäres Daten-BLOB für Ereignisse, die mithilfe der [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging)geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="94766-105">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

<span data-ttu-id="94766-106">Das **Binary** -Element wird durch den komplexen [**eventdatatype**](eventschema-eventdatatype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="94766-106">The **Binary** element is defined by the [**EventDataType**](eventschema-eventdatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="94766-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94766-107">Requirements</span></span>



| <span data-ttu-id="94766-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94766-108">Requirement</span></span> | <span data-ttu-id="94766-109">Wert</span><span class="sxs-lookup"><span data-stu-id="94766-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94766-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94766-110">Minimum supported client</span></span><br/> | <span data-ttu-id="94766-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94766-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94766-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94766-112">Minimum supported server</span></span><br/> | <span data-ttu-id="94766-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94766-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94766-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94766-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="94766-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="94766-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="94766-116">**EVENTDATA (EventType)**</span><span class="sxs-lookup"><span data-stu-id="94766-116">**EventData (EventType)**</span></span>](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

