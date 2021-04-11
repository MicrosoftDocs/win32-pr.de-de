---
title: Farb Raum Konvertierung
description: Farb Raum Konvertierung
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media-Format-SDK, Farb Raum Konvertierung
- Advanced Systems Format (ASF), Farb Raum Konvertierung
- ASF (Advanced Systems Format), Farb Raum Konvertierung
- Farb Raum Konvertierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206749"
---
# <a name="color-space-conversion"></a><span data-ttu-id="8056a-107">Farb Raum Konvertierung</span><span class="sxs-lookup"><span data-stu-id="8056a-107">Color Space Conversion</span></span>

<span data-ttu-id="8056a-108">Häufig gibt es einen Unterschied zwischen der Farbtiefe des komprimierten Video Formats im Profil und dem Eingabeformat.</span><span class="sxs-lookup"><span data-stu-id="8056a-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="8056a-109">In diesem Fall muss das Quellvideo konvertiert werden, damit es dem Farbraum des Ziels entspricht.</span><span class="sxs-lookup"><span data-stu-id="8056a-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="8056a-110">Der Writer verarbeitet diesen Prozess und kommuniziert mit einem internen Farb Raum Konverter.</span><span class="sxs-lookup"><span data-stu-id="8056a-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="8056a-111">Der Reader kommuniziert auch mit dem Farb Raum Konverter, um den Unterschied zwischen dem komprimierten Format und dem Ausgabeformat abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="8056a-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="8056a-112">Wie bei allen Transformationen, die für Daten ausgeführt werden, kann durch die Umwandlung zwischen Farbtiefen die Qualität der Ausgabe verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8056a-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="8056a-113">Wenn möglich, sollten Sie Eingabe-und Ausgabeformate mit der gleichen Farbtiefe wie das komprimierte Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="8056a-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8056a-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8056a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8056a-115">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="8056a-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="8056a-116">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="8056a-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="8056a-117">**Arbeiten mit Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="8056a-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




