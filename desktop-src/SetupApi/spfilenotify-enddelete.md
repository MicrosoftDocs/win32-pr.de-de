---
description: Die spfilenotify- \_ endlösch Benachrichtigung wird an die Rückruf Routine zurückgegeben, wenn eine Warteschlange einen Löschvorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: SPFILENOTIFY_ENDDELETE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350135"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="bf685-104">Spfilenotify- \_ endlösch Nachricht</span><span class="sxs-lookup"><span data-stu-id="bf685-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="bf685-105">Die **spfilenotify- \_ endlösch** Benachrichtigung wird an die Rückruf Routine zurückgegeben, wenn eine Warteschlange einen Löschvorgang abschließt.</span><span class="sxs-lookup"><span data-stu-id="bf685-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="bf685-106">Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="bf685-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="bf685-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf685-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf685-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="bf685-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="bf685-109">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bf685-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="bf685-110">Der **Win32Error** -Member der **FilePath** -Struktur gibt das Ergebnis eines Kopiervorgangs an.</span><span class="sxs-lookup"><span data-stu-id="bf685-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf685-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="bf685-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="bf685-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf685-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf685-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf685-113">Return value</span></span>

<span data-ttu-id="bf685-114">Der Rückgabecode wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bf685-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf685-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf685-115">Requirements</span></span>



| <span data-ttu-id="bf685-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf685-116">Requirement</span></span> | <span data-ttu-id="bf685-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bf685-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf685-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf685-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf685-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf685-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf685-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf685-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf685-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf685-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf685-122">Header</span><span class="sxs-lookup"><span data-stu-id="bf685-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf685-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf685-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf685-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bf685-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf685-125">Übersicht</span><span class="sxs-lookup"><span data-stu-id="bf685-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="bf685-126">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bf685-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="bf685-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="bf685-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="bf685-128">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="bf685-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="bf685-129">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="bf685-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




