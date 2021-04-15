---
title: E/a-Funktionen für Multimedia-Dateien
description: E/a-Funktionen für Multimedia-Dateien
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Windows-Multimedia, Datei-e/a-Funktionen
- Multimedia, Datei-e/a-Funktionen
- Multimedia-Eingabe, Datei-e/a-Funktionen
- Multimedia-Datei-e/a, Funktionen
- Datei-e/a, Funktionen
- Eingabe und Ausgabe (e/a), Funktionen
- E/a (Eingabe und Ausgabe), Funktionen
- Referenz für Multimedia-Datei-e/a, Funktionen
- Multimedia-Datei-e/a-Referenz, Funktionen
- Datei-e/a-Verweis, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516727"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="2b055-113">E/a-Funktionen für Multimedia-Dateien</span><span class="sxs-lookup"><span data-stu-id="2b055-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="2b055-114">Die folgenden Funktionen werden mit der Multimedia-Datei-e/a verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b055-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="2b055-115">[**Ioproc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b055-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="2b055-116">**mmioadvance**</span><span class="sxs-lookup"><span data-stu-id="2b055-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="2b055-117">**mmioascend**</span><span class="sxs-lookup"><span data-stu-id="2b055-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="2b055-118">**mmioclose**</span><span class="sxs-lookup"><span data-stu-id="2b055-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="2b055-119">**mmiokreatechunk**</span><span class="sxs-lookup"><span data-stu-id="2b055-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="2b055-120">**mmioabstieg**</span><span class="sxs-lookup"><span data-stu-id="2b055-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="2b055-121">**mmioflush**</span><span class="sxs-lookup"><span data-stu-id="2b055-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="2b055-122">**mmiogetinfo**</span><span class="sxs-lookup"><span data-stu-id="2b055-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="2b055-123">**mmioinstallioproc**</span><span class="sxs-lookup"><span data-stu-id="2b055-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="2b055-124">**mmioopen**</span><span class="sxs-lookup"><span data-stu-id="2b055-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="2b055-125">**mmioread**</span><span class="sxs-lookup"><span data-stu-id="2b055-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="2b055-126">**mmiorename**</span><span class="sxs-lookup"><span data-stu-id="2b055-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="2b055-127">**mmioseek**</span><span class="sxs-lookup"><span data-stu-id="2b055-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="2b055-128">**mmiosendmessage**</span><span class="sxs-lookup"><span data-stu-id="2b055-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="2b055-129">**mmiosetbuffer**</span><span class="sxs-lookup"><span data-stu-id="2b055-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="2b055-130">**mmioabtinfo**</span><span class="sxs-lookup"><span data-stu-id="2b055-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="2b055-131">**mmiostringto FourCC**</span><span class="sxs-lookup"><span data-stu-id="2b055-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="2b055-132">**mmiowrite**</span><span class="sxs-lookup"><span data-stu-id="2b055-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="2b055-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b055-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b055-134">Multimedia-Datei-e/a-Referenz</span><span class="sxs-lookup"><span data-stu-id="2b055-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 