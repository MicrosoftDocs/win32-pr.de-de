---
title: Ausgabe Format-Enumeration
description: Ausgabe Format-Enumeration
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media-Format-SDK, Ausgabe Format Enumerationen
- Advanced Systems Format (ASF), Ausgabe Format Enumerationen
- ASF (Advanced Systems Format), Ausgabe Format Enumerationen
- Windows Media-Format-SDK, iwmreadertypenegotiationinterface
- Advanced Systems Format (ASF), iwmreadertypenegotiations-Schnittstelle
- ASF (Advanced Systems Format), iwmreadertypenegotiationinterface
- Ausgabe formatenumerationen
- Iwmreadertypenegotiziierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038510"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="a1b6d-111">Ausgabe Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a1b6d-111">Output Format Enumeration</span></span>

<span data-ttu-id="a1b6d-112">Sowohl das Reader-Objekt als auch das synchrone Reader-Objekt kommunizieren mit den Codecs, um die möglichen Ausgabeformate für komprimierte Streams aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="a1b6d-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="a1b6d-113">Wenn Sie eine Datei lesen, die mit einem oder mehreren der Windows Media-Codecs komprimierte Inhalte enthält, können Sie die möglichen Ausgabeformate untersuchen, um den Wert auszuwählen, der Ihren Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="a1b6d-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="a1b6d-114">Zur einfacheren Verwendung hat jeder Codec ein Standardausgabeformat, das auf das am häufigsten verwendete Format festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1b6d-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="a1b6d-115">Weitere Informationen zur Ausgabe Enumeration finden Sie unter [Arbeiten mit Ausgaben](working-with-outputs.md).</span><span class="sxs-lookup"><span data-stu-id="a1b6d-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="a1b6d-116">Sie können bestimmte Änderungen an einem Ausgabeformat vornehmen, abhängig vom Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a1b6d-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="a1b6d-117">Für Videostreams können Sie z. b. die Frame Größe und die Farbtiefe ändern.</span><span class="sxs-lookup"><span data-stu-id="a1b6d-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="a1b6d-118">Die Lese Objekte unterstützen beide eine Schnittstelle zum Testen von Änderungen, die Sie an das Ausgabeformat vornehmen, die als [**iwmreadertypenegotität**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation)bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a1b6d-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1b6d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1b6d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1b6d-120">**Funktionen zum Lesen von Dateien**</span><span class="sxs-lookup"><span data-stu-id="a1b6d-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




