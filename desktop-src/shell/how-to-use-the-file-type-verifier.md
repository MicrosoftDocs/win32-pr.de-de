---
description: In diesem Thema wird beschrieben, wie Sie den Dateityp Verifier verwenden, der im Windows 7 SDK bereitgestellt wird.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Verwenden des Dateityp-verifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104218891"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="67023-103">Verwenden des Dateityp-verifizierers</span><span class="sxs-lookup"><span data-stu-id="67023-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="67023-104">In diesem Thema wird beschrieben, wie Sie den Dateityp Verifier verwenden, der im [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="67023-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67023-105">Wenn das Programmdatei Typen erstellt, mit denen Benutzer von der Windows-Shell aus interagieren (in der Regel im bekannten Ordner eines Benutzers, z. b. " **eigene** Dateien"), ist es sehr wichtig, die Anwendung zu testen und zu überprüfen, ob die erstellten Dateien ordnungsgemäß registriert sind und eine hochwertige Benutzer Darstellung beim Durchsuchen und Durchsuchen von Dateien bieten.</span><span class="sxs-lookup"><span data-stu-id="67023-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="67023-106">Dies ist besonders wichtig, wenn Sie erwarten, dass Benutzer ihre Anwendungen unter Windows 7 ausführen, was für viele Shellfeatures hochwertige Dateityp Handler ist.</span><span class="sxs-lookup"><span data-stu-id="67023-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="67023-107">Führen Sie die folgenden Schritte aus, um den Dateityp mit dem Dateityp Verifier zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="67023-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="67023-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="67023-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="67023-109">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="67023-109">Step 1:</span></span>

<span data-ttu-id="67023-110">Installieren Sie die Anwendung in der Testumgebung, und kopieren Sie die Dateityp Überprüfung in diese Umgebung.</span><span class="sxs-lookup"><span data-stu-id="67023-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="67023-111">Der Dateityp Verifier ist im [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67023-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="67023-112">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="67023-112">Step 2:</span></span>

<span data-ttu-id="67023-113">Verwenden Sie Ihre Anwendung, um eine zu testende Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67023-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="67023-114">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="67023-114">Step 3:</span></span>

<span data-ttu-id="67023-115">Starten Sie den Dateityp Verifier.</span><span class="sxs-lookup"><span data-stu-id="67023-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="67023-116">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="67023-116">Step 4:</span></span>

<span data-ttu-id="67023-117">Wählen Sie die Kategorie für den Dateityp aus, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="67023-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![Screenshot, der die Drag & amp; Drop-Funktion anzeigt.](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="67023-119">Die Kategorieauswahl bestimmt den Satz von Tests, die vom Tool ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67023-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="67023-120">Wenn Ihr Typ unter mehr als eine Kategorie fallen könnte (z. b. kann eine TIF-Datei je nach Inhalt ein Bild oder ein Dokument sein), führen Sie das Tool erneut mit jeder entsprechenden Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="67023-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="67023-121">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="67023-121">Step 5:</span></span>

<span data-ttu-id="67023-122">Suchen Sie mithilfe von Windows-Explorer eine zu testende Datei, und ziehen Sie Sie mit der Maus auf das Ziel im Dateityp Verifier, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="67023-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![Screenshot der Drag & Drop-Funktion](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="67023-124">Schritt 6:</span><span class="sxs-lookup"><span data-stu-id="67023-124">Step 6:</span></span>

<span data-ttu-id="67023-125">Warten Sie, bis das Dateityp-Verifier-Tool eine Reihe von Tests durchläuft.</span><span class="sxs-lookup"><span data-stu-id="67023-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="67023-126">Der Fortschritt der Tests wird von der Statusanzeige wie im folgenden Screenshot dargestellt.</span><span class="sxs-lookup"><span data-stu-id="67023-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![Screenshot der Statusanzeige](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="67023-128">Schritt 7:</span><span class="sxs-lookup"><span data-stu-id="67023-128">Step 7:</span></span>

<span data-ttu-id="67023-129">Überprüfen Sie die Ergebnis Zusammenfassung Ihrer Dokument Dateityp Tests, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="67023-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![Screenshot der Ergebnis Zusammenfassung](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="67023-131">Schritt 8:</span><span class="sxs-lookup"><span data-stu-id="67023-131">Step 8:</span></span>

<span data-ttu-id="67023-132">Klicken Sie auf die Ergebnisse auf der Zusammenfassungs Seite, um das ausführliche Protokoll anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="67023-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="67023-133">Ein Beispiel Protokoll für einen Vorschau Handler wird im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="67023-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![Screenshot des Vorschau handlerprotokolls](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="67023-135">Schritt 9:</span><span class="sxs-lookup"><span data-stu-id="67023-135">Step 9:</span></span>

<span data-ttu-id="67023-136">Wenn Sie eine Kopie der Protokolldatei speichern möchten, klicken Sie am unteren Rand der Protokoll Anzeige auf **Protokolldatei speichern** , und wählen Sie einen geeigneten Speicherort für die Speicherung auf dem Computer aus.</span><span class="sxs-lookup"><span data-stu-id="67023-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="67023-137">Schritt 10:</span><span class="sxs-lookup"><span data-stu-id="67023-137">Step 10:</span></span>

<span data-ttu-id="67023-138">Wenn Fehler gemeldet werden, nehmen Sie die entsprechenden Änderungen in der Anwendung vor, und führen Sie das Tool erneut aus, um zu überprüfen, ob die Fehler nicht mehr in den Tests angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="67023-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="67023-139">Wenn Warnungen gemeldet werden, sollten Sie diese auswerten und entscheiden, ob Sie für Ihren speziellen Dateityp relevant sind, und die entsprechenden Änderungen an der Anwendung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="67023-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67023-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67023-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67023-141">Windows 7 SDK</span><span class="sxs-lookup"><span data-stu-id="67023-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



