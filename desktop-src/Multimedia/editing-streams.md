---
title: Bearbeiten von Streams
description: Bearbeiten von Streams
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- Funktion "deateeditablestream"
- Editstreamcut-Funktion
- Editstreamcopy-Funktion
- Editstreampaste-Funktion
- Editstreamclone-Funktion
- Editstreamabtinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471461"
---
# <a name="editing-streams"></a><span data-ttu-id="e1c12-109">Bearbeiten von Streams</span><span class="sxs-lookup"><span data-stu-id="e1c12-109">Editing Streams</span></span>

<span data-ttu-id="e1c12-110">Sie können einen Stream erstellen, den Sie [**mit der Funktion**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) "-Funktion" in der Funktion "Funktion" bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="e1c12-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="e1c12-111">Diese Funktion initialisiert die Umgebung zum Bearbeiten eines Streams.</span><span class="sxs-lookup"><span data-stu-id="e1c12-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="e1c12-112">Dazu gehört das Erstellen einer Schnittstelle für den neuen Stream und interne Bearbeitungs Tabellen, die Änderungen am Stream nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="e1c12-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="e1c12-113">" **Kreateeditablestream** " gibt einen Datenstrom Zeiger auf einen bearbeitbaren Datenstrom zurück, der für andere streambearbeitungs Funktionen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e1c12-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="e1c12-114">Der bearbeitbare Streamzeiger kann auch von anderen avifile-Funktionen verwendet werden, die Streamzeiger akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="e1c12-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="e1c12-115">Sie können ein oder mehrere Beispiele aus einem bearbeitbaren Stream mithilfe der [**editstreamcut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) -Funktion Ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="e1c12-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="e1c12-116">Um Beispiele aus dem bearbeitbaren Stream zu entfernen, fügt diese Funktion einen Eintrag in die Bearbeitungs Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="e1c12-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="e1c12-117">Die Funktion platziert dann eine Kopie der Ausschneide Proben in einem neuen temporären Stream, dessen Schnittstellen Zeiger in einer Variablen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1c12-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="e1c12-118">Sie können ein oder mehrere Beispiele aus einem bearbeitbaren Datenstrom mithilfe der [**editstreamcopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) -Funktion in einen temporären Stream kopieren.</span><span class="sxs-lookup"><span data-stu-id="e1c12-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="e1c12-119">**Editstreamcopy** platziert Kopien der Beispiele in einem neuen temporären Stream, dessen Schnittstellen Zeiger in einer Variablen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1c12-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="e1c12-120">Sie können ein oder mehrere Beispiele aus einem Stream kopieren und in einen bearbeitbaren Stream einfügen, indem Sie die [**editstreampaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1c12-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="e1c12-121">Um die Beispiele an der angegebenen Position einzufügen, fügt diese Funktion einen Eintrag in der Bearbeitungs Tabelle des bearbeitbaren Ziel Datenstroms hinzu.</span><span class="sxs-lookup"><span data-stu-id="e1c12-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="e1c12-122">Sie können einen bearbeitbaren Stream mithilfe der [**editstreamclone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) -Funktion duplizieren.</span><span class="sxs-lookup"><span data-stu-id="e1c12-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="e1c12-123">Diese Funktion gibt einen Zeiger auf die streamschnittstelle des neuen Streams zurück.</span><span class="sxs-lookup"><span data-stu-id="e1c12-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="e1c12-124">Sie können diese Datenströme in die Zwischenablage kopieren oder Sie verwenden, um einen Pfad der an einen Stream vorgenommenen Änderungen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e1c12-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="e1c12-125">Sie können mehrere der Merkmale eines bearbeitbaren Streams mithilfe der [**editstreamtstinfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) -Funktion ändern.</span><span class="sxs-lookup"><span data-stu-id="e1c12-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="e1c12-126">Diese Funktion aktualisiert die Prioritäts Einstellung, die Sprache, die Skala und die Rate, die Startzeit, die Qualitätseinstellung, die Abmessungen und Koordinaten des Ziel Rechtecks und die Textbeschreibung des Streams.</span><span class="sxs-lookup"><span data-stu-id="e1c12-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="e1c12-127">Diese Elemente werden in der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur gespeichert, die dem bearbeitbaren Stream zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e1c12-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="e1c12-128">Sie können auch die Textbeschreibung eines bearbeitbaren Streams mithilfe der Funktion [**editstreamsetname**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) ändern.</span><span class="sxs-lookup"><span data-stu-id="e1c12-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="e1c12-129">Diese Funktion aktualisiert den **szName** -Member der **AVISTREAMINFO** -Struktur, die dem bearbeitbaren Stream zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e1c12-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="e1c12-130">Die Bearbeitungsfunktionen funktionieren in Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="e1c12-130">The editing functions work on streams.</span></span> <span data-ttu-id="e1c12-131">Sie müssen jeden Stream einzeln Ausschneiden und einfügen und dann die [**avimakefilefromstreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) -Funktion verwenden, um einen neuen Dateizeiger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1c12-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="e1c12-132">Die Bearbeitungs Tabellen in einem bearbeitbaren Stream behalten alle Änderungen für einen Datenstrom bei.</span><span class="sxs-lookup"><span data-stu-id="e1c12-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="e1c12-133">Der Quellstream wird nie geändert.</span><span class="sxs-lookup"><span data-stu-id="e1c12-133">The source stream is never changed.</span></span>

 

 

 




