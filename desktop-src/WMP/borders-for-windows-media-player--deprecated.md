---
title: Rahmen für Windows-Media Player (veraltet)
description: Rahmen für Windows-Media Player (veraltet)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows-Media Player, Rahmen
- Windows Media Player Skins, Rahmen
- Skins, Rahmen
- Rahmen im Vergleich zu Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309983"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="505e5-107">Rahmen für Windows-Media Player (veraltet)</span><span class="sxs-lookup"><span data-stu-id="505e5-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="505e5-108">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="505e5-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="505e5-109">Ein Rahmen ähnelt einem Skin, aber anstatt die Benutzeroberfläche für den Compact-Modus von Windows Media Player zu ersetzen, wird ein Rahmen in den Bereich "jetzt wiedergegeben" der Windows-Media Player im Vollmodus eingebettet.</span><span class="sxs-lookup"><span data-stu-id="505e5-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="505e5-110">Mithilfe eines Windows Media-Download Pakets können Sie Inhalte mit einem Rahmen einschließen, um Multimedia-Anwendungen zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="505e5-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="505e5-111">Ein Beispiel für ein Windows-Medien Download Paket, das einen Rahmen und eingebetteten Inhalt enthält, ist im Verzeichnis "Samples" dieses SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="505e5-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="505e5-112">Erstellen eines Rahmens</span><span class="sxs-lookup"><span data-stu-id="505e5-112">Creating a Border</span></span>

<span data-ttu-id="505e5-113">Ein Rahmen wird auf die gleiche Weise wie ein Skin erstellt.</span><span class="sxs-lookup"><span data-stu-id="505e5-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="505e5-114">Der einzige Unterschied besteht darin, dass die Skin in den Bereich für die wieder **Gabe** eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="505e5-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="505e5-115">Dies bedeutet, dass die Skin-Größe nicht berechnet werden kann und dass alle Skin-Elemente relativ sein müssen.</span><span class="sxs-lookup"><span data-stu-id="505e5-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="505e5-116">Wenn der Benutzer die Größe des Windows-Media Player ändert, sind Teile des Rahmens möglicherweise abgeschnitten und werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="505e5-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="505e5-117">Laden eines Rahmens</span><span class="sxs-lookup"><span data-stu-id="505e5-117">Loading a Border</span></span>

<span data-ttu-id="505e5-118">Ein Rahmen wird geladen, wenn eine Windows Media-Metadatendatei geladen wird, die das **Skin** -Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="505e5-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="505e5-119">Das **href** -Attribut des **Skin** -Elements muss auf ein Skin verweisen.</span><span class="sxs-lookup"><span data-stu-id="505e5-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="505e5-120">Ein typisches **Skin** -Element würde wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="505e5-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="505e5-121">Weitere Informationen finden Sie unter [Skin-Element (veraltet)](skin-element--deprecated.md).</span><span class="sxs-lookup"><span data-stu-id="505e5-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="505e5-122">Einschließen von Inhalten mit einem Rahmen</span><span class="sxs-lookup"><span data-stu-id="505e5-122">Including Content with a Border</span></span>

<span data-ttu-id="505e5-123">Sie können Inhalte mit einem Rahmen mithilfe einer Windows Media-Download Datei (mit der Dateinamenerweiterung ". WMD") einschließen.</span><span class="sxs-lookup"><span data-stu-id="505e5-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="505e5-124">Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="505e5-124">Follow these steps:</span></span>

1.  <span data-ttu-id="505e5-125">Erstellen Sie den Rahmen.</span><span class="sxs-lookup"><span data-stu-id="505e5-125">Create the border.</span></span> <span data-ttu-id="505e5-126">Achten Sie darauf, dass Sie diese so erstellen, dass die Größe des Rahmens durch die Größe der Größe nicht ruiniert wird.</span><span class="sxs-lookup"><span data-stu-id="505e5-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="505e5-127">Fügen Sie z. b. keine Hintergrund Datei ein. machen Sie den Hintergrund transparent, damit eine Visualisierung dahinter ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="505e5-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="505e5-128">Komprimieren Sie den Inhalt der Skin (Kunst, JScript-Dateien und Skin-Definitionsdatei) in eine Datei mit der Dateinamenerweiterung. WMZ.</span><span class="sxs-lookup"><span data-stu-id="505e5-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="505e5-129">Erstellen Sie eine Windows Media-Metadatendatei (mit der Dateinamenerweiterung ". asx"), die auf die komprimierte Rahmen Datei (mit der Dateinamenerweiterung ". WMZ") verweist.</span><span class="sxs-lookup"><span data-stu-id="505e5-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="505e5-130">Die Metadatei kann Wiedergabelisten Informationen mit Metadaten für Kunst und URLs für bestimmten Inhalt enthalten.</span><span class="sxs-lookup"><span data-stu-id="505e5-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="505e5-131">Assemblieren Sie den Inhalt der digitalen Medien.</span><span class="sxs-lookup"><span data-stu-id="505e5-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="505e5-132">Komprimieren Sie den Rahmen, die Metadatendatei und den Inhalt in einer Datei, und versehen Sie Sie mit der Dateinamenerweiterung ". WMD".</span><span class="sxs-lookup"><span data-stu-id="505e5-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="505e5-133">Verwenden eines Rahmens</span><span class="sxs-lookup"><span data-stu-id="505e5-133">Using a Border</span></span>

<span data-ttu-id="505e5-134">Nachdem Sie die Windows Media-Download Datei erstellt haben, muss der Benutzer lediglich darauf doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="505e5-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="505e5-135">Die Datei wird auf den Computer des Benutzers heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="505e5-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="505e5-136">Die Dateien im Paket werden entpackt, die Wiedergabeliste wird den Wiedergabelisten hinzugefügt, der Rahmen wird im Fenster " **jetzt** wiedergegeben" des Windows-Media Player für den vollständigen Modus angezeigt, und das erste Element in der neuen Wiedergabeliste wird wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="505e5-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="505e5-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="505e5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="505e5-138">**Informationen zu Skins**</span><span class="sxs-lookup"><span data-stu-id="505e5-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="505e5-139">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="505e5-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="505e5-140">**Windows Media-Download Pakete (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="505e5-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




