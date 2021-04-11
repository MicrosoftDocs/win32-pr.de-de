---
title: Guidtype Simple Type (Ereignis Schema)
description: Definiert einen Globally Unique Identifier Typ im Registrierungs Format. | Guidtype Simple Type (Ereignis Schema)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Guidtype Simple Type EventLog
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07635bc43ff07d65eee5f32786818ca7dad8dd64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352769"
---
# <a name="guidtype-simple-type-event-schema"></a><span data-ttu-id="466fa-105">Guidtype Simple Type (Ereignis Schema)</span><span class="sxs-lookup"><span data-stu-id="466fa-105">GUIDType simple type (Event Schema)</span></span>

<span data-ttu-id="466fa-106">Definiert einen Globally Unique Identifier Typ im Registrierungs Format.</span><span class="sxs-lookup"><span data-stu-id="466fa-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="466fa-107">Muster</span><span class="sxs-lookup"><span data-stu-id="466fa-107">Patterns</span></span>

<span data-ttu-id="466fa-108">Der einfache **guidtype** -Typ ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="466fa-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="466fa-109">Der Wert muss ein Globally Unique Identifier Typ im Registrierungs Format sein.</span><span class="sxs-lookup"><span data-stu-id="466fa-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="466fa-110">Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="466fa-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="466fa-111">Verwenden Sie GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="466fa-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="466fa-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="466fa-112">Requirements</span></span>



| <span data-ttu-id="466fa-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="466fa-113">Requirement</span></span> | <span data-ttu-id="466fa-114">Wert</span><span class="sxs-lookup"><span data-stu-id="466fa-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="466fa-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="466fa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="466fa-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="466fa-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="466fa-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="466fa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="466fa-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="466fa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





