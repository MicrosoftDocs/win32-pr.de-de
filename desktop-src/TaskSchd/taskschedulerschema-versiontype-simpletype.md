---
title: versiontype simple-Typ
description: Definiert ein Muster, das eine Version eines Tasks angibt.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- versiontype Simple Type Taskplaner
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340487"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="5896a-104">versiontype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="5896a-104">versionType Simple Type</span></span>

<span data-ttu-id="5896a-105">Definiert ein Muster, das eine Version eines Tasks angibt.</span><span class="sxs-lookup"><span data-stu-id="5896a-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="5896a-106">Muster</span><span class="sxs-lookup"><span data-stu-id="5896a-106">Patterns</span></span>

<span data-ttu-id="5896a-107">Der einfache **versiontype** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="5896a-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="5896a-108">Ein Double, auf das ein, zwei oder drei Doubles folgt.</span><span class="sxs-lookup"><span data-stu-id="5896a-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="5896a-109">Beispielsweise 1,2 oder 1.2.3.</span><span class="sxs-lookup"><span data-stu-id="5896a-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="5896a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5896a-110">Requirements</span></span>



| <span data-ttu-id="5896a-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5896a-111">Requirement</span></span> | <span data-ttu-id="5896a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5896a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5896a-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5896a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5896a-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5896a-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5896a-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5896a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5896a-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5896a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





