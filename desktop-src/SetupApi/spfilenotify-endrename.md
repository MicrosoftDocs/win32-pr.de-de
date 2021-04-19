---
description: Die spfilenotify \_ endrename-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Warteschlange einen Umbenennungs Vorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: SPFILENOTIFY_ENDRENAME Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352340"
---
# <a name="spfilenotify_endrename-message"></a><span data-ttu-id="607d7-104">Spfilenotify \_ endrename-Meldung</span><span class="sxs-lookup"><span data-stu-id="607d7-104">SPFILENOTIFY\_ENDRENAME message</span></span>

<span data-ttu-id="607d7-105">Die **spfilenotify \_ endrename** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Warteschlange einen Umbenennungs Vorgang abschließt.</span><span class="sxs-lookup"><span data-stu-id="607d7-105">The **SPFILENOTIFY\_ENDRENAME** notification is sent to the callback routine when the queue completes a rename operation.</span></span> <span data-ttu-id="607d7-106">Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="607d7-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="607d7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="607d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="607d7-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="607d7-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="607d7-109">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="607d7-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="607d7-110">Der **Win32Error** -Member der **FilePath** -Struktur gibt das Ergebnis des Kopiervorgangs an.</span><span class="sxs-lookup"><span data-stu-id="607d7-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="607d7-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="607d7-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="607d7-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="607d7-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="607d7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="607d7-113">Return value</span></span>

<span data-ttu-id="607d7-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="607d7-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="607d7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="607d7-115">Requirements</span></span>



| <span data-ttu-id="607d7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="607d7-116">Requirement</span></span> | <span data-ttu-id="607d7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="607d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="607d7-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="607d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="607d7-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="607d7-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="607d7-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="607d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="607d7-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="607d7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="607d7-122">Header</span><span class="sxs-lookup"><span data-stu-id="607d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="607d7-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="607d7-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607d7-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="607d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607d7-125">Übersicht</span><span class="sxs-lookup"><span data-stu-id="607d7-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="607d7-126">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="607d7-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="607d7-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="607d7-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="607d7-128">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="607d7-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="607d7-129">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="607d7-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




