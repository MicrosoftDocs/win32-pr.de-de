---
title: komplexer NamedValue-Typ
description: Definiert einen Namen, der mit einem Wert in einem Name-Wert-Paar verknüpft ist.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- komplexer NamedValue-Typ Taskplaner
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956764"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="cd21f-104">komplexer NamedValue-Typ</span><span class="sxs-lookup"><span data-stu-id="cd21f-104">namedValue Complex Type</span></span>

<span data-ttu-id="cd21f-105">Definiert einen Namen, der mit einem Wert in einem Name-Wert-Paar verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="cd21f-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="cd21f-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd21f-106">Attributes</span></span>



| <span data-ttu-id="cd21f-107">Name</span><span class="sxs-lookup"><span data-stu-id="cd21f-107">Name</span></span> | <span data-ttu-id="cd21f-108">type</span><span class="sxs-lookup"><span data-stu-id="cd21f-108">Type</span></span>                                                                    | <span data-ttu-id="cd21f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd21f-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd21f-110">name</span><span class="sxs-lookup"><span data-stu-id="cd21f-110">name</span></span> | [<span data-ttu-id="cd21f-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="cd21f-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="cd21f-112">Gibt den Namen an, der mit einem Wert in einem Name-Wert-Paar verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="cd21f-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cd21f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd21f-113">Requirements</span></span>



| <span data-ttu-id="cd21f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd21f-114">Requirement</span></span> | <span data-ttu-id="cd21f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cd21f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd21f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd21f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cd21f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd21f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd21f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd21f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cd21f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd21f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





