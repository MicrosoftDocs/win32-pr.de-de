---
description: Die spfilenotify- \_ EndCopy-Benachrichtigung wird an die Rückruffunktion übermittelt, wenn die Warteschlange einen Kopiervorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: SPFILENOTIFY_ENDCOPY Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354028"
---
# <a name="spfilenotify_endcopy-message"></a><span data-ttu-id="b41b3-104">Spfilenotify- \_ endkopier Nachricht</span><span class="sxs-lookup"><span data-stu-id="b41b3-104">SPFILENOTIFY\_ENDCOPY message</span></span>

<span data-ttu-id="b41b3-105">Die **spfilenotify- \_ EndCopy** -Benachrichtigung wird an die Rückruffunktion übermittelt, wenn die Warteschlange einen Kopiervorgang abschließt.</span><span class="sxs-lookup"><span data-stu-id="b41b3-105">The **SPFILENOTIFY\_ENDCOPY** notification is passed to the callback function when the queue completes a copy operation.</span></span> <span data-ttu-id="b41b3-106">Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b41b3-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b41b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b41b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b41b3-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b41b3-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b41b3-109">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b41b3-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="b41b3-110">Der **Win32Error** -Member der **FilePath** -Struktur gibt das Ergebnis des Kopiervorgangs an.</span><span class="sxs-lookup"><span data-stu-id="b41b3-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="b41b3-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b41b3-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b41b3-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41b3-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b41b3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b41b3-113">Return value</span></span>

<span data-ttu-id="b41b3-114">Der Rückgabecode wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b41b3-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b41b3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b41b3-115">Requirements</span></span>



| <span data-ttu-id="b41b3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b41b3-116">Requirement</span></span> | <span data-ttu-id="b41b3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b41b3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b41b3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b41b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b41b3-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b41b3-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b41b3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b41b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b41b3-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b41b3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b41b3-122">Header</span><span class="sxs-lookup"><span data-stu-id="b41b3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b41b3-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b41b3-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b41b3-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b41b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41b3-125">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b41b3-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b41b3-126">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b41b3-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b41b3-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="b41b3-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="b41b3-128">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="b41b3-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b41b3-129">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="b41b3-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




