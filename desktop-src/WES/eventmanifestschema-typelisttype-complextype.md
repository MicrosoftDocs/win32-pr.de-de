---
title: Komplexer typelisttype-Typ
description: Definiert die Typen, die im Manifest verwendet werden.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Typelisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344695"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="36d5e-104">Komplexer typelisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="36d5e-104">TypeListType Complex Type</span></span>

<span data-ttu-id="36d5e-105">Definiert die Typen, die im Manifest verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36d5e-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="36d5e-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36d5e-106">Child elements</span></span>



| <span data-ttu-id="36d5e-107">Element</span><span class="sxs-lookup"><span data-stu-id="36d5e-107">Element</span></span>                                                               | <span data-ttu-id="36d5e-108">type</span><span class="sxs-lookup"><span data-stu-id="36d5e-108">Type</span></span>                                                                           | <span data-ttu-id="36d5e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36d5e-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36d5e-110">**Intypes**</span><span class="sxs-lookup"><span data-stu-id="36d5e-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="36d5e-111">**Inputtypelisttype**</span><span class="sxs-lookup"><span data-stu-id="36d5e-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="36d5e-112">Definiert eine Liste von Eingabe Datentypen.</span><span class="sxs-lookup"><span data-stu-id="36d5e-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="36d5e-113">**xmltypes**</span><span class="sxs-lookup"><span data-stu-id="36d5e-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="36d5e-114">**Xmltypelisttype**</span><span class="sxs-lookup"><span data-stu-id="36d5e-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="36d5e-115">Definiert einen Listen Ausgabetyp, den der Dienst verwendet, um zu bestimmen, wie ein Eingabe Datentyp dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="36d5e-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="36d5e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36d5e-116">Requirements</span></span>



| <span data-ttu-id="36d5e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36d5e-117">Requirement</span></span> | <span data-ttu-id="36d5e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="36d5e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36d5e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36d5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36d5e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36d5e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36d5e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36d5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36d5e-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36d5e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





