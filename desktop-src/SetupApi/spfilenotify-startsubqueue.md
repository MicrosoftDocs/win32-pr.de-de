---
description: Die spfilenotify- \_ Benachrichtigung startsubqueue wird an die Rückruffunktion gesendet, wenn die Warteschlange mit der Verarbeitung der Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren beginnt.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: SPFILENOTIFY_STARTSUBQUEUE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355392"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="54f81-103">Spfilenotify- \_ startsubqueue-Nachricht</span><span class="sxs-lookup"><span data-stu-id="54f81-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="54f81-104">Die **spfilenotify-Benachrichtigung \_ startsubqueue** wird an die Rückruffunktion gesendet, wenn die Warteschlange mit der Verarbeitung der Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren beginnt.</span><span class="sxs-lookup"><span data-stu-id="54f81-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="54f81-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="54f81-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f81-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="54f81-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="54f81-107">Unter Warteschlange, die gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="54f81-107">Subqueue that has been started.</span></span> <span data-ttu-id="54f81-108">Dieser Parameter kann einer der Werte fileOp \_ Delete, fileOp \_ Rename oder fileOp \_ Copy sein.</span><span class="sxs-lookup"><span data-stu-id="54f81-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="54f81-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="54f81-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="54f81-110">Anzahl der Datei Kopier-, Umbenennungs-oder Löschvorgänge in der unter Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="54f81-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f81-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54f81-111">Return value</span></span>

<span data-ttu-id="54f81-112">Wenn ein Fehler auftritt, sollte die Rückruf Routine [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)aufrufen und den Fehler angeben und dann 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="54f81-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="54f81-113">Die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion gibt " **false** " zurück, und ein nachfolgendes Aufrufen von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt den von der Rückruf Routine festgelegten Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="54f81-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="54f81-114">Wenn kein Fehler auftritt, sollte die Rückruf Routine einen Wert ungleich 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="54f81-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f81-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54f81-115">Requirements</span></span>



| <span data-ttu-id="54f81-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54f81-116">Requirement</span></span> | <span data-ttu-id="54f81-117">Wert</span><span class="sxs-lookup"><span data-stu-id="54f81-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54f81-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54f81-118">Minimum supported client</span></span><br/> | <span data-ttu-id="54f81-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54f81-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54f81-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54f81-120">Minimum supported server</span></span><br/> | <span data-ttu-id="54f81-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54f81-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54f81-122">Header</span><span class="sxs-lookup"><span data-stu-id="54f81-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="54f81-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f81-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f81-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="54f81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f81-125">Übersicht</span><span class="sxs-lookup"><span data-stu-id="54f81-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="54f81-126">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="54f81-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="54f81-127">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="54f81-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="54f81-128">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="54f81-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

