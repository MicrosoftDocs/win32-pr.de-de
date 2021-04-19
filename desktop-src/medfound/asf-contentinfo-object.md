---
description: ASF-ContentInfo-Objekt
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: ASF-ContentInfo-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346054"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="018bd-103">ASF-ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="018bd-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="018bd-104">Das Objekt "ASF *ContentInfo* " speichert Informationen aus dem ASF-Header Objekt einer Datei.</span><span class="sxs-lookup"><span data-stu-id="018bd-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="018bd-105">Eine Anwendung kann das ContentInfo-Objekt für folgende Zwecke verwenden:</span><span class="sxs-lookup"><span data-stu-id="018bd-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="018bd-106">Lesen Sie das Header Objekt für eine vorhandene Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="018bd-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="018bd-107">In diesem Fall analysiert das ContentInfo-Objekt das Header Objekt und speichert Informationen über die Eigenschaften Datei.</span><span class="sxs-lookup"><span data-stu-id="018bd-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="018bd-108">Media Foundation stellt einige dieser Eigenschaften über Attribute und Schnittstellen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="018bd-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="018bd-109">Diese werden in [Media Foundation Attributen für ASF-Header Objekte](media-foundation-attributes-for-asf-header-objects.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="018bd-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="018bd-110">Schreiben Sie Header Informationen, und erstellen Sie ein Header Objekt für eine neue Datei.</span><span class="sxs-lookup"><span data-stu-id="018bd-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="018bd-111">Initialisieren Sie andere ASF-Objekte, z. b. den [ASF-Splitter](asf-splitter.md), den [ASF Multiplexer](asf-multiplexer.md)und den ASF-Indexer beim Lesen oder Schreiben einer Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="018bd-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="018bd-112">Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="018bd-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="018bd-113">Erstellen des ContentInfo-Objekts</span><span class="sxs-lookup"><span data-stu-id="018bd-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="018bd-114">Rufen Sie die [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) -Funktion auf, um eine neue Instanz des ContentInfo-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="018bd-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="018bd-115">Diese Methode gibt einen Zeiger auf ein leeres ContentInfo-Objekt zurück, das für die Arbeit mit einer bestimmten ASF-Datei initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="018bd-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="018bd-116">Abhängig davon, ob die Anwendung eine vorhandene Datei liest oder eine neue ASF-Datei schreibt, muss Sie [**imfasfcontentinfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) oder [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) aufrufen, um das leere Objekt aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="018bd-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="018bd-117">Weitere Informationen zu diesen Methoden aufrufen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="018bd-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="018bd-118">Lesen des ASF-Header Objekts einer vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="018bd-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="018bd-119">Informationen aus den ASF-Header Objekten werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="018bd-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="018bd-120">Schreiben eines ASF-Header Objekts für eine neue Datei</span><span class="sxs-lookup"><span data-stu-id="018bd-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="018bd-121">Media Foundation Attribute für ASF-Header Objekte</span><span class="sxs-lookup"><span data-stu-id="018bd-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="018bd-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="018bd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="018bd-123">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="018bd-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



