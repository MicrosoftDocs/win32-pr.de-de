---
description: In diesem Abschnitt wird beschrieben, wie Sie aus einem systemeigenen Windows-Programm drucken.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Gewusst wie: Drucken von einem Windows-Programm'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349686"
---
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="c25b5-103">Gewusst wie: Drucken von einem Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="c25b5-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="c25b5-104">In diesem Abschnitt wird beschrieben, wie Sie aus einem systemeigenen Windows-Programm drucken.</span><span class="sxs-lookup"><span data-stu-id="c25b5-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="c25b5-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c25b5-105">Overview</span></span>

<span data-ttu-id="c25b5-106">Der Druckvorgang ist in der Regel ein wesentlicher Bestandteil eines nativen Windows-Programms.</span><span class="sxs-lookup"><span data-stu-id="c25b5-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="c25b5-107">Daher ist es kein Feature, das Sie nach dem Schreiben des Programms problemlos hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="c25b5-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="c25b5-108">Das heißt, wenn das Programm für die Verwendung von XPS-Dokumenten konzipiert ist, benötigen Sie ggf. zusätzlichen Code, um den Dokumentinhalt für den Druck zu rendieren.</span><span class="sxs-lookup"><span data-stu-id="c25b5-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="c25b5-109">Die XPS-Dokumente der Anwendung können direkt an einen Drucker gesendet werden, der über einen XPSDrv-Druckertreiber verfügt.</span><span class="sxs-lookup"><span data-stu-id="c25b5-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="c25b5-110">Verwenden Sie die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) , um den Dokumentinhalt und die [XPS-Druck-API](xps-printing.md) zu erstellen, um den Dokumentinhalt an den Drucker zu senden.</span><span class="sxs-lookup"><span data-stu-id="c25b5-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="c25b5-111">Die XPS-Druck-API verarbeitet den Dokumentinhalt für den Ziel Drucker.</span><span class="sxs-lookup"><span data-stu-id="c25b5-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="c25b5-112">Wenn der ausgewählte Drucker über einen XPSDrv-Druckertreiber verfügt, wird das Dokument ohne zusätzliche Konvertierung an den Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="c25b5-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="c25b5-113">Wenn der ausgewählte Drucker über einen GDI-basierten Druckertreiber verfügt, kann das Programm den Inhalt auch an den Drucker senden, und die XPS-Druck-API konvertiert den Dokumentinhalt so, dass er mit dem GDI-basierten Druckertreiber kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c25b5-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="c25b5-114">In beiden Fällen ist die Verarbeitung, die die Anwendung ausführt, identisch.</span><span class="sxs-lookup"><span data-stu-id="c25b5-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="c25b5-115">Drucken von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c25b5-115">Printing tasks</span></span>

<span data-ttu-id="c25b5-116">In den folgenden Themen werden die grundlegenden Schritte zum Drucken von Programminhalten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c25b5-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="c25b5-117">**Sammeln von Druckauftrags Informationen vom Benutzer.**</span><span class="sxs-lookup"><span data-stu-id="c25b5-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="c25b5-118">In der Regel initiiert ein Benutzer einen Druckauftrag, wenn die Option Drucken in einem Menü ausgewählt wird, und das Programm zeigt ein Druck Dialogfeld an, in dem die Details des Druckauftrags erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="c25b5-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="c25b5-119">Der Benutzer wählt in der Regel den Drucker, die Anzahl der Kopien und die Drucker Konfigurationsdetails aus, z. b. zweiseitiges Drucken und Heften.</span><span class="sxs-lookup"><span data-stu-id="c25b5-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="c25b5-120">Weitere Informationen hierzu finden Sie unter Gewusst [wie: Sammeln von Druckauftrags Informationen vom Benutzer](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="c25b5-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="c25b5-121">**Statusanzeige erstellen.**</span><span class="sxs-lookup"><span data-stu-id="c25b5-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="c25b5-122">Eine Statusanzeige bietet dem Benutzer Feedback darüber, wie der Druckauftrag fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c25b5-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="c25b5-123">Die Statusanzeige kann eine Statusanzeige sein, die Teil eines Dialog Felds ist, das die Schaltfläche **Abbrechen** für den Auftrag enthält, oder es kann sich um eine Statusleiste in der Statusleiste am unteren Rand des Hauptfensters handeln.</span><span class="sxs-lookup"><span data-stu-id="c25b5-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="c25b5-124">Weitere Informationen zur Funktions Anzeige finden Sie unter Gewusst [wie: Anzeigen des Status des Druckauftrags](cancel-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="c25b5-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="c25b5-125">Weitere Ideen zum Anzeigen des Status des Druckauftrags finden Sie in den Informationen in den Entwicklungs Richtlinien für die [Windows-Anwendungs Benutzeroberfläche](/windows/desktop/windows-application-ui-development) .</span><span class="sxs-lookup"><span data-stu-id="c25b5-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="c25b5-126">**Starten Sie den Druck Thread.**</span><span class="sxs-lookup"><span data-stu-id="c25b5-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="c25b5-127">Nachdem das Programm die Druckauftrags Informationen vom Benutzer gesammelt hat, kann es den Druck Thread starten, um die tatsächliche Verarbeitung des Dokuments zum Drucken auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c25b5-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="c25b5-128">Weitere Informationen zum Druck Thread finden Sie unter Gewusst [wie: starten und Abbrechen eines Druck Threads](how-to--start-and-stop-a-printing-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c25b5-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="c25b5-129">**Renderdruck Auftragsdaten.**</span><span class="sxs-lookup"><span data-stu-id="c25b5-129">**Render print job data.**</span></span>

    <span data-ttu-id="c25b5-130">Der Druck Thread rendert die Dokument Daten zum Drucken.</span><span class="sxs-lookup"><span data-stu-id="c25b5-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="c25b5-131">Sie sollten diese Verarbeitung in diskrete Verarbeitungsschritte unterbrechen, damit der Benutzer die Verarbeitung unterbrechen und den Auftrag abbrechen und den Verarbeitungs Thread nicht zulassen kann, um andere Threads und Prozesse zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="c25b5-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="c25b5-132">Informationen dazu, wie die Druckauftrags Daten rendert, finden [Sie unter Gewusst wie: Rendern von Druckauftrags Daten](how-to--render-the-print-job-data.md).</span><span class="sxs-lookup"><span data-stu-id="c25b5-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="c25b5-133">**Überwachen des Status des Druckauftrags.**</span><span class="sxs-lookup"><span data-stu-id="c25b5-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="c25b5-134">Aktualisieren Sie die Statusanzeige, wenn jeder Verarbeitungsschritt ausgeführt wird, um die Verwendung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="c25b5-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="c25b5-135">Berechnen Sie die Verarbeitungsschritte, um den angeforderten Auftrag abzuschließen, und aktualisieren Sie dann die Statusanzeige, wenn diese Schritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c25b5-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="c25b5-136">**Druckauftrag schließen und Druck Thread beenden.**</span><span class="sxs-lookup"><span data-stu-id="c25b5-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="c25b5-137">Nachdem das Programm den Druckauftrag an den Drucker gesendet hat, oder wenn der Benutzer den Druckauftrag abgebrochen hat, müssen Sie den Druckauftrag schließen und die vom Druckauftrag verwendeten Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="c25b5-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c25b5-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c25b5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c25b5-139">Gewusst wie: Sammeln von Druckauftrags Informationen vom Benutzer</span><span class="sxs-lookup"><span data-stu-id="c25b5-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
