---
description: Startet den Abschluss der Aufgabe.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Taskcompletionclient:: applytaskcompletion-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994966"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="65fcb-103">Taskcompletionclient:: applytaskcompletion-Methode</span><span class="sxs-lookup"><span data-stu-id="65fcb-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="65fcb-104">Startet den Abschluss der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="65fcb-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fcb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65fcb-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="65fcb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65fcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65fcb-107">*ptcfcategory*</span><span class="sxs-lookup"><span data-stu-id="65fcb-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="65fcb-108">Ein-Wert, der die Kategorie der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="65fcb-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65fcb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65fcb-109">Return value</span></span>

<span data-ttu-id="65fcb-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="65fcb-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65fcb-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="65fcb-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65fcb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65fcb-112">Remarks</span></span>

<span data-ttu-id="65fcb-113">Der einzige unterstützte Wert für *ptcfcategory* ist 0x08000000.</span><span class="sxs-lookup"><span data-stu-id="65fcb-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="65fcb-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="65fcb-114">Requirements</span></span>



| <span data-ttu-id="65fcb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65fcb-115">Requirement</span></span> | <span data-ttu-id="65fcb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="65fcb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65fcb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65fcb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65fcb-118">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65fcb-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65fcb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65fcb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65fcb-120">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65fcb-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65fcb-121">DLL</span><span class="sxs-lookup"><span data-stu-id="65fcb-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65fcb-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65fcb-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65fcb-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65fcb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fcb-124">**Taskcompletionclient**</span><span class="sxs-lookup"><span data-stu-id="65fcb-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




