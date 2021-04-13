---
description: Die spfilenotify- \_ renameerror-Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Umbenennungs Vorgangs ein Fehler auftritt.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: SPFILENOTIFY_RENAMEERROR Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347248"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="f339f-103">Spfilenotify \_ renameerror-Meldung</span><span class="sxs-lookup"><span data-stu-id="f339f-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="f339f-104">Die **spfilenotify- \_ renameerror** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Umbenennungs Vorgangs ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="f339f-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="f339f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f339f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f339f-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="f339f-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f339f-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f339f-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="f339f-108">Der **Win32Error** -Member der **FilePath** -Struktur gibt den Fehler an, der beim Umbenennungs Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f339f-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="f339f-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f339f-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f339f-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f339f-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f339f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f339f-111">Return value</span></span>

<span data-ttu-id="f339f-112">Die Rückruf Routine sollte eine der folgenden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f339f-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="f339f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f339f-113">Return code</span></span>                                                                                  | <span data-ttu-id="f339f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f339f-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f339f-115"><dt>**fileOp- \_ Wiederholung**</dt></span><span class="sxs-lookup"><span data-stu-id="f339f-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="f339f-116">Der Benutzer hat versucht, den Umbenennungs Vorgang erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f339f-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="f339f-117"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="f339f-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="f339f-118">Der Benutzer hat den Vorgang zum Umbenennen von Dateien übersprungen.</span><span class="sxs-lookup"><span data-stu-id="f339f-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="f339f-119"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="f339f-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="f339f-120">Stoppt den warteschlangencommit.</span><span class="sxs-lookup"><span data-stu-id="f339f-120">Stop the queue commit.</span></span> <span data-ttu-id="f339f-121">[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="f339f-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="f339f-122">" [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt erweiterte Fehlerinformationen zurück, z \_ . b \_ \_ \_ . "Fehler abgebrochen" (wenn der Benutzer abgebrochen wurde) oder "Fehler"</span><span class="sxs-lookup"><span data-stu-id="f339f-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f339f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f339f-123">Requirements</span></span>



| <span data-ttu-id="f339f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f339f-124">Requirement</span></span> | <span data-ttu-id="f339f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f339f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f339f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f339f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f339f-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f339f-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f339f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f339f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f339f-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f339f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f339f-130">Header</span><span class="sxs-lookup"><span data-stu-id="f339f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f339f-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f339f-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f339f-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f339f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f339f-133">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f339f-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f339f-134">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f339f-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f339f-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="f339f-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="f339f-136">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="f339f-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="f339f-137">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="f339f-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

