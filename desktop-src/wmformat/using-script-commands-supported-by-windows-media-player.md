---
title: Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden
description: Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media-Format-SDK, Skript Befehle
- Windows Media-Format-SDK, Windows Media Player
- Advanced Systems Format (ASF), Skript Befehle
- ASF (Advanced Systems Format), Skript Befehle
- Advanced Systems Format (ASF), Windows Media Player
- ASF (Advanced Systems Format), Windows Media Player
- Skripts, Befehle
- Skripts, Windows-Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037046"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="abb65-112">Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="abb65-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="abb65-113">Das SDK für den Windows Media-Format bietet keine native Unterstützung für das Auswerten und reagieren auf Skript Befehle.</span><span class="sxs-lookup"><span data-stu-id="abb65-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="abb65-114">Sie müssen eine beliebige Logik im Zusammenhang mit Skript Befehlen in der Anwendung einschließen.</span><span class="sxs-lookup"><span data-stu-id="abb65-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="abb65-115">Die verwendeten Skript Typen müssen auch in der Anwendung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="abb65-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="abb65-116">Sie können Code einschließen, um dieselben Skript Befehle zu verarbeiten, die von Windows Media Player unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="abb65-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="abb65-117">Die Beibehaltung der Kompatibilität mit Windows-Media Player macht Ihre Dateien universeller, als wenn Sie benutzerdefinierte Skript Befehle einbetten.</span><span class="sxs-lookup"><span data-stu-id="abb65-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="abb65-118">In der folgenden Tabelle sind die Skript Typen aufgeführt, die von Windows Media Player unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="abb65-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="abb65-119">Skripttyp</span><span class="sxs-lookup"><span data-stu-id="abb65-119">Script type</span></span> | <span data-ttu-id="abb65-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abb65-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb65-121">URL</span><span class="sxs-lookup"><span data-stu-id="abb65-121">URL</span></span>         | <span data-ttu-id="abb65-122">Der Player sendet die angegebene URL an den Browser, damit Sie dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abb65-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="abb65-123">Wenn ein eingebettetes Player-Steuerelement verwendet wird, können Sie einen bestimmten Frame Verweis auf die URL hinzufügen, indem Sie die &&*frameName* -Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="abb65-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="abb65-124">Einfügen</span><span class="sxs-lookup"><span data-stu-id="abb65-124">FILENAME</span></span>    | <span data-ttu-id="abb65-125">Eine URL zu einer anderen zu Wiedergabe enden Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="abb65-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="abb65-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="abb65-126">CAPTION</span></span>     | <span data-ttu-id="abb65-127">Eine Text Zeichenfolge, die im Beschriftungen Bereich von Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abb65-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="abb65-128">Dieser Typ unterstützt die HTML-Standard Formatierung, sodass der Text so formatiert werden kann, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="abb65-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="abb65-129">Ein Beispiel für die Verwendung von Untertiteln.</span><span class="sxs-lookup"><span data-stu-id="abb65-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="abb65-130">EREIGNIS</span><span class="sxs-lookup"><span data-stu-id="abb65-130">EVENT</span></span>       | <span data-ttu-id="abb65-131">Der Name eines Ereignisses, das auftreten soll.</span><span class="sxs-lookup"><span data-stu-id="abb65-131">The name of an event that is to occur.</span></span> <span data-ttu-id="abb65-132">Der Ereignistyp unterstützt Anpassungen für Ihre eigenen Verwendungszwecke.</span><span class="sxs-lookup"><span data-stu-id="abb65-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="abb65-133">Der Code für das angegebene Ereignis muss in der Windows Media-Metadatendatei für den Datenstrom definiert werden, damit der Player das angegebene Ereignis ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="abb65-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="abb65-134">Ein Beispiel für die Verwendung von Werbe Einfügungs.</span><span class="sxs-lookup"><span data-stu-id="abb65-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="abb65-135">OpenEvent</span><span class="sxs-lookup"><span data-stu-id="abb65-135">OPENEVENT</span></span>   | <span data-ttu-id="abb65-136">Dieses Skript befindet sich vor dem eigentlichen-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="abb65-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="abb65-137">Das OpenEvent ermöglicht dem Player, den Inhalt vorab zu puffern, damit der Wechsel zwischen Streams bei Auftreten des Ereignisses nahtlos erscheint.</span><span class="sxs-lookup"><span data-stu-id="abb65-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="abb65-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="abb65-138">TEXT</span></span>        | <span data-ttu-id="abb65-139">Eine Text Zeichenfolge, die im Beschriftungen Bereich von Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abb65-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="abb65-140">Kann nur-Text-, Sami-oder HTML-formatierter Text sein.</span><span class="sxs-lookup"><span data-stu-id="abb65-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="abb65-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abb65-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abb65-142">**Verwenden von Skript Befehlen**</span><span class="sxs-lookup"><span data-stu-id="abb65-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




