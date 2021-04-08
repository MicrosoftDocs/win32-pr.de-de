---
description: Definiert eine Liste, die bis zu fünf Counter-Attribute enthält.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: komplexer counterAttribute-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959756"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="6cc69-103">komplexer counterAttribute-Typ</span><span class="sxs-lookup"><span data-stu-id="6cc69-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="6cc69-104">Definiert eine Liste, die bis zu fünf Counter-Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="6cc69-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6cc69-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6cc69-105">Child elements</span></span>



| <span data-ttu-id="6cc69-106">Element</span><span class="sxs-lookup"><span data-stu-id="6cc69-106">Element</span></span>              | <span data-ttu-id="6cc69-107">type</span><span class="sxs-lookup"><span data-stu-id="6cc69-107">Type</span></span>                                                                               | <span data-ttu-id="6cc69-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cc69-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc69-109">**Counter Attribute**</span><span class="sxs-lookup"><span data-stu-id="6cc69-109">**counterAttribute**</span></span> | [<span data-ttu-id="6cc69-110">**man: counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="6cc69-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="6cc69-111">Ein Counter-Attribut, das angibt, wie die gegen Daten in einer Consumeranwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc69-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6cc69-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cc69-112">Requirements</span></span>



| <span data-ttu-id="6cc69-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cc69-113">Requirement</span></span> | <span data-ttu-id="6cc69-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6cc69-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6cc69-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cc69-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc69-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cc69-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6cc69-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cc69-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc69-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cc69-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




