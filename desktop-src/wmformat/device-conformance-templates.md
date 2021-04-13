---
title: Geräte Konformitäts Vorlagen
description: Geräte Konformitäts Vorlagen
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Codecs, Geräte Konformitäts Vorlagen
- Geräte Konformitäts Vorlagen, Informationen zu
- Vorlagen, Geräte Konformitäts Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311274"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="b323f-107">Geräte Konformitäts Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b323f-107">Device Conformance Templates</span></span>

<span data-ttu-id="b323f-108">Die Codecs der Windows Media 9-Serie unterstützen Geräte Konformitäts Vorlagen, bei denen es sich um definierte Bereiche von Datenstrom-Konfigurationseinstellungen und Codec-Algorithmen handelt.</span><span class="sxs-lookup"><span data-stu-id="b323f-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="b323f-109">Jede Vorlage definiert die Wertebereiche, die für bestimmte Geräte geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="b323f-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="b323f-110">In der Vergangenheit arbeiteten die Hardwarehersteller, die Geräte, die in der Lage waren, ASF-Dateien zu spielen, alle an Ihren eigenen Standards.</span><span class="sxs-lookup"><span data-stu-id="b323f-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="b323f-111">Dies führte zu den weitgehend unterschiedlichen Funktionen auf ähnlichen Geräten, die heute fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b323f-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="b323f-112">Mit den Geräte Konformitäts Vorlagen legen die Windows Media Codecs eine gemeinsame Basis für ähnliche Geräte fest.</span><span class="sxs-lookup"><span data-stu-id="b323f-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="b323f-113">Hardware Hersteller können angeben, welchen Vorlagen Ihre Geräte entsprechen. so können Inhalts Ersteller ihre Dateien zuverlässiger auf das Lesen von Geräten ausrichten.</span><span class="sxs-lookup"><span data-stu-id="b323f-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="b323f-114">Außerdem ist es für Player Anwendungen einfacher zu bestimmen, ob eine Datei für das Gerät ungeeignet ist, bevor versucht wird, Sie wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b323f-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="b323f-115">Eine Vorlage für die Geräte Konformität wird durch eine Zeichenfolge identifiziert, die als Metadatenattribut gespeichert ist, das dem Stream zugeordnet ist, für den die Vorlage gilt.</span><span class="sxs-lookup"><span data-stu-id="b323f-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="b323f-116">Eine Liste der Vorlagen und deren Zeichen folgen und Parameter finden Sie unter [Geräte](device-conformance-template-parameters.md)Übereinstimmungs-Vorlagen Parameter.</span><span class="sxs-lookup"><span data-stu-id="b323f-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="b323f-117">Geräte Konformitäts Vorlagen werden für alle Windows Media 9-und spätere Codecs unterstützt, mit Ausnahme der Windows Media Video 9-Bildschirm Codecs und des Windows Media Audio 9-Codec ohne Verlust.</span><span class="sxs-lookup"><span data-stu-id="b323f-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b323f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b323f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b323f-119">**Codec-Features**</span><span class="sxs-lookup"><span data-stu-id="b323f-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="b323f-120">**Arbeiten mit Geräte Konformitäts Vorlagen**</span><span class="sxs-lookup"><span data-stu-id="b323f-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




