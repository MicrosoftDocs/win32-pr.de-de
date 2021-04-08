---
title: Einfacher Typ von zählype
description: Definiert einen Zähltyp, der verwendet wird, um die Anzahl von Elementen in einem Array anzugeben.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Event Log für den einfachen Typ von "zählype"
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743840"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="8d4f0-104">Einfacher Typ von zählype</span><span class="sxs-lookup"><span data-stu-id="8d4f0-104">CountType Simple Type</span></span>

<span data-ttu-id="8d4f0-105">Definiert einen Zähltyp, der verwendet wird, um die Anzahl von Elementen in einem Array anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8d4f0-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="8d4f0-106">Der Wert kann als xs: unsignedshort-Wert oder als Zeichenfolge angegeben werden, die auf den Namen des Datenelement Knotens verweist, der den unbestimmten Kurzwert enthält.</span><span class="sxs-lookup"><span data-stu-id="8d4f0-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="8d4f0-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d4f0-107">Requirements</span></span>



| <span data-ttu-id="8d4f0-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d4f0-108">Requirement</span></span> | <span data-ttu-id="8d4f0-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8d4f0-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8d4f0-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d4f0-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8d4f0-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d4f0-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8d4f0-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d4f0-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8d4f0-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d4f0-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





