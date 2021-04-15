---
description: Die spfilenotify \_ startdelete-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Datei Löschvorgang startet.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: SPFILENOTIFY_STARTDELETE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a4a0d362a1c1c3824154fb02e0bb9cf01b24d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529771"
---
# <a name="spfilenotify_startdelete-message"></a><span data-ttu-id="848af-103">Spfilenotify- \_ startdelete-Meldung</span><span class="sxs-lookup"><span data-stu-id="848af-103">SPFILENOTIFY\_STARTDELETE message</span></span>

<span data-ttu-id="848af-104">Die **spfilenotify \_ startdelete** -Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange einen Datei Löschvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="848af-104">The **SPFILENOTIFY\_STARTDELETE** notification is sent to the callback function when the queue starts a file delete operation.</span></span>


```C++
SPFILENOTIFY_STARTDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="848af-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="848af-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="848af-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="848af-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="848af-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="848af-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="848af-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="848af-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="848af-109">Weist immer den Wert fileOp \_ Delete auf.</span><span class="sxs-lookup"><span data-stu-id="848af-109">Always has the value FILEOP\_DELETE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="848af-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="848af-110">Return value</span></span>

<span data-ttu-id="848af-111">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="848af-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="848af-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="848af-112">Return code</span></span>                                                                                  | <span data-ttu-id="848af-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="848af-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="848af-114"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="848af-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="848af-115">Abbrechen des warteschlangencommit.</span><span class="sxs-lookup"><span data-stu-id="848af-115">Abort the queue commit.</span></span> <span data-ttu-id="848af-116">Die Rückruf Routine sollte [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) aufrufen, um den Grund für den Abbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="848af-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for aborting.</span></span> <span data-ttu-id="848af-117">[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **false** zurück, und ein nachfolgendes Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode zurück, der von der Rückruf Routine während des Aufrufs von **SetLastError** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="848af-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="848af-118"><dt>**fileOp- \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="848af-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="848af-119">Führen Sie den Datei Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="848af-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="848af-120"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="848af-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="848af-121">Überspringt den aktuellen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="848af-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="848af-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="848af-122">Requirements</span></span>



| <span data-ttu-id="848af-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="848af-123">Requirement</span></span> | <span data-ttu-id="848af-124">Wert</span><span class="sxs-lookup"><span data-stu-id="848af-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="848af-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="848af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="848af-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="848af-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="848af-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="848af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="848af-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="848af-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="848af-129">Header</span><span class="sxs-lookup"><span data-stu-id="848af-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="848af-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="848af-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="848af-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="848af-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848af-132">Übersicht</span><span class="sxs-lookup"><span data-stu-id="848af-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="848af-133">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="848af-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="848af-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="848af-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="848af-135">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="848af-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="848af-136">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="848af-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

