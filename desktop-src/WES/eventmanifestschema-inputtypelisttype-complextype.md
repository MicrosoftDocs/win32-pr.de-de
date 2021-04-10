---
title: Komplexer inputtypelisttype-Typ
description: Definiert eine Liste von Eingabetypen.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Inputtypelisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106035"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="d897a-104">Komplexer inputtypelisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="d897a-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="d897a-105">Definiert eine Liste von Eingabetypen.</span><span class="sxs-lookup"><span data-stu-id="d897a-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d897a-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d897a-106">Child elements</span></span>



| <span data-ttu-id="d897a-107">Element</span><span class="sxs-lookup"><span data-stu-id="d897a-107">Element</span></span>                                                                | <span data-ttu-id="d897a-108">type</span><span class="sxs-lookup"><span data-stu-id="d897a-108">Type</span></span>                                                           | <span data-ttu-id="d897a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d897a-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="d897a-110">**intype**</span><span class="sxs-lookup"><span data-stu-id="d897a-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="d897a-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="d897a-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="d897a-112">Definiert einen Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="d897a-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d897a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d897a-113">Requirements</span></span>



| <span data-ttu-id="d897a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d897a-114">Requirement</span></span> | <span data-ttu-id="d897a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d897a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d897a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d897a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d897a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d897a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d897a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d897a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d897a-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d897a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





