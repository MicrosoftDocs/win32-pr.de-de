---
title: Opcode (opcodelisttype)-Element
description: Enthält einen numerischen Wert, der die Aktivität oder einen Punkt innerhalb einer Aktivität identifiziert, der von der Anwendung beim Auslösung des Ereignisses (z. b. Initialisierung oder schließen) durchgeführt wurde.
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- Opcode-Element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106028"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="cea9d-104">Opcode (opcodelisttype)-Element</span><span class="sxs-lookup"><span data-stu-id="cea9d-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="cea9d-105">Enthält einen numerischen Wert, der die Aktivität oder einen Punkt innerhalb einer Aktivität identifiziert, der von der Anwendung beim Auslösung des Ereignisses (z. b. Initialisierung oder schließen) durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="cea9d-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="cea9d-106">Das **Opcode** -Element wird durch den komplexen [**opcodelisttype**](eventmanifestschema-opcodelisttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="cea9d-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea9d-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cea9d-107">Requirements</span></span>



| <span data-ttu-id="cea9d-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cea9d-108">Requirement</span></span> | <span data-ttu-id="cea9d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cea9d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cea9d-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cea9d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="cea9d-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea9d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cea9d-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cea9d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="cea9d-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea9d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cea9d-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cea9d-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="cea9d-115">**Übergeordnete Elemente**</span><span class="sxs-lookup"><span data-stu-id="cea9d-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="cea9d-116">**Opcodes (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="cea9d-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="cea9d-117">**Opcodes (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="cea9d-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="cea9d-118">**Opcodes (metadataType)**</span><span class="sxs-lookup"><span data-stu-id="cea9d-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





