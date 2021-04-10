---
description: Die keysvc- \_ Typenumeration definiert, ob ein Schlüssel für einen Computer oder einen Dienst gilt.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: KEYSVC_TYPE-Enumeration (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960904"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="6dc80-103">Keysvc- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="6dc80-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="6dc80-104">Die **keysvc- \_ Typenumeration** definiert, ob ein Schlüssel für einen Computer oder einen Dienst gilt.</span><span class="sxs-lookup"><span data-stu-id="6dc80-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dc80-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6dc80-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6dc80-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6dc80-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**Keysvcmachine**</span><span class="sxs-lookup"><span data-stu-id="6dc80-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="6dc80-108">Der Schlüssel ist für einen Computer.</span><span class="sxs-lookup"><span data-stu-id="6dc80-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="6dc80-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**Keysvcservice**</span><span class="sxs-lookup"><span data-stu-id="6dc80-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="6dc80-110">Der Schlüssel ist für einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="6dc80-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dc80-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dc80-111">Requirements</span></span>



| <span data-ttu-id="6dc80-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dc80-112">Requirement</span></span> | <span data-ttu-id="6dc80-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6dc80-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc80-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6dc80-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc80-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6dc80-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6dc80-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6dc80-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc80-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6dc80-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6dc80-118">Header</span><span class="sxs-lookup"><span data-stu-id="6dc80-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dc80-119"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc80-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc80-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dc80-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc80-121">**Rkeyopenkeyservice**</span><span class="sxs-lookup"><span data-stu-id="6dc80-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




