---
title: komplexer attachmentstype-Typ
description: Definiert die Elemente, mit denen eine mit einer e-Mail-Nachricht gesendete Anlage angegeben wird.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- komplexer attachmentstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344488"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="6e13c-104">komplexer attachmentstype-Typ</span><span class="sxs-lookup"><span data-stu-id="6e13c-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="6e13c-105">Definiert die Elemente, mit denen eine mit einer e-Mail-Nachricht gesendete Anlage angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e13c-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6e13c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e13c-106">Child elements</span></span>



| <span data-ttu-id="6e13c-107">Element</span><span class="sxs-lookup"><span data-stu-id="6e13c-107">Element</span></span>                                                          | <span data-ttu-id="6e13c-108">type</span><span class="sxs-lookup"><span data-stu-id="6e13c-108">Type</span></span>                                                                    | <span data-ttu-id="6e13c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e13c-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e13c-110">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6e13c-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="6e13c-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="6e13c-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="6e13c-112">Gibt den Pfad zu einer Datei an, die als Anlage in einer e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e13c-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6e13c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e13c-113">Requirements</span></span>



| <span data-ttu-id="6e13c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e13c-114">Requirement</span></span> | <span data-ttu-id="6e13c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6e13c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e13c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e13c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e13c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e13c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e13c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e13c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e13c-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e13c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





