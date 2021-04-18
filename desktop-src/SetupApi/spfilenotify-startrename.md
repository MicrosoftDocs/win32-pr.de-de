---
description: Die spfilenotify \_ startrename-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Vorgang zum Umbenennen von Dateien startet.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: SPFILENOTIFY_STARTRENAME Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c17d0c70b49ba00b3b16956e7ede5eda43b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351422"
---
# <a name="spfilenotify_startrename-message"></a><span data-ttu-id="f83a3-103">Spfilenotify- \_ startrename-Meldung</span><span class="sxs-lookup"><span data-stu-id="f83a3-103">SPFILENOTIFY\_STARTRENAME message</span></span>

<span data-ttu-id="f83a3-104">Die **spfilenotify \_ startrename** -Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Vorgang zum Umbenennen von Dateien startet.</span><span class="sxs-lookup"><span data-stu-id="f83a3-104">The **SPFILENOTIFY\_STARTRENAME** notification is sent to the callback function when the queue starts a file rename operation.</span></span>


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="f83a3-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f83a3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f83a3-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="f83a3-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f83a3-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f83a3-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f83a3-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f83a3-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f83a3-109">Hat immer den Wert fileOp \_ Rename.</span><span class="sxs-lookup"><span data-stu-id="f83a3-109">Always has the value FILEOP\_RENAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f83a3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f83a3-110">Return value</span></span>

<span data-ttu-id="f83a3-111">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f83a3-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="f83a3-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f83a3-112">Return code</span></span>                                                                                  | <span data-ttu-id="f83a3-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f83a3-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f83a3-114"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="f83a3-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="f83a3-115">Abbrechen des warteschlangencommit.</span><span class="sxs-lookup"><span data-stu-id="f83a3-115">Abort the queue commit.</span></span> <span data-ttu-id="f83a3-116">Die Rückruf Routine sollte [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) aufrufen, um den Grund für die Beendigung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f83a3-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="f83a3-117">[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **false** zurück, und ein nachfolgendes Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode zurück, der von der Rückruf Routine während des Aufrufs von **SetLastError** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f83a3-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="f83a3-118"><dt>**fileOp- \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="f83a3-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="f83a3-119">Führen Sie den Datei Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="f83a3-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f83a3-120"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="f83a3-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="f83a3-121">Überspringt den aktuellen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="f83a3-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="f83a3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f83a3-122">Requirements</span></span>



| <span data-ttu-id="f83a3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f83a3-123">Requirement</span></span> | <span data-ttu-id="f83a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f83a3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f83a3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f83a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f83a3-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f83a3-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f83a3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f83a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f83a3-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f83a3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f83a3-129">Header</span><span class="sxs-lookup"><span data-stu-id="f83a3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f83a3-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f83a3-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f83a3-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f83a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83a3-132">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f83a3-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f83a3-133">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f83a3-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f83a3-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="f83a3-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="f83a3-135">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="f83a3-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="f83a3-136">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="f83a3-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

