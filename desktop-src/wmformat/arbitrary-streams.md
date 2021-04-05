---
title: Beliebige Streams
description: Beliebige Streams
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media-Format-SDK, beliebige Streams
- Advanced Systems Format (ASF), beliebige Streams
- ASF (Advanced Systems Format), beliebige Streams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- beliebige Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707871"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="10c33-110">Beliebige Streams</span><span class="sxs-lookup"><span data-stu-id="10c33-110">Arbitrary Streams</span></span>

<span data-ttu-id="10c33-111">Zusätzlich zu den Audio-und Videostreams und bildstreams kann eine ASF-Datei Datenströme aufnehmen, die eine Vielzahl von Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="10c33-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="10c33-112">Die Objekte des Windows Media SDK-SDKs unterstützen Skriptstreams, Datei Übertragungsdaten Ströme, Webstreams und beliebige Datenströme.</span><span class="sxs-lookup"><span data-stu-id="10c33-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="10c33-113">Alle diese Streamtypen sind willkürlich, d. h., es erfolgt keine Datenüberprüfung durch das Lese Objekt.</span><span class="sxs-lookup"><span data-stu-id="10c33-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="10c33-114">Wenn Sie Streams dieser Typen in Ihre Dateien einschließen, achten Sie darauf, dass die Leseanwendung eine Validierung oder Datenüberprüfung durchführt, um sicherzustellen, dass Ihre Inhalte nicht beschädigt oder absichtlich von einem böswilligen Drittanbieter manipuliert wurden.</span><span class="sxs-lookup"><span data-stu-id="10c33-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="10c33-115">Obwohl die Objekte dieses SDK die Daten in beliebigen Streams nicht überprüfen oder validieren, werden verschiedene Typen von beliebigen Datenströmen nativ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10c33-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="10c33-116">In der folgenden Tabelle sind die vordefinierten willkürlichen Streamtypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="10c33-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="10c33-117">Skript Datenströme werden ebenfalls unterstützt, werden jedoch separat im Abschnitt [Skript Befehle](script-commands.md) behandelt.</span><span class="sxs-lookup"><span data-stu-id="10c33-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="10c33-118">Weitere Informationen zum Erstellen von benutzerdefinierten Typen finden Sie unter [benutzerdefinierte beliebige Datenströme](custom-arbitrary-data-streams.md).</span><span class="sxs-lookup"><span data-stu-id="10c33-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="10c33-119">Beliebiger Typ</span><span class="sxs-lookup"><span data-stu-id="10c33-119">Arbitrary type</span></span>                   | <span data-ttu-id="10c33-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10c33-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="10c33-121">Textstreams</span><span class="sxs-lookup"><span data-stu-id="10c33-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="10c33-122">Enthalten Text Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="10c33-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="10c33-123">Dateistreams</span><span class="sxs-lookup"><span data-stu-id="10c33-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="10c33-124">Enthalten mindestens eine Datendatei.</span><span class="sxs-lookup"><span data-stu-id="10c33-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="10c33-125">Webstreams</span><span class="sxs-lookup"><span data-stu-id="10c33-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="10c33-126">Enthalten Datendateien, die der zwischengespeicherten Version von Webseiten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="10c33-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="10c33-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10c33-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10c33-128">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="10c33-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="10c33-129">**Audiodaten und Videostreams**</span><span class="sxs-lookup"><span data-stu-id="10c33-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="10c33-130">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="10c33-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




