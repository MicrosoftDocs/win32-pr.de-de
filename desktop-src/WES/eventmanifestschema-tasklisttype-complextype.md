---
title: Komplexer tasklisttype-Typ
description: Definiert eine Liste von Aufgaben, die zum Identifizieren der Komponenten einer Anwendung verwendet werden.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Tasklisttype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391486"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="1525d-104">Komplexer tasklisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="1525d-104">TaskListType Complex Type</span></span>

<span data-ttu-id="1525d-105">Definiert eine Liste von Aufgaben, die zum Identifizieren der Komponenten einer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1525d-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1525d-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1525d-106">Child elements</span></span>



| <span data-ttu-id="1525d-107">Element</span><span class="sxs-lookup"><span data-stu-id="1525d-107">Element</span></span>                                                       | <span data-ttu-id="1525d-108">type</span><span class="sxs-lookup"><span data-stu-id="1525d-108">Type</span></span>                                                         | <span data-ttu-id="1525d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1525d-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="1525d-110">**Task**</span><span class="sxs-lookup"><span data-stu-id="1525d-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="1525d-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="1525d-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="1525d-112">Definiert eine Komponente oder eine Unterkomponente einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1525d-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1525d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1525d-113">Requirements</span></span>



| <span data-ttu-id="1525d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1525d-114">Requirement</span></span> | <span data-ttu-id="1525d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1525d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1525d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1525d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1525d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1525d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1525d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1525d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1525d-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1525d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





