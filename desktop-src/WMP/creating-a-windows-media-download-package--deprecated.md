---
title: Erstellen eines Windows Media-Download Pakets (veraltet)
description: Erstellen eines Windows Media-Download Pakets (veraltet)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Windows Media-Download Pakete, erstellen
- Erstellen von Windows Media-Download Paketen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037168"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="e7e95-109">Erstellen eines Windows Media-Download Pakets (veraltet)</span><span class="sxs-lookup"><span data-stu-id="e7e95-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="e7e95-110">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e7e95-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="e7e95-111">Führen Sie diese Schritte aus, um ein Windows Media-Download Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7e95-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="e7e95-112">**Erstellen Sie einen Rahmen.**</span><span class="sxs-lookup"><span data-stu-id="e7e95-112">**Create a border.**</span></span> <span data-ttu-id="e7e95-113">Verwenden Sie dieselben Techniken, die Sie zum Erstellen eines Skin für Windows-Media Player verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7e95-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="e7e95-114">Entwerfen Sie den Rahmen so, dass das Ändern der Größe von Windows-Media Player nicht die Komposition der Border-Elemente ruiniert.</span><span class="sxs-lookup"><span data-stu-id="e7e95-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="e7e95-115">Verwenden Sie beispielsweise eine voll Tonfarbe oder Visualisierung als Hintergrund, da diese bei der Größenänderung von Windows Media Player gut skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="e7e95-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="e7e95-116">**Komprimieren Sie den Rahmen Inhalt.**</span><span class="sxs-lookup"><span data-stu-id="e7e95-116">**Compress the border contents.**</span></span> <span data-ttu-id="e7e95-117">Erstellen Sie einen komprimierten Ordner (mit der Dateinamenerweiterung ". zip"), der die Border-Dateien enthält: Bilder, JScript-Dateien und die Skin-Definitionsdatei mit der Dateinamenerweiterung ". WMS".</span><span class="sxs-lookup"><span data-stu-id="e7e95-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="e7e95-118">Benennen Sie die komprimierte Datei so um, dass Sie die Dateinamenerweiterung. WMZ enthält.</span><span class="sxs-lookup"><span data-stu-id="e7e95-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="e7e95-119">**Schreiben Sie eine Windows Media-Metadatendatei.**</span><span class="sxs-lookup"><span data-stu-id="e7e95-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="e7e95-120">Windows Media Player lädt den Rahmen nur dann, wenn Sie eine Windows Media-Metadatendatei mit der Dateinamenerweiterung ". asx" erstellen, die das **Skin** -Element implementiert.</span><span class="sxs-lookup"><span data-stu-id="e7e95-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="e7e95-121">Die Metadatei kann auch verwendet werden, um eine Wiedergabeliste zu erstellen, die den im Paket enthaltenen Inhalt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e7e95-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="e7e95-122">**Assemblieren Sie Ihre Inhalte.**</span><span class="sxs-lookup"><span data-stu-id="e7e95-122">**Assemble your content.**</span></span> <span data-ttu-id="e7e95-123">Legen Sie alle Dateien, die Sie verwenden möchten, in einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="e7e95-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="e7e95-124">Dies schließt Audiodateien, Videodateien, Metadateien und Rahmen Definitions Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="e7e95-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="e7e95-125">**Erstellen Sie das Paket.**</span><span class="sxs-lookup"><span data-stu-id="e7e95-125">**Create the package.**</span></span> <span data-ttu-id="e7e95-126">Erstellen Sie einen komprimierten Ordner (mit der Dateinamenerweiterung ". zip"), der die Rand Datei, Inhalts Dateien und die Metadatendatei enthält.</span><span class="sxs-lookup"><span data-stu-id="e7e95-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="e7e95-127">Ändern Sie die Dateinamenerweiterung dieser zip-Datei in die Dateinamenerweiterung. WMD.</span><span class="sxs-lookup"><span data-stu-id="e7e95-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="e7e95-128">**Veröffentlichen Sie das Paket auf einer Website.**</span><span class="sxs-lookup"><span data-stu-id="e7e95-128">**Post the package to a website.**</span></span> <span data-ttu-id="e7e95-129">Das fertige Paket ist bereit für die Bereitstellung auf einer Website und von Benutzern heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="e7e95-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7e95-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7e95-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e95-131">**Windows Media-Download Pakete (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="e7e95-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




