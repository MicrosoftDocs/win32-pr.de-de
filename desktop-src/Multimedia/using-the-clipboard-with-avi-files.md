---
title: Verwenden der Zwischenablage mit AVI-Dateien
description: Verwenden der Zwischenablage mit AVI-Dateien
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Aviputfleonclipboard-Funktion
- Avigetfromclipboard-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710620"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="7dbf4-105">Verwenden der Zwischenablage mit AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="7dbf4-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="7dbf4-106">Die Zwischenablage bietet einen bequemen temporären Speicher, der von einer Anwendung zum Kopieren oder übertragen von AVI-Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="7dbf4-107">Avifile umfasst Zwischenablage Funktionen, die Sie mit Datenträger-oder Arbeitsspeicher Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="7dbf4-108">Mithilfe der [**aviputfleonclipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) -Funktion können Sie eine Datei in die Zwischenablage kopieren.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="7dbf4-109">Um eine Datei in der Zwischenablage in den Arbeitsspeicher oder Datenträger zu schreiben, verwenden Sie die [**avigetfromclipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="7dbf4-110">Mithilfe der [**aviclearclipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) -Funktion können Sie eine Datei aus der Zwischenablage löschen.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="7dbf4-111">Diese Funktion löscht keine anderen Arten von Informationen, z. b. Text, aus der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="7dbf4-112">Wenn Sie in der Anwendung Zwischenablage Funktionen verwenden, löschen Sie die Zwischenablage mit **aviclearclipboard** , bevor Sie die Anwendung schließen oder die Datei in der Zwischenablage schließen.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="7dbf4-113">Sie können **aviclearclipboard** in Ihrer Anwendung aufrufen, unabhängig davon, ob **aviputfleonclipboard** verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="7dbf4-114">Wenn Ihre Anwendung eine Datei in die Zwischenablage kopiert und die Datei Streamdaten enthält, die sich möglicherweise ändern, können Sie mithilfe der [**avimakefilefromstreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) -Funktion eine Speicherdatei mit geklonten Streams erstellen.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="7dbf4-115">Anschließend können Sie die Datei in der Zwischenablage platzieren und die ursprüngliche Datei freigeben, ohne sie ungültig zu machen.</span><span class="sxs-lookup"><span data-stu-id="7dbf4-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 




