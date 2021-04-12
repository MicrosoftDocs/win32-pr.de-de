---
description: Entwicklung von DVD-Decodern in DirectShow
ms.assetid: c00ff132-fee1-47b5-8a8a-df7cb920ad89
title: Entwicklung von DVD-Decodern in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3de64b3c1d91dbf5f22ba3e4b4ae8fe78edda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482430"
---
# <a name="dvd-decoder-development-in-directshow"></a><span data-ttu-id="8c1a2-103">Entwicklung von DVD-Decodern in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8c1a2-103">DVD Decoder Development in DirectShow</span></span>

<span data-ttu-id="8c1a2-104">Dieser Abschnitt enthält Verweise auf die Referenzseiten für alle DirectShow-Eigenschaften Sätze und-Schnittstellen, die entweder DVD-spezifisch sind oder bei der DVD-Decodierung häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c1a2-104">This section contains pointers to the reference pages for all the DirectShow property sets and interfaces that are either DVD-specific or else used extensively in DVD decoding.</span></span> <span data-ttu-id="8c1a2-105">Zusätzlich zu den hier aufgeführten Angaben müssen ein Decoder und seine Pins auch die generischen DirectShow-Filter Schnittstellen unterstützen, wie unter [Schreiben von DirectShow-Filtern](writing-directshow-filters.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8c1a2-105">In addition to what is listed here, a decoder and its pins must also support the generic DirectShow filter interfaces as described in [Writing DirectShow Filters](writing-directshow-filters.md).</span></span>

<span data-ttu-id="8c1a2-106">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="8c1a2-106">This section contains the following topics.</span></span>

-   [<span data-ttu-id="8c1a2-107">Decodersteuerelement</span><span class="sxs-lookup"><span data-stu-id="8c1a2-107">Decoder Volume Control</span></span>](decoder-volume-control.md)
-   [<span data-ttu-id="8c1a2-108">Unterstützung der Änderung von DVD-Regionen in Windows</span><span class="sxs-lookup"><span data-stu-id="8c1a2-108">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)

<span data-ttu-id="8c1a2-109">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="8c1a2-109">See also:</span></span>

-   [<span data-ttu-id="8c1a2-110">**DVD-Karaoke-Eigenschaften Satz**</span><span class="sxs-lookup"><span data-stu-id="8c1a2-110">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="8c1a2-111">**Eigenschaften Satz für den DVD-Kopierschutz**</span><span class="sxs-lookup"><span data-stu-id="8c1a2-111">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="8c1a2-112">**Eigenschaften Satz des DVD-Teil Bilds**</span><span class="sxs-lookup"><span data-stu-id="8c1a2-112">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="8c1a2-113">PIN-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="8c1a2-113">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="8c1a2-114">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="8c1a2-114">**IKsPropertySet**</span></span>](ikspropertyset.md)
-   <span data-ttu-id="8c1a2-115">[**Ivideoframestep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (nur Hardware-Decoder)</span><span class="sxs-lookup"><span data-stu-id="8c1a2-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (hardware decoders only)</span></span>
-   <span data-ttu-id="8c1a2-116">[**Ivpconfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (nur Hardware-Decoder)</span><span class="sxs-lookup"><span data-stu-id="8c1a2-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (hardware decoders only)</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c1a2-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c1a2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c1a2-118">Decoder-Schnittstellen und Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="8c1a2-118">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



