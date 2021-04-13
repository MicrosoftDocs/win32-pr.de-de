---
title: Tasknamedvaluecollection. Create-Methode
description: Erstellt bei der Skripterstellung ein Name-Wert-Paar in der Auflistung.
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- Create-Methode Taskplaner
- Create Method-Taskplaner, tasknamedvaluecollection-Objekt
- Tasknamedvaluecollection-Objekt Taskplaner, Create-Methode
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3926142b25cbb2d65efaa45d6b767ce2e56ba86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478393"
---
# <a name="tasknamedvaluecollectioncreate-method"></a><span data-ttu-id="d2ea0-106">Tasknamedvaluecollection. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="d2ea0-106">TaskNamedValueCollection.Create method</span></span>

<span data-ttu-id="d2ea0-107">Erstellt bei der Skripterstellung ein Name-Wert-Paar in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d2ea0-107">For scripting, creates a name-value pair in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ea0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2ea0-108">Syntax</span></span>


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a><span data-ttu-id="d2ea0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2ea0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ea0-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ea0-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea0-111">Der Name, der mit einem Wert in einem Name-Wert-Paar verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d2ea0-111">The name that is associated with a value in a name-value pair.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea0-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ea0-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea0-113">Der Wert, der einem Namen in einem Name-Wert-Paar zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d2ea0-113">The value that is associated with a name in a name-value pair.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea0-114">*paar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d2ea0-114">*pair* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea0-115">Das Name-Wert-Paar, das in der-Auflistung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ea0-115">The name-value pair that is created in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ea0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2ea0-116">Return value</span></span>

<span data-ttu-id="d2ea0-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2ea0-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ea0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2ea0-118">Requirements</span></span>



| <span data-ttu-id="d2ea0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2ea0-119">Requirement</span></span> | <span data-ttu-id="d2ea0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d2ea0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ea0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2ea0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ea0-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2ea0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2ea0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2ea0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ea0-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2ea0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2ea0-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d2ea0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2ea0-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea0-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2ea0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ea0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ea0-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea0-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





