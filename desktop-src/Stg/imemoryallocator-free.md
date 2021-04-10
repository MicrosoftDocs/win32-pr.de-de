---
title: Kostenlose Methode für imemoryzucator
description: Die Free-Methode gibt den von der Zuordnungs Methode belegten Arbeitsspeicher frei.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Strukturierter Speicher für die kostenlose Methode
- Kostenlose strukturierte Speichermethode, imemoryzuordnerschnittstelle
- Strukturierte Speicherung der imemoryzuordcator-Schnittstelle, kostenlose Methode
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040206"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="b2b91-106">Imemoryzuweisung:: Free-Methode</span><span class="sxs-lookup"><span data-stu-id="b2b91-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="b2b91-107">Die **Free** [**-Methode gibt**](imemoryallocator-allocate.md) den von der Zuordnungs Methode belegten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="b2b91-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b91-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2b91-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="b2b91-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2b91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b91-110">*teuren*</span><span class="sxs-lookup"><span data-stu-id="b2b91-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="b2b91-111">Zeiger auf den frei zufügenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b2b91-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b91-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2b91-112">Requirements</span></span>



| <span data-ttu-id="b2b91-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2b91-113">Requirement</span></span> | <span data-ttu-id="b2b91-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b2b91-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b91-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2b91-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b91-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2b91-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b2b91-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2b91-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b91-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2b91-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b2b91-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2b91-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2b91-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2b91-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





