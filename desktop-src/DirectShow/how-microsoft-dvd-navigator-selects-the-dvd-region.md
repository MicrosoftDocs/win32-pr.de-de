---
description: Auswählen des DVD-Bereichs durch Microsoft DVD Navigator
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Auswählen des DVD-Bereichs durch Microsoft DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343120"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="f5a3d-103">Auswählen des DVD-Bereichs durch Microsoft DVD Navigator</span><span class="sxs-lookup"><span data-stu-id="f5a3d-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="f5a3d-104">Der Microsoft DVD Navigator verwendet den folgenden Algorithmus, um die Regions Übereinstimmung bei der Wiedergabe von DVD-CDs auf einem PC zu bestimmen</span><span class="sxs-lookup"><span data-stu-id="f5a3d-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="f5a3d-105">Der DVD-Navigator Ruft den Bereich für die Festplatte, den Laufwerk Bereich und den decoderbereich ab.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="f5a3d-106">Wenn der Festplatten Bereich "alle Regionen" ist, gibt der DVD-Navigator die Festplatte aus.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="f5a3d-107">Wenn die Festplatte nicht für alle Regionen markiert ist, überprüft der DVD-Navigator, ob der Decoder einen voreingestellten Bereich aufweist.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="f5a3d-108">Wenn der Decoder einen voreingestellten Bereich hat, der nicht mit dem Bereich der Festplatte identisch ist, gibt der DVD-Navigator einen Fehler zurück, der anzeigt, dass er die CD nicht in der aktuellen DVD-Konfiguration wiedergeben kann</span><span class="sxs-lookup"><span data-stu-id="f5a3d-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="f5a3d-109">Abstiegs</span><span class="sxs-lookup"><span data-stu-id="f5a3d-109">(Exit)</span></span>
5.  <span data-ttu-id="f5a3d-110">Wenn der decoderbereich nicht festgelegt ist oder mit dem Bereich der Festplatte identisch ist, überprüft der DVD-Navigator, ob der Laufwerks Bereich mit dem Bereich der Festplatte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="f5a3d-111">Wenn die Laufwerks Region mit dem Bereich der Festplatte übereinstimmt, gibt der DVD-Navigator den Titel wieder.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="f5a3d-112">Andernfalls ruft der DVD-Navigator den Code auf, wenn der Treiber Bereich nicht mit dem Bereich der Festplatte identisch ist, um den Bereich des Laufwerks zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="f5a3d-113">Wenn die zulässige Anzahl von Regions Änderungen ausgeschöpft ist, tritt beim Änderungs Versuch der Region ein Fehler auf, und der Titel kann auf diesem System nicht wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5a3d-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5a3d-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5a3d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5a3d-115">Unterstützung der Änderung von DVD-Regionen in Windows</span><span class="sxs-lookup"><span data-stu-id="f5a3d-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



