---
description: Weitere Informationen finden Sie in den CAB-API-Makros.
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: CAB-API-Makros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522867"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="942e1-103">CAB-API-Makros</span><span class="sxs-lookup"><span data-stu-id="942e1-103">Cabinet API Macros</span></span>

<span data-ttu-id="942e1-104">In diesem Abschnitt werden die von der CAB-API verwendeten Makros ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="942e1-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="942e1-105">FCI-Makros</span><span class="sxs-lookup"><span data-stu-id="942e1-105">FCI Macros</span></span>

<span data-ttu-id="942e1-106">Die folgenden Makros werden von FCI verwendet:</span><span class="sxs-lookup"><span data-stu-id="942e1-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="942e1-107">Makro</span><span class="sxs-lookup"><span data-stu-id="942e1-107">Macro</span></span>                                              | <span data-ttu-id="942e1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="942e1-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="942e1-109">**FNF-Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="942e1-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="942e1-110">Wird verwendet, um Arbeitsspeicher in einem FCI-Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="942e1-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="942e1-111">**Fnficiclose**</span><span class="sxs-lookup"><span data-stu-id="942e1-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="942e1-112">Wird verwendet, um eine Datei zu schließen.</span><span class="sxs-lookup"><span data-stu-id="942e1-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="942e1-113">**Fnficidelete**</span><span class="sxs-lookup"><span data-stu-id="942e1-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="942e1-114">Wird verwendet, um eine Datei zu löschen.</span><span class="sxs-lookup"><span data-stu-id="942e1-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="942e1-115">**FNF-Datei platziert**</span><span class="sxs-lookup"><span data-stu-id="942e1-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="942e1-116">Wird verwendet, um zu benachrichtigen, wenn eine Datei in der CAB-Datei platziert wird.</span><span class="sxs-lookup"><span data-stu-id="942e1-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="942e1-117">**FNF-frei**</span><span class="sxs-lookup"><span data-stu-id="942e1-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="942e1-118">Wird verwendet, um zuvor zugeordneten Speicher in einem FCI-kontextfrei zugeben.</span><span class="sxs-lookup"><span data-stu-id="942e1-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="942e1-119">**Fnscigetnextcabinet**</span><span class="sxs-lookup"><span data-stu-id="942e1-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="942e1-120">Wird verwendet, um Informationen für den nächsten Schrank anzufordern.</span><span class="sxs-lookup"><span data-stu-id="942e1-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="942e1-121">**FNF-getopeninfo**</span><span class="sxs-lookup"><span data-stu-id="942e1-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="942e1-122">Wird verwendet, um eine Datei zu öffnen und Datum, Uhrzeit und Attribute der Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="942e1-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="942e1-123">**Fnficigettempfile**</span><span class="sxs-lookup"><span data-stu-id="942e1-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="942e1-124">Wird zum Abrufen eines temporären Datei namens verwendet.</span><span class="sxs-lookup"><span data-stu-id="942e1-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="942e1-125">**FNF-offen**</span><span class="sxs-lookup"><span data-stu-id="942e1-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="942e1-126">Wird zum Öffnen einer Datei in einem FCI-Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="942e1-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="942e1-127">**FNF-Lesevorgänge**</span><span class="sxs-lookup"><span data-stu-id="942e1-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="942e1-128">Wird zum Lesen von Daten aus einer Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="942e1-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="942e1-129">**FNF-Seek**</span><span class="sxs-lookup"><span data-stu-id="942e1-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="942e1-130">Wird verwendet, um einen Dateizeiger an eine angegebene Position zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="942e1-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="942e1-131">**Fnfcistatus**</span><span class="sxs-lookup"><span data-stu-id="942e1-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="942e1-132">Wird verwendet, um den Benutzer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="942e1-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="942e1-133">**FNF schreiben**</span><span class="sxs-lookup"><span data-stu-id="942e1-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="942e1-134">Wird verwendet, um Daten in eine Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="942e1-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="942e1-135">**Tcompfromlzxwindow**</span><span class="sxs-lookup"><span data-stu-id="942e1-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="942e1-136">Konvertiert die Windows-Größe in einen lxz-tcomp-Wert für " [**sciaddfile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)".</span><span class="sxs-lookup"><span data-stu-id="942e1-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="942e1-137">FDI-Makros</span><span class="sxs-lookup"><span data-stu-id="942e1-137">FDI Macros</span></span>

<span data-ttu-id="942e1-138">Die folgenden Makros werden von FDI verwendet:</span><span class="sxs-lookup"><span data-stu-id="942e1-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="942e1-139">Makro</span><span class="sxs-lookup"><span data-stu-id="942e1-139">Macro</span></span>                              | <span data-ttu-id="942e1-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="942e1-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="942e1-141">**Fnzuweisung**</span><span class="sxs-lookup"><span data-stu-id="942e1-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="942e1-142">Wird verwendet, um Speicher in einem FDI-Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="942e1-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="942e1-143">**Fnclose**</span><span class="sxs-lookup"><span data-stu-id="942e1-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="942e1-144">Wird verwendet, um eine Datei in einem FDI-Kontext zu schließen.</span><span class="sxs-lookup"><span data-stu-id="942e1-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="942e1-145">**Fnodinotifizieren**</span><span class="sxs-lookup"><span data-stu-id="942e1-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="942e1-146">Wird verwendet, um die Anwendung auf den Status des Decoders zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="942e1-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="942e1-147">**Fnfree**</span><span class="sxs-lookup"><span data-stu-id="942e1-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="942e1-148">Wird verwendet, um zuvor zugeordneten Speicher in einem FDI-kontextfrei zugeben.</span><span class="sxs-lookup"><span data-stu-id="942e1-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="942e1-149">**Fnopen**</span><span class="sxs-lookup"><span data-stu-id="942e1-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="942e1-150">Wird zum Öffnen einer Datei in einem FDI-Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="942e1-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="942e1-151">**Fnread**</span><span class="sxs-lookup"><span data-stu-id="942e1-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="942e1-152">Wird zum Lesen von Daten aus einer Datei in einem FDI-Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="942e1-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="942e1-153">**Fnseek**</span><span class="sxs-lookup"><span data-stu-id="942e1-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="942e1-154">Wird verwendet, um einen Dateizeiger an die angegebene Position in einem FDI-Kontext zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="942e1-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="942e1-155">**Fnwrite**</span><span class="sxs-lookup"><span data-stu-id="942e1-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="942e1-156">Wird verwendet, um Daten in eine Datei in einem FDI-Kontext zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="942e1-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="942e1-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="942e1-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="942e1-158">CAB-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="942e1-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="942e1-159">Verwenden der CAB-API</span><span class="sxs-lookup"><span data-stu-id="942e1-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




