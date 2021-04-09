---
title: Öffnen und Schließen von Streams
description: Öffnen und Schließen von Streams
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream-Funktion
- Avistreamrelease-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036678"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="3c45b-105">Öffnen und Schließen von Streams</span><span class="sxs-lookup"><span data-stu-id="3c45b-105">Opening and Closing Streams</span></span>

<span data-ttu-id="3c45b-106">Das Öffnen von Datenströmen ähnelt dem Öffnen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="3c45b-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="3c45b-107">Sie können einen Stream mithilfe der [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) -Funktion öffnen.</span><span class="sxs-lookup"><span data-stu-id="3c45b-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="3c45b-108">Diese Funktion erstellt eine Datenstrom Schnittstelle, platziert ein Handle des Streams in der-Schnittstelle und gibt einen Zeiger auf die-Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="3c45b-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="3c45b-109">**AVIFileGetStream** verwaltet auch den Verweis Zähler der Anwendungen, die einen Stream geöffnet haben, jedoch nicht von den Anwendungen, die ihn geschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="3c45b-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="3c45b-110">Wenn Sie auf einen einzelnen Datenstrom in einer Datei zugreifen möchten, können Sie die Datei und den Datenstrom mithilfe der [**avistreamopenfromfile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) -Funktion öffnen.</span><span class="sxs-lookup"><span data-stu-id="3c45b-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="3c45b-111">Diese Funktion kombiniert die Vorgänge und Funktionsargumente der Funktionen [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) und **AVIFileGetStream** .</span><span class="sxs-lookup"><span data-stu-id="3c45b-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="3c45b-112">Wenn Sie auf mehr als einen Stream in einer Datei zugreifen möchten, verwenden Sie **AVIFileOpen** , gefolgt von mehreren Aufrufen von **AVIFileGetStream**.</span><span class="sxs-lookup"><span data-stu-id="3c45b-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="3c45b-113">Sie können den Verweis Zähler eines Streams erhöhen, indem Sie die [**avistreamadref**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) -Funktion verwenden, um einen Datenstrom geöffnet zu lassen, wenn Sie eine Funktion verwenden, die normalerweise den Datenstrom schließt.</span><span class="sxs-lookup"><span data-stu-id="3c45b-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="3c45b-114">Sie können einen Stream mit der [**avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) -Funktion schließen.</span><span class="sxs-lookup"><span data-stu-id="3c45b-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="3c45b-115">Diese Funktion Dekremente den Verweis Zähler des Streams und schließt diese, wenn der Verweis Zähler Null erreicht.</span><span class="sxs-lookup"><span data-stu-id="3c45b-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="3c45b-116">Ihre Anwendungen sollten den Verweis Zähler ausgleichen, indem Sie für jede Verwendung der [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)-, [**avifileforatestream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)-, **avistreamadressf**-oder **avistreamopenfromfile** -Funktion einen **avistreamrelease** -Befehl einschließen.</span><span class="sxs-lookup"><span data-stu-id="3c45b-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="3c45b-117">Wenn Sie einen Stream freigeben, der mithilfe von **avistreamopenfromfile** geöffnet wurde, schließt avifile die Datei, die den Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="3c45b-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="3c45b-118">Wenn Ihre Anwendung eine Datei mit geöffneten Datenströmen freigibt, schließt avifile die Streams erst, wenn alle Streams freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="3c45b-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 




