---
title: Ausführen von Speicherdatei-e/a
description: Ausführen von Speicherdatei-e/a
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- Multimedia-Datei-e/a, Arbeitsspeicher
- Datei-e/a, Arbeitsspeicher
- Eingabe und Ausgabe (e/a), Arbeitsspeicher
- E/a (Eingabe und Ausgabe), Arbeitsspeicher
- Arbeitsspeicher-e/a
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472749"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="188c0-109">Ausführen von Speicherdatei-e/a</span><span class="sxs-lookup"><span data-stu-id="188c0-109">Performing Memory File I/O</span></span>

<span data-ttu-id="188c0-110">Die Multimedia-Datei-e/a-Dienste ermöglichen es Ihnen, einen Speicherblock als Datei zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="188c0-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="188c0-111">Dies kann hilfreich sein, wenn Sie bereits über ein Datei Image im Arbeitsspeicher verfügen.</span><span class="sxs-lookup"><span data-stu-id="188c0-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="188c0-112">Mithilfe von Speicherdateien können Sie die Anzahl von Sonderbedingungen im Code reduzieren, da Sie für e/a-Zwecke Speicherdateien als Datenträger basierte Dateien behandeln können.</span><span class="sxs-lookup"><span data-stu-id="188c0-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="188c0-113">Sie können auch Speicherdateien mit der Zwischenablage verwenden.</span><span class="sxs-lookup"><span data-stu-id="188c0-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="188c0-114">Wie bei e/a-Puffern können Speicherdateien den von der Anwendung oder dem Datei-e/a-Manager zugeordneten Arbeitsspeicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="188c0-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="188c0-115">Außerdem können Speicherdateien entweder erweiterbar oder nicht erweiterbar sein.</span><span class="sxs-lookup"><span data-stu-id="188c0-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="188c0-116">Wenn der Datei-e/a-Manager das Ende einer erweiterbaren Speicherdatei erreicht, erweitert er die Speicherdatei um ein vordefiniertes Inkrement.</span><span class="sxs-lookup"><span data-stu-id="188c0-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="188c0-117">Um eine Speicherdatei zu öffnen, verwenden Sie die [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion, wobei der *szFilename* -Parameter auf **null** festgelegt ist und das MMIO- \_ Schreib Flag im *dwOpenFlags* -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="188c0-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="188c0-118">Legen Sie den *lpmmioinfo* -Parameter so fest, dass er auf eine [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur verweist, die wie folgt eingerichtet wurde:</span><span class="sxs-lookup"><span data-stu-id="188c0-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="188c0-119">Legen Sie den **pioproc** -Member auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="188c0-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="188c0-120">Legen Sie den **fccioproc** -Member auf FourCC \_ mem fest.</span><span class="sxs-lookup"><span data-stu-id="188c0-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="188c0-121">Legen Sie den **pchBuffer** -Member so fest, dass er auf den Speicherblock verweist.</span><span class="sxs-lookup"><span data-stu-id="188c0-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="188c0-122">Legen Sie **pchBuffer** auf **null** fest, um anzufordern, dass der Datei-e/a-Manager den Speicherblock zuweist.</span><span class="sxs-lookup"><span data-stu-id="188c0-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="188c0-123">Legen Sie den **cchBuffer** -Member auf die anfängliche Größe des Speicherblocks fest.</span><span class="sxs-lookup"><span data-stu-id="188c0-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="188c0-124">Legen Sie den **adwinfo** -Member auf die minimale Erweiterungs Größe des Speicherblocks fest.</span><span class="sxs-lookup"><span data-stu-id="188c0-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="188c0-125">Legen Sie für eine nicht erweiterbare Speicherdatei **adwinfo** auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="188c0-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="188c0-126">Legen Sie alle anderen Elemente auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="188c0-126">Set all other members to zero.</span></span>

<span data-ttu-id="188c0-127">Es gibt keine Einschränkungen für das belegen von Speicher für die Verwendung als nicht erweiterbare Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="188c0-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 