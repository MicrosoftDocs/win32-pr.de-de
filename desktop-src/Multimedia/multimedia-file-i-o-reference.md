---
title: Multimedia-Datei-e/a-Referenz
description: Multimedia-Datei-e/a-Referenz
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows Multimedia, Datei-e/a-Referenz
- Multimedia, Datei-e/a-Referenz
- Multimedia-Eingabe, Datei-e/a-Referenz
- Multimedia-Datei-e/a, Referenz
- Datei-e/a, Referenz
- Eingabe und Ausgabe (e/a), Referenz
- E/a (Eingabe und Ausgabe), Referenz
- Referenz für Multimedia-Datei-e/a, Informationen zu
- Multimedia-Datei-e/a-Referenz, Informationen zu
- Datei-e/a-Referenz, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724817"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="56077-113">Multimedia-Datei-e/a-Referenz</span><span class="sxs-lookup"><span data-stu-id="56077-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="56077-114">In diesem Abschnitt werden die Funktionen, Makros, Meldungen und Strukturen beschrieben, die mit der Multimedia-Dateieingabe und-Ausgabe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="56077-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="56077-115">Diese Elemente werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="56077-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="56077-116">Grundlegende e/a</span><span class="sxs-lookup"><span data-stu-id="56077-116">Basic I/O</span></span>

-   [<span data-ttu-id="56077-117">**mmioclose**</span><span class="sxs-lookup"><span data-stu-id="56077-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="56077-118">**mmioopen**</span><span class="sxs-lookup"><span data-stu-id="56077-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="56077-119">**mmioread**</span><span class="sxs-lookup"><span data-stu-id="56077-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="56077-120">**mmiorename**</span><span class="sxs-lookup"><span data-stu-id="56077-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="56077-121">**mmioseek**</span><span class="sxs-lookup"><span data-stu-id="56077-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="56077-122">**mmiowrite**</span><span class="sxs-lookup"><span data-stu-id="56077-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="56077-123">Gepufferte e/a</span><span class="sxs-lookup"><span data-stu-id="56077-123">Buffered I/O</span></span>

-   [<span data-ttu-id="56077-124">**mmioadvance**</span><span class="sxs-lookup"><span data-stu-id="56077-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="56077-125">**mmioflush**</span><span class="sxs-lookup"><span data-stu-id="56077-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="56077-126">**mmiogetinfo**</span><span class="sxs-lookup"><span data-stu-id="56077-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="56077-127">[**Mmioinfo**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56077-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="56077-128">**mmiosetbuffer**</span><span class="sxs-lookup"><span data-stu-id="56077-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="56077-129">**mmioabtinfo**</span><span class="sxs-lookup"><span data-stu-id="56077-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="56077-130">Riff-e/a</span><span class="sxs-lookup"><span data-stu-id="56077-130">RIFF I/O</span></span>

-   [<span data-ttu-id="56077-131">**mmioascend**</span><span class="sxs-lookup"><span data-stu-id="56077-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="56077-132">**Mmckinfo**</span><span class="sxs-lookup"><span data-stu-id="56077-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="56077-133">**mmiokreatechunk**</span><span class="sxs-lookup"><span data-stu-id="56077-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="56077-134">**mmioabstieg**</span><span class="sxs-lookup"><span data-stu-id="56077-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="56077-135">**mmiofourcc**</span><span class="sxs-lookup"><span data-stu-id="56077-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="56077-136">**mmiostringto FourCC**</span><span class="sxs-lookup"><span data-stu-id="56077-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="56077-137">Angepasste e/a-Prozeduren</span><span class="sxs-lookup"><span data-stu-id="56077-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="56077-138">[**Ioproc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56077-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="56077-139">**mmioinstallioproc**</span><span class="sxs-lookup"><span data-stu-id="56077-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="56077-140">**mmiom \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="56077-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="56077-141">**mmiom \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="56077-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="56077-142">**mmiom- \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="56077-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="56077-143">**Umbenennen von mmiom \_**</span><span class="sxs-lookup"><span data-stu-id="56077-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="56077-144">**mmiom- \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="56077-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="56077-145">**mmiom- \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="56077-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="56077-146">**mmiom- \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="56077-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="56077-147">**mmiosendmessage**</span><span class="sxs-lookup"><span data-stu-id="56077-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="56077-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56077-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56077-149">Multimedia-Datei-e/a</span><span class="sxs-lookup"><span data-stu-id="56077-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 