---
description: Das ordnungsgemäße Einrichten von Symbolen für das Debuggen kann eine schwierige Aufgabe sein, insbesondere für das Kernel Debugging.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Symbolserver und Symbolspeicher"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214103"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="87f65-103">  Symbolserver und Symbolspeicher</span><span class="sxs-lookup"><span data-stu-id="87f65-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="87f65-104">Das ordnungsgemäße Einrichten von Symbolen für das Debuggen kann eine schwierige Aufgabe sein, insbesondere für das Kernel Debugging.</span><span class="sxs-lookup"><span data-stu-id="87f65-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="87f65-105">Häufig ist es erforderlich, dass Sie die Namen und Releases aller Produkte auf Ihrem Computer kennen.</span><span class="sxs-lookup"><span data-stu-id="87f65-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="87f65-106">Der Debugger muss in der Lage sein, die Symbol Dateien zu finden, die den einzelnen Produkt Releases und Service Pack entsprechen.</span><span class="sxs-lookup"><span data-stu-id="87f65-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="87f65-107">Dies kann zu einem extrem langen Symbol Pfad führen, der aus einer langen Liste von Verzeichnissen besteht.</span><span class="sxs-lookup"><span data-stu-id="87f65-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="87f65-108">Verwenden Sie den *Symbol Server*, um diese Schwierigkeiten beim koordinieren von Symbol Dateien zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="87f65-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="87f65-109">Der Symbol Server ermöglicht den Debuggern das automatische Abrufen der richtigen Symbol Dateien ohne Produktnamen, Releases oder Buildnummern.</span><span class="sxs-lookup"><span data-stu-id="87f65-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="87f65-110">Debugtools für Windows enthalten den SymSrv-Symbol Server.</span><span class="sxs-lookup"><span data-stu-id="87f65-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="87f65-111">Der Symbol Server wird aktiviert, indem eine bestimmte Text Zeichenfolge in den Symbol Pfad eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="87f65-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="87f65-112">Jedes Mal, wenn der Debugger Symbole für ein neu geladenes Modul laden muss, ruft er den Symbol Server auf, um die entsprechenden Symbol Dateien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="87f65-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="87f65-113">Der Symbol Server verwendet die Dateien in einem *Symbol Speicher*.</span><span class="sxs-lookup"><span data-stu-id="87f65-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="87f65-114">Dies ist eine Sammlung von Symbol Dateien, einem Index und einem Tool, das von einem Administrator zum Hinzufügen und Löschen von Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="87f65-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="87f65-115">Die Dateien werden nach eindeutigen Parametern, wie z. b. Zeitstempel und Bildgröße, indiziert.</span><span class="sxs-lookup"><span data-stu-id="87f65-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="87f65-116">Debugtools für Windows enthalten ein Symbol Speicher Tool namens SymStore.</span><span class="sxs-lookup"><span data-stu-id="87f65-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="87f65-117">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="87f65-117">For more information, see:</span></span>

-   [<span data-ttu-id="87f65-118">Verwenden von SymSrv</span><span class="sxs-lookup"><span data-stu-id="87f65-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="87f65-119">Verwenden von SymStore</span><span class="sxs-lookup"><span data-stu-id="87f65-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="87f65-120">Verwenden anderer Symbol Speicher</span><span class="sxs-lookup"><span data-stu-id="87f65-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="87f65-121">Optionen für SymStore-Command-Line</span><span class="sxs-lookup"><span data-stu-id="87f65-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="87f65-122">Symbol Server und Internet Firewalls</span><span class="sxs-lookup"><span data-stu-id="87f65-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="87f65-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87f65-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f65-124">Symbol Dateien</span><span class="sxs-lookup"><span data-stu-id="87f65-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 



