---
title: Informationen zu benutzerdefinierten Datei-und streamhandlern
description: Informationen zu benutzerdefinierten Datei-und streamhandlern
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video für Windows (Vfw), benutzerdefinierte Datei Handler
- Video für Windows (Vfw), benutzerdefinierte Datenstrom Handler
- Video für Windows (Vfw), Datei Handler
- Video für Windows (Vfw), Datenstrom Handler
- VFW (Video für Windows), benutzerdefinierte Datei Handler
- VFW (Video für Windows), benutzerdefinierte Datenstrom Handler
- VFW (Video für Windows), Datei Handler
- VFW (Video für Windows), Datenstrom Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856916"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="e9dd6-111">Informationen zu benutzerdefinierten Datei-und streamhandlern</span><span class="sxs-lookup"><span data-stu-id="e9dd6-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="e9dd6-112">Die Anwendung kann einen benutzerdefinierten Datei Handler zum Lesen aus einer Datei oder schreiben in eine Datei verwenden, die nicht dem Standard entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="e9dd6-113">Zu diesem Zweck verwendet Ihre Anwendung einfach den Namen Ihres Datei Handlers, wenn Sie die Datei öffnen oder die Datei Schnittstelle zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="e9dd6-114">Die avifile-Bibliothek verwendet dann die Funktionen Ihres Datei Handlers anstelle der von einem anderen Datei Handler.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="e9dd6-115">Das nicht dem Standard entsprechende Format wird als Standard-AVI-Daten für Ihre Anwendung oder eine beliebige andere Anwendung mit Ihrem benutzerdefinierten Datei Handler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="e9dd6-116">Ebenso kann die Anwendung einen benutzerdefinierten Datenstrom Handler verwenden, um einen Datenstrom zu lesen, der nicht dem Standard entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="e9dd6-117">Ein Datenstrom – ob es sich um Audiodaten, Video-, MIDI-, Text-oder benutzerdefinierte Daten handelt – ist eine Komponente einer AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="e9dd6-118">Eine AVI-Datei, die eine Videosequenz, einen englischen Sound Sound und einen französischen Sound enthält, besteht beispielsweise aus drei Streams.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="e9dd6-119">Die Anwendung kann die Datenströme in einer AVI-Datei angeben, um die Datenströme zu verarbeiten und an einen Handler weiterzuleiten, der den entsprechenden Typ von Multimedia-Daten optimal verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="e9dd6-120">Sie müssen benutzerdefinierte Stream-und Datei Handler in einer oder mehreren DLLs platzieren, die von den Haupt Anwendungs Dateien getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="e9dd6-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




