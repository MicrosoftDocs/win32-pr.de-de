---
title: Guidtype Simple Type (eventmanifest-Schema)
description: Definiert einen Globally Unique Identifier Typ im Registrierungs Format. | Guidtype Simple Type (eventmanifest-Schema)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
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
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373476"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a><span data-ttu-id="bc517-105">Guidtype Simple Type (eventmanifest-Schema)</span><span class="sxs-lookup"><span data-stu-id="bc517-105">GUIDType Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="bc517-106">Definiert einen Globally Unique Identifier Typ im Registrierungs Format.</span><span class="sxs-lookup"><span data-stu-id="bc517-106">Defines a globally unique identifier type, in Registry format.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="bc517-107">Muster</span><span class="sxs-lookup"><span data-stu-id="bc517-107">Patterns</span></span>

<span data-ttu-id="bc517-108">Der einfache **guidtype** -Typ ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="bc517-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="bc517-109">Der Wert muss ein Globally Unique Identifier Typ im Registrierungs Format sein.</span><span class="sxs-lookup"><span data-stu-id="bc517-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="bc517-110">Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="bc517-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="bc517-111">Verwenden Sie GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc517-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc517-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc517-112">Requirements</span></span>



| <span data-ttu-id="bc517-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc517-113">Requirement</span></span> | <span data-ttu-id="bc517-114">Wert</span><span class="sxs-lookup"><span data-stu-id="bc517-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc517-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc517-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bc517-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc517-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc517-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc517-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bc517-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc517-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





