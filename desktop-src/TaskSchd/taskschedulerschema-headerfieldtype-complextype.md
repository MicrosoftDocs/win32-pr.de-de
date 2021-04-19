---
title: komplexer headerfieldtype-Typ
description: Definiert die Elemente, die zum Erstellen eines Header Felds in einer e-Mail-Nachricht verwendet werden.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- komplexer headerfieldtype-Typ Taskplaner
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342198"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="c5ac2-104">komplexer headerfieldtype-Typ</span><span class="sxs-lookup"><span data-stu-id="c5ac2-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="c5ac2-105">Definiert die Elemente, die zum Erstellen eines Header Felds in einer e-Mail-Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c5ac2-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5ac2-106">Child elements</span></span>



| <span data-ttu-id="c5ac2-107">Element</span><span class="sxs-lookup"><span data-stu-id="c5ac2-107">Element</span></span>                                                            | <span data-ttu-id="c5ac2-108">type</span><span class="sxs-lookup"><span data-stu-id="c5ac2-108">Type</span></span>                                                                    | <span data-ttu-id="c5ac2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5ac2-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c5ac2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="c5ac2-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="c5ac2-112">Gibt den Namen des Header Felds in einer e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="c5ac2-113">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="c5ac2-114">**string**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-114">**string**</span></span>                                                              | <span data-ttu-id="c5ac2-115">Gibt den Wert eines Header Felds in einer e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="c5ac2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5ac2-116">Requirements</span></span>



| <span data-ttu-id="c5ac2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5ac2-117">Requirement</span></span> | <span data-ttu-id="c5ac2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c5ac2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5ac2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5ac2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ac2-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5ac2-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5ac2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5ac2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ac2-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5ac2-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





