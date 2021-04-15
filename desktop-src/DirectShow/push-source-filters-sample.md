---
description: Beispiel für Push-Quell Filter
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Beispiel für Push-Quell Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521331"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="51c53-103">Beispiel für Push-Quell Filter</span><span class="sxs-lookup"><span data-stu-id="51c53-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="51c53-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51c53-104">Description</span></span>

<span data-ttu-id="51c53-105">Dieses Beispiel besteht aus einem Satz von drei Quell filtern, die die folgenden Quelldaten als Videostream bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="51c53-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="51c53-106">Cpushsourcebitmap: Single Bitmap (aus aktuellem Verzeichnis geladen)</span><span class="sxs-lookup"><span data-stu-id="51c53-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="51c53-107">Cpushsourcebitmapset: Satz von Bitmaps (aus aktuellem Verzeichnis geladen)</span><span class="sxs-lookup"><span data-stu-id="51c53-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="51c53-108">Cpushsourcedesktop: Kopie des aktuellen Desktop Abbilds (nur GDI)</span><span class="sxs-lookup"><span data-stu-id="51c53-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="51c53-109">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="51c53-109">Usage</span></span>

<span data-ttu-id="51c53-110">Wenn Sie einen Filter verwenden möchten, laden Sie ihn in GraphEdit, und rendieren Sie seine Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="51c53-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="51c53-111">Dadurch wird eine Verbindung mit einem Videorenderer (und möglicherweise mit einem Farb Raum Konverter-Filter) hergestellt, und Sie können die Ausgabe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="51c53-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="51c53-112">Wenn Sie die Ausgabe in eine AVI-Datei renderten möchten, laden Sie die Datei "AVI MUX", laden Sie einen Datei Schreiber Filter, geben Sie einen Ausgabe Namen an den dateiwriter an, und renderten Sie die Ausgabe-PIN des pushsource</span><span class="sxs-lookup"><span data-stu-id="51c53-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="51c53-113">Sie können auch Video Kompressoren, Video Effekte usw. Laden und verbinden.</span><span class="sxs-lookup"><span data-stu-id="51c53-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="51c53-114">Der Desktop Erfassungs Filter bietet keine Unterstützung für Hardware Überlagerungen, sodass das Video, das auf einer über Lagerungs Oberfläche gerendert wird, oder Cursor, die über die Hardware über</span><span class="sxs-lookup"><span data-stu-id="51c53-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="51c53-115">Er verwendet GDI zum Konvertieren des aktuellen Desktop Bilds in eine Bitmap, die als Beispiel für ein Medium an die Ausgabe-PIN übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="51c53-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="51c53-116">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="51c53-116">Downloading the Sample</span></span>

<span data-ttu-id="51c53-117">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="51c53-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="51c53-118">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ pushsource.</span><span class="sxs-lookup"><span data-stu-id="51c53-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51c53-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51c53-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51c53-120">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="51c53-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



