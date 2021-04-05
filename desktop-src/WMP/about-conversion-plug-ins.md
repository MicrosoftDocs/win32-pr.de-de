---
title: Informationen zu Konvertierungs-Plug-ins
description: Informationen zu Konvertierungs-Plug-ins
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, Konvertierungs-Plug-ins
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, Informationen
- Advanced Systems Format (ASF)
- ASF (Advanced Systems-Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708052"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="c6851-109">Informationen zu Konvertierungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="c6851-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="c6851-110">Sie können ein Windows Media Player-Plug-in erstellen, um digitale Mediendateien, die mithilfe von nicht von Microsoft bereitgestellten Technologien erstellt wurden, in das Advanced Systems Format (ASF) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c6851-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="c6851-111">Konvertierungs-Plug-ins sind Component Object Model (com)-Objekte, die als ausführbare Dateien (exe-Dateien) verpackt und verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c6851-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="c6851-112">Windows Media Player instanziiert Konvertierungs-Plug-ins, um digitale Medienformate von Drittanbietern in den folgenden Szenarien zu konvertieren:</span><span class="sxs-lookup"><span data-stu-id="c6851-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="c6851-113">Der Inhalt digitaler Medien wird von einem tragbaren Gerät auf den Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="c6851-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="c6851-114">Inhalt digitaler Medien wird der Bibliothek mithilfe von **iwmpmediacollection:: Add** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6851-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="c6851-115">Inhalt digitaler Medien wird mithilfe der Suchfunktion von Windows Media Player der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6851-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="c6851-116">Inhalt digitaler Medien wird der Bibliothek von der Ordner Überwachungsfunktion von Windows Media Player hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6851-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="c6851-117">Inhalt digitaler Medien wird der Synchronisierungs Liste hinzugefügt, wenn der Benutzer eine Datei zieht und löscht.</span><span class="sxs-lookup"><span data-stu-id="c6851-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="c6851-118">Nachdem Windows Media Player eine Instanz eines Konvertierungs-Plug-Ins erstellt hat, muss das Plug-in die bereitgestellte Datei in ASF oder WMA konvertieren und relevante Metadaten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c6851-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="c6851-119">(Verwenden Sie nicht das Konvertierungs-Plug-in, um die Datei zu transcodieren.) Das Plug-in muss dann die konvertierte Datei in den angegebenen Ordner kopieren und den Pfad zur neuen Datei an Windows Media Player zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c6851-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="c6851-120">Konvertierungs-Plug-Ins müssen die **iwmpconvert** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="c6851-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="c6851-121">Weitere Informationen finden Sie unter [Programmier Referenz für Konvertierungen](conversion-plug-ins-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c6851-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6851-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6851-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6851-123">**Informationen zum Konvertierungsprozess**</span><span class="sxs-lookup"><span data-stu-id="c6851-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="c6851-124">**Hinzufügen von Metadaten zu konvertierten Dateien**</span><span class="sxs-lookup"><span data-stu-id="c6851-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="c6851-125">**Windows Media Player-Konvertierungs-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="c6851-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




