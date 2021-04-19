---
description: Die spfilenotifitifimedia- \_ Benachrichtigung wird an die Rückruf Routine gesendet, wenn neue Medien oder eine neue CAB-Datei erforderlich sind.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: SPFILENOTIFY_NEEDMEDIA Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361761"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="0a0d0-103">Spfilenotify- \_ needmedia-Meldung</span><span class="sxs-lookup"><span data-stu-id="0a0d0-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="0a0d0-104">Die **spfilenotifitifimedia \_** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn neue Medien oder eine neue CAB-Datei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="0a0d0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a0d0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a0d0-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="0a0d0-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0a0d0-107">Zeiger auf eine [**Quell \_ Medien**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) Struktur.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a0d0-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0a0d0-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0a0d0-109">Zeiger auf ein Zeichen Array zum Speichern neuer Pfadinformationen, die vom Benutzer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="0a0d0-110">Die Puffergröße ist ein **TCHAR** -Array mit maximalen \_ Pfad Elementen.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="0a0d0-111">Die von der Setup Anwendung zurückgegebenen Pfadinformationen sollten diese Größe nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a0d0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a0d0-112">Return value</span></span>

<span data-ttu-id="0a0d0-113">Die Rückruf Routine sollte eine der folgenden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="0a0d0-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0a0d0-114">Return code</span></span>                                                                                    | <span data-ttu-id="0a0d0-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a0d0-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a0d0-116"><dt>**fileOp \_ NewPath**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0d0-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="0a0d0-117">Die Medien sind vorhanden, und die angeforderte Datei ist in dem Pfad verfügbar, der in dem Puffer angegeben ist, auf den *Param2* zeigt.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="0a0d0-118"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0d0-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="0a0d0-119">Überspringen der angeforderten Datei</span><span class="sxs-lookup"><span data-stu-id="0a0d0-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="0a0d0-120"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0d0-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="0a0d0-121">Verarbeitung der Warteschlange abbrechen.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-121">Abort queue processing.</span></span> <span data-ttu-id="0a0d0-122">Die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion gibt **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="0a0d0-123">GetLastError gibt erweiterte Fehlerinformationen zurück, z. b. einen Fehler, \_ Wenn der Benutzer abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="0a0d0-124"><dt>**fileOp-doit**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0d0-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="0a0d0-125">Das Medium ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a0d0-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="0a0d0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a0d0-126">Requirements</span></span>



| <span data-ttu-id="0a0d0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a0d0-127">Requirement</span></span> | <span data-ttu-id="0a0d0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0a0d0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0d0-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a0d0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0a0d0-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a0d0-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0a0d0-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a0d0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0a0d0-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a0d0-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a0d0-133">Header</span><span class="sxs-lookup"><span data-stu-id="0a0d0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a0d0-134"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a0d0-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a0d0-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a0d0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0d0-136">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0a0d0-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0a0d0-137">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0a0d0-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0a0d0-138">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="0a0d0-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="0a0d0-139">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="0a0d0-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="0a0d0-140">**Quell \_ Medien**</span><span class="sxs-lookup"><span data-stu-id="0a0d0-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




