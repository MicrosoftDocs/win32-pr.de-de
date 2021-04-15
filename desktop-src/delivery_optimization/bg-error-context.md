---
title: BG_ERROR_CONTEXT-Enumeration (deliveryoptimization. h)
description: Die BG_ERROR_CONTEXT-Enumeration definiert die Konstanten Werte, die den Kontext angeben, in dem der Fehler aufgetreten ist.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- BG_ERROR_CONTEXT-Enumeration
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476176"
---
# <a name="bg_error_context-enumeration"></a><span data-ttu-id="bfcf2-104">BG_ERROR_CONTEXT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="bfcf2-104">BG_ERROR_CONTEXT enumeration</span></span>

<span data-ttu-id="bfcf2-105">Die **BG_ERROR_CONTEXT** -Enumeration definiert die Konstanten Werte, die den Kontext angeben, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-105">The **BG_ERROR_CONTEXT** enumeration defines the constant values that specify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcf2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfcf2-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="bfcf2-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bfcf2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bfcf2-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-109">Es ist kein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-109">An error has not occurred.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-111">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-111">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-113">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-115">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-117">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-119">Der Fehler ist mit der angegebenen Remote Datei verknüpft.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-119">The error was related to the specified remote file.</span></span> <span data-ttu-id="bfcf2-120">Beispielsweise konnte nicht auf die URL zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-120">For example, the URL was not accessible.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-122">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf2-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf2-124">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-124">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfcf2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfcf2-125">Requirements</span></span>



| <span data-ttu-id="bfcf2-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfcf2-126">Requirement</span></span> | <span data-ttu-id="bfcf2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bfcf2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcf2-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfcf2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcf2-129">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfcf2-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bfcf2-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfcf2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcf2-131">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfcf2-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bfcf2-132">Header</span><span class="sxs-lookup"><span data-stu-id="bfcf2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfcf2-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcf2-133"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcf2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfcf2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcf2-135">**Ibackgroundcopyerror:: getError**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-135">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





