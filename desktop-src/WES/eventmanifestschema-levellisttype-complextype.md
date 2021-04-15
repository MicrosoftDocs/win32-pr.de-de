---
title: Komplexer levellist Type-Typ
description: Definiert eine Liste mit Schweregraden, die den ausführlichkeits Grad eines Ereignisses angeben.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- Typ des komplexen levellisttype-Typs EventLog
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479197"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="07a89-104">Komplexer levellist Type-Typ</span><span class="sxs-lookup"><span data-stu-id="07a89-104">LevelListType Complex Type</span></span>

<span data-ttu-id="07a89-105">Definiert eine Liste mit Schweregraden, die den ausführlichkeits Grad eines Ereignisses angeben.</span><span class="sxs-lookup"><span data-stu-id="07a89-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="07a89-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07a89-106">Child elements</span></span>



| <span data-ttu-id="07a89-107">Element</span><span class="sxs-lookup"><span data-stu-id="07a89-107">Element</span></span>                                                          | <span data-ttu-id="07a89-108">type</span><span class="sxs-lookup"><span data-stu-id="07a89-108">Type</span></span>                                                           | <span data-ttu-id="07a89-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a89-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07a89-110">**geringen**</span><span class="sxs-lookup"><span data-stu-id="07a89-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="07a89-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="07a89-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="07a89-112">Definiert einen Schweregrad, der die Ausführlichkeit von Ereignissen während der Protokollierung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="07a89-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="07a89-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07a89-113">Requirements</span></span>



| <span data-ttu-id="07a89-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07a89-114">Requirement</span></span> | <span data-ttu-id="07a89-115">Wert</span><span class="sxs-lookup"><span data-stu-id="07a89-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07a89-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07a89-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07a89-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07a89-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07a89-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07a89-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07a89-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07a89-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





