---
title: Komplexer maptype-Typ
description: Definiert eine Liste von Name-Wert-Paaren.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- "\"Maptype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740392"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="ddd08-104">Komplexer maptype-Typ</span><span class="sxs-lookup"><span data-stu-id="ddd08-104">MapType Complex Type</span></span>

<span data-ttu-id="ddd08-105">Definiert eine Liste von Name-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="ddd08-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ddd08-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddd08-106">Child elements</span></span>



| <span data-ttu-id="ddd08-107">Element</span><span class="sxs-lookup"><span data-stu-id="ddd08-107">Element</span></span>                                                          | <span data-ttu-id="ddd08-108">type</span><span class="sxs-lookup"><span data-stu-id="ddd08-108">Type</span></span>                                                                 | <span data-ttu-id="ddd08-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddd08-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddd08-110">**bitMap**</span><span class="sxs-lookup"><span data-stu-id="ddd08-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="ddd08-111">**Bitmaptype**</span><span class="sxs-lookup"><span data-stu-id="ddd08-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="ddd08-112">Definiert eine Liste von Name-Wert-Paaren, die Bitwerte und Zeichen folgen Werte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ddd08-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="ddd08-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="ddd08-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="ddd08-114">**Valuemaptype**</span><span class="sxs-lookup"><span data-stu-id="ddd08-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="ddd08-115">Definiert eine Liste von Name-Wert-Paaren, die ganzzahlige Werte und Zeichen folgen Werte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ddd08-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ddd08-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddd08-116">Remarks</span></span>

<span data-ttu-id="ddd08-117">In der Regel erstellen Sie Zuordnungen, um aufgelistete Zeichen folgen Werte für Ereignisdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ddd08-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="ddd08-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddd08-118">Examples</span></span>

<span data-ttu-id="ddd08-119">Im folgenden Beispiel wird gezeigt, wie eine Werte Zuordnung und eine Bitmap angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ddd08-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="ddd08-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddd08-120">Requirements</span></span>



| <span data-ttu-id="ddd08-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddd08-121">Requirement</span></span> | <span data-ttu-id="ddd08-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ddd08-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ddd08-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddd08-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd08-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddd08-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ddd08-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddd08-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd08-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddd08-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





