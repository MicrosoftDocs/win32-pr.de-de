---
title: Count. GetValue-Methode
description: Ruft den letzten Wert des Zählers ab.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- GetValue-Methode (Sysmon)
- GetValue-Methode "sysmon", "count"-Klasse
- "\"Sysmon\"-Klasse der \"count Value\"-Klasse"
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342466"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="5af6e-106">Count. GetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="5af6e-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="5af6e-107">Ruft den letzten Wert des Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="5af6e-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af6e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af6e-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="5af6e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af6e-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5af6e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5af6e-111">Der zuletzt erfasste Wert des Zählers.</span><span class="sxs-lookup"><span data-stu-id="5af6e-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5af6e-112">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5af6e-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5af6e-113">Gibt an, ob der Wert gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5af6e-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="5af6e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="5af6e-114">Value</span></span>                                                                                              | <span data-ttu-id="5af6e-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5af6e-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="5af6e-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5af6e-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5af6e-117">Der Wert ist gültig.</span><span class="sxs-lookup"><span data-stu-id="5af6e-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="5af6e-118"><dt>0xc0000bba (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="5af6e-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="5af6e-119">Der Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5af6e-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af6e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5af6e-120">Return value</span></span>

<span data-ttu-id="5af6e-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5af6e-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af6e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5af6e-122">Remarks</span></span>

<span data-ttu-id="5af6e-123">Wenn die Quelle der Leistungsdaten aus einer Protokolldatei ist, ist der Wert der letzte Leistungswert in der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="5af6e-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af6e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5af6e-124">Requirements</span></span>



| <span data-ttu-id="5af6e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5af6e-125">Requirement</span></span> | <span data-ttu-id="5af6e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5af6e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5af6e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5af6e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5af6e-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5af6e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5af6e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5af6e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5af6e-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5af6e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5af6e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5af6e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af6e-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5af6e-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af6e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5af6e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af6e-134">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="5af6e-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="5af6e-135">**"Count. getstatistics"**</span><span class="sxs-lookup"><span data-stu-id="5af6e-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="5af6e-136">**"Count. Value"**</span><span class="sxs-lookup"><span data-stu-id="5af6e-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





