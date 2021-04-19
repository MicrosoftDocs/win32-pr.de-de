---
description: Die spfilenotify- \_ Start Kopier Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Datei Kopiervorgang startet.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: SPFILENOTIFY_STARTCOPY Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368950"
---
# <a name="spfilenotify_startcopy-message"></a><span data-ttu-id="7939d-103">Spfilenotify- \_ StartCopy-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7939d-103">SPFILENOTIFY\_STARTCOPY message</span></span>

<span data-ttu-id="7939d-104">Die **spfilenotify- \_ Start Kopier** Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Datei Kopiervorgang startet.</span><span class="sxs-lookup"><span data-stu-id="7939d-104">The **SPFILENOTIFY\_STARTCOPY** notification is sent to the callback function when the queue starts a file copy operation.</span></span>


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="7939d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7939d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7939d-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="7939d-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="7939d-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7939d-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7939d-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="7939d-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="7939d-109">Hat immer den Wert fileOp \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="7939d-109">Always has the value FILEOP\_COPY.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7939d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7939d-110">Return value</span></span>

<span data-ttu-id="7939d-111">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7939d-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="7939d-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7939d-112">Return code</span></span>                                                                                  | <span data-ttu-id="7939d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7939d-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7939d-114"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="7939d-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="7939d-115">Brechen Sie den warteschlangencommit-Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="7939d-115">Abort the queue commit process.</span></span> <span data-ttu-id="7939d-116">Die Rückruf Routine sollte [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) aufrufen, um den Grund für die Beendigung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7939d-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="7939d-117">Die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion gibt **false** zurück, und ein nachfolgende Aufrufs von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode zurück, der von der Rückruf Routine während des Aufrufs von **SetLastError** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7939d-117">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="7939d-118"><dt>**fileOp- \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="7939d-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="7939d-119">Führen Sie den Datei Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="7939d-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7939d-120"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="7939d-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="7939d-121">Überspringt den aktuellen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="7939d-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="7939d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7939d-122">Requirements</span></span>



| <span data-ttu-id="7939d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7939d-123">Requirement</span></span> | <span data-ttu-id="7939d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7939d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7939d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7939d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7939d-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7939d-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7939d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7939d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7939d-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7939d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7939d-129">Header</span><span class="sxs-lookup"><span data-stu-id="7939d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7939d-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7939d-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7939d-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7939d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7939d-132">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7939d-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="7939d-133">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7939d-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="7939d-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="7939d-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="7939d-135">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="7939d-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="7939d-136">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="7939d-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

