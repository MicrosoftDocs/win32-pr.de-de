---
title: komplexer principalstype-Typ
description: Definiert das untergeordnete-Element für das Principals-Element.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- komplexer principalstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949515"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="ed79c-104">komplexer principalstype-Typ</span><span class="sxs-lookup"><span data-stu-id="ed79c-104">principalsType Complex Type</span></span>

<span data-ttu-id="ed79c-105">Definiert das untergeordnete-Element für das [**Principals**](taskschedulerschema-principals-tasktype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ed79c-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ed79c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed79c-106">Child elements</span></span>



| <span data-ttu-id="ed79c-107">Element</span><span class="sxs-lookup"><span data-stu-id="ed79c-107">Element</span></span>                                                                  | <span data-ttu-id="ed79c-108">type</span><span class="sxs-lookup"><span data-stu-id="ed79c-108">Type</span></span>                                                                   | <span data-ttu-id="ed79c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed79c-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ed79c-110">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="ed79c-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="ed79c-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="ed79c-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="ed79c-112">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="ed79c-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ed79c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed79c-113">Requirements</span></span>



| <span data-ttu-id="ed79c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed79c-114">Requirement</span></span> | <span data-ttu-id="ed79c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ed79c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed79c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed79c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed79c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed79c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed79c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed79c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed79c-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed79c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





