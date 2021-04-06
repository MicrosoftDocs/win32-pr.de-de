---
title: komplexer namedValues-Typ
description: Definiert ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- komplexer namedValues-Typ Taskplaner
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742161"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="a1641-104">komplexer namedValues-Typ</span><span class="sxs-lookup"><span data-stu-id="a1641-104">namedValues Complex Type</span></span>

<span data-ttu-id="a1641-105">Definiert ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1641-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a1641-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1641-106">Child elements</span></span>



| <span data-ttu-id="a1641-107">Element</span><span class="sxs-lookup"><span data-stu-id="a1641-107">Element</span></span>                                                        | <span data-ttu-id="a1641-108">type</span><span class="sxs-lookup"><span data-stu-id="a1641-108">Type</span></span>                                                | <span data-ttu-id="a1641-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1641-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1641-110">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a1641-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="a1641-111">**NamedValue**</span><span class="sxs-lookup"><span data-stu-id="a1641-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="a1641-112">Gibt den Wert an, der einem Namen in einem Name-Wert-Paar zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1641-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a1641-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1641-113">Requirements</span></span>



| <span data-ttu-id="a1641-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1641-114">Requirement</span></span> | <span data-ttu-id="a1641-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a1641-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1641-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1641-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1641-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1641-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1641-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1641-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1641-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1641-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





