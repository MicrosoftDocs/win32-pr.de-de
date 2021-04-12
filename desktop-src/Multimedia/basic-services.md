---
title: Grundlegende Dienste
description: Grundlegende Dienste
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- Multimedia-Datei-e/a, grundlegende Dienste
- Datei-e/a, grundlegende Dienste
- Eingabe und Ausgabe (e/a), grundlegende Dienste
- E/a (Eingabe und Ausgabe), grundlegende Dienste
- grundlegende e/a
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390278"
---
# <a name="basic-services"></a><span data-ttu-id="f8755-109">Grundlegende Dienste</span><span class="sxs-lookup"><span data-stu-id="f8755-109">Basic Services</span></span>

<span data-ttu-id="f8755-110">Die Verwendung der grundlegenden e/a-Dienste ähnelt der Verwendung der Lauf Zeit Datei-e/a-Dienste der C-Lauf Zeit Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="f8755-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="f8755-111">Dateien müssen geöffnet werden, bevor Sie gelesen oder geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="f8755-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="f8755-112">Nach dem Lesen oder schreiben muss die Datei geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="f8755-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="f8755-113">Sie können auch den aktuellen Lese-oder Schreib Speicherort innerhalb einer geöffneten Datei ändern.</span><span class="sxs-lookup"><span data-stu-id="f8755-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="f8755-114">Bevor Sie mit e/a-Vorgängen in einer Datei beginnen, müssen Sie die Datei mit der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion öffnen.</span><span class="sxs-lookup"><span data-stu-id="f8755-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="f8755-115">Diese Funktion gibt ein Datei Handle vom Typ **hmmio** zurück.</span><span class="sxs-lookup"><span data-stu-id="f8755-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="f8755-116">Sie können dieses Datei Handle verwenden, um die geöffnete Datei zu identifizieren, wenn Sie andere Datei-e/a-Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f8755-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="f8755-117">Ein **hmmio** -Datei Handle ist kein Standarddatei handle.</span><span class="sxs-lookup"><span data-stu-id="f8755-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="f8755-118">Verwenden Sie keine **hmmio** -Datei Handles mit Win32-oder C-Lauf Zeit Datei-e/a-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f8755-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="f8755-119">Wenn Sie [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) verwenden, um eine Datei zu öffnen, verwenden Sie ein Flag, um anzugeben, ob Sie es zum Lesen, schreiben oder beides öffnen.</span><span class="sxs-lookup"><span data-stu-id="f8755-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="f8755-120">Sie können auch Flags angeben, die es Ihnen ermöglichen, eine Datei zu erstellen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f8755-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="f8755-121">Verwenden Sie die Funktion " [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) ", um eine Datei zu schließen, wenn Sie das Lesen oder schreiben in Sie abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="f8755-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="f8755-122">Sie können Dateien mit den Funktionen [**mmioread**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) und [**mmiowrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="f8755-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="f8755-123">Der nächste Lese-oder Schreibvorgang erfolgt an der aktuellen Dateiposition oder dem Dateizeiger in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="f8755-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="f8755-124">Die aktuelle Dateiposition wird immer dann erweitert, wenn eine Datei gelesen oder geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f8755-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="f8755-125">Sie können auch die aktuelle Dateiposition ändern, indem Sie die [**mmioseek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="f8755-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="f8755-126">Stellen Sie sicher, dass Sie einen gültigen Speicherort in einer Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="f8755-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="f8755-127">Wenn Sie einen ungültigen Speicherort angeben, z. b. nach dem Ende der Datei, gibt **mmioseek** möglicherweise keinen Fehler zurück, aber nachfolgende e/a-Vorgänge könnten fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="f8755-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="f8755-128">Es gibt Flags, die Sie mit der **mmioopen** -Funktion für Vorgänge über einfache Datei-e/a verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f8755-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="f8755-129">Durch Angeben einer [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur können Sie z. b. Arbeitsspeicher Dateien öffnen, eine benutzerdefinierte e/a-Prozedur angeben oder einen Puffer für gepufferte e/a-Vorgänge angeben.</span><span class="sxs-lookup"><span data-stu-id="f8755-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 