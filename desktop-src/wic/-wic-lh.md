---
description: Windows-Bilderstellungskomponente
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Windows-Bilderstellungskomponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216966"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="bdb40-103">Windows-Bilderstellungskomponente</span><span class="sxs-lookup"><span data-stu-id="bdb40-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="bdb40-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="bdb40-104">Purpose</span></span>

<span data-ttu-id="bdb40-105">Bei der Windows Imaging Component (WIC) handelt es sich um eine erweiterbare Plattform, die eine Low-Level-API für digitale Images bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bdb40-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="bdb40-106">WIC unterstützt die Standardweb Bildformate, hohe dynamische Bereichs Bilder und unformatierte Kameradaten.</span><span class="sxs-lookup"><span data-stu-id="bdb40-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="bdb40-107">WIC unterstützt auch zusätzliche Funktionen wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="bdb40-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="bdb40-108">Integrierte Unterstützung für standardmetadatenformate</span><span class="sxs-lookup"><span data-stu-id="bdb40-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="bdb40-109">Erweiterbares Framework für Bild Codecs, Pixel Formate und Metadatenformate.</span><span class="sxs-lookup"><span data-stu-id="bdb40-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="bdb40-110">Unterstützung für eine breite Palette an Pixel Formaten.</span><span class="sxs-lookup"><span data-stu-id="bdb40-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="bdb40-111">Unterstützung für hohe Farben; Dazu zählen der erweiterte 30-Bit-Bereich, die 30-Bit-Genauigkeit mit hoher Genauigkeit und 48-Bit-Pixel Formate mit hoher Genauigkeit und Breite.</span><span class="sxs-lookup"><span data-stu-id="bdb40-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="bdb40-112">Die progressive Bild Decodierung.</span><span class="sxs-lookup"><span data-stu-id="bdb40-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bdb40-113">Entwicklerzielgruppe</span><span class="sxs-lookup"><span data-stu-id="bdb40-113">Developer Audience</span></span>

<span data-ttu-id="bdb40-114">WIC ist so konzipiert, dass die Anforderungen der folgenden Klassen von Entwicklern erfüllt werden:</span><span class="sxs-lookup"><span data-stu-id="bdb40-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="bdb40-115">Entwickler, die Bilddaten in einer Anwendung lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="bdb40-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="bdb40-116">Entwickler, die Bild Metadaten in einer Anwendung lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="bdb40-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="bdb40-117">Entwickler, die die Laufzeit-Codec-Ermittlung für neu entworfene oder implementierte Bild Codecs benötigen.</span><span class="sxs-lookup"><span data-stu-id="bdb40-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="bdb40-118">Entwickler, die neue Bild Codecs und Metadatenformate entwerfen oder implementieren.</span><span class="sxs-lookup"><span data-stu-id="bdb40-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="bdb40-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bdb40-119">In this section</span></span>



| <span data-ttu-id="bdb40-120">Thema</span><span class="sxs-lookup"><span data-stu-id="bdb40-120">Topic</span></span>                                                                 | <span data-ttu-id="bdb40-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdb40-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="bdb40-122">Neues in WIC</span><span class="sxs-lookup"><span data-stu-id="bdb40-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="bdb40-123">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="bdb40-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="bdb40-124">Beschreibt die Verwendung der WIC-APIs.</span><span class="sxs-lookup"><span data-stu-id="bdb40-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="bdb40-125">Verweis</span><span class="sxs-lookup"><span data-stu-id="bdb40-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="bdb40-126">Enthält den Verweis auf die WIC-APIs.</span><span class="sxs-lookup"><span data-stu-id="bdb40-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="bdb40-127">WIC-Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdb40-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="bdb40-128">Enthält Beispiele für WIC.</span><span class="sxs-lookup"><span data-stu-id="bdb40-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="bdb40-129">Glossar</span><span class="sxs-lookup"><span data-stu-id="bdb40-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="bdb40-130">Definiert Begriffe, die in WIC verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdb40-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




