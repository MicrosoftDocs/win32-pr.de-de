---
description: Die spfilenotify- \_ Datei extrahierte Benachrichtigung wird von setupiteratecabinet an eine Rückruf Routine gesendet, um anzugeben, dass eine Datei aus der CAB-Datei extrahiert wurde oder dass eine Extraktion fehlgeschlagen ist und die CAB-Verarbeitung abgebrochen wurde.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: SPFILENOTIFY_FILEEXTRACTED Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363384"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="0d993-103">Spfilenotify \_ fileextrahierte Meldung</span><span class="sxs-lookup"><span data-stu-id="0d993-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="0d993-104">Die **spfilenotify- \_ Datei extrahierte** Benachrichtigung wird von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) an eine Rückruf Routine gesendet, um anzugeben, dass eine Datei aus der CAB-Datei extrahiert wurde oder dass eine Extraktion fehlgeschlagen ist und die CAB-Verarbeitung abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="0d993-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="0d993-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d993-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d993-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="0d993-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0d993-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Pfadinformationen für die extrahierte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="0d993-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="0d993-108">Der **SourceFile** -Member der **FilePath** -Struktur enthält den vollständigen Quellpfad der CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="0d993-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="0d993-109">Der **targetfile** -Member liefert den vollständigen Zielpfad der Datei, die auf dem System installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d993-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d993-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0d993-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0d993-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d993-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d993-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d993-112">Return value</span></span>

<span data-ttu-id="0d993-113">Die CAB-Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0d993-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="0d993-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0d993-114">Return code</span></span>                                                                               | <span data-ttu-id="0d993-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d993-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d993-116"><dt>**kein \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="0d993-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="0d993-117">Es wurde kein Fehler gefunden. setzen Sie die Verarbeitung der CAB-</span><span class="sxs-lookup"><span data-stu-id="0d993-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="0d993-118"><dt>**Fehler \_ xxx**</dt></span><span class="sxs-lookup"><span data-stu-id="0d993-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="0d993-119">Ein Fehler des angegebenen Typs ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0d993-119">An error of the specified type occurred.</span></span> <span data-ttu-id="0d993-120">[**Setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="0d993-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="0d993-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den angegebenen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="0d993-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="0d993-122">Mit der Setup-API wird keine standardmäßige CAB-Rückruf Routine bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0d993-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="0d993-123">Die Setup Anwendung sollte eine Rückruf Routine bereitstellen, um die Benachrichtigungen zu verarbeiten, die von der [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d993-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d993-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d993-124">Requirements</span></span>



| <span data-ttu-id="0d993-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d993-125">Requirement</span></span> | <span data-ttu-id="0d993-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0d993-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d993-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d993-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0d993-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d993-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0d993-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d993-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0d993-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d993-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d993-131">Header</span><span class="sxs-lookup"><span data-stu-id="0d993-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d993-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d993-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d993-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0d993-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d993-134">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0d993-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0d993-135">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0d993-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0d993-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="0d993-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="0d993-137">**Setupiteratecabinet**</span><span class="sxs-lookup"><span data-stu-id="0d993-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

