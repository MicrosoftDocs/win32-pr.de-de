---
description: Die spfilenotify \_ endsubqueue-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange alle Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren abschließt.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: SPFILENOTIFY_ENDSUBQUEUE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050518"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="b710b-103">Spfilenotify- \_ endsubqueue-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b710b-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="b710b-104">Die **spfilenotify \_ endsubqueue** -Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange alle Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren abschließt.</span><span class="sxs-lookup"><span data-stu-id="b710b-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b710b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b710b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b710b-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b710b-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b710b-107">Die unter Warteschlange wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b710b-107">Subqueue that has been completed.</span></span> <span data-ttu-id="b710b-108">Dieser Parameter kann einer der folgenden Werte sein: fileOp \_ Delete, fileOp \_ Rename oder fileOp \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="b710b-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="b710b-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b710b-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b710b-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b710b-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b710b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b710b-111">Return value</span></span>

<span data-ttu-id="b710b-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b710b-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b710b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b710b-113">Requirements</span></span>



| <span data-ttu-id="b710b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b710b-114">Requirement</span></span> | <span data-ttu-id="b710b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b710b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b710b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b710b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b710b-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b710b-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b710b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b710b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b710b-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b710b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b710b-120">Header</span><span class="sxs-lookup"><span data-stu-id="b710b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b710b-121"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b710b-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b710b-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b710b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b710b-123">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b710b-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b710b-124">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b710b-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b710b-125">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="b710b-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b710b-126">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="b710b-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




