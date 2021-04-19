---
title: CMM-Transformationserstellungsflags
description: CMMS verwenden Transformations Erstellungs Flags als Hinweise zum Erstellen einer Farb Transformation. Der CMM kann feststellen, wie diese Flags am besten verwendet werden.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "106349750"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="64d2e-104">CMM-Transformationserstellungsflags</span><span class="sxs-lookup"><span data-stu-id="64d2e-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="64d2e-105">CMMS verwenden Transformations Erstellungs Flags als Hinweise zum Erstellen einer Farb Transformation.</span><span class="sxs-lookup"><span data-stu-id="64d2e-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="64d2e-106">Der CMM kann feststellen, wie diese Flags am besten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64d2e-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="64d2e-107">Alle Funktionen, die diese Flags verwenden, übergeben oder empfangen Flagwerte über einen Parameter namens *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="64d2e-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="64d2e-108">Das höchst wertige **Wort** von *dwFlags* sollte auf einen Wert aus der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64d2e-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="64d2e-109">Konstante</span><span class="sxs-lookup"><span data-stu-id="64d2e-109">Constant</span></span>                    | <span data-ttu-id="64d2e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64d2e-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d2e-111">Aktivieren der über \_ Prüfung von Gamut \_</span><span class="sxs-lookup"><span data-stu-id="64d2e-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="64d2e-112">Verwenden Sie diese Transformation für die Überprüfung der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="64d2e-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="64d2e-113">\_relative \_ farbige Metrik verwenden</span><span class="sxs-lookup"><span data-stu-id="64d2e-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="64d2e-114">Behalten Sie den weißen Punkt nicht bei.</span><span class="sxs-lookup"><span data-stu-id="64d2e-114">Do not preserve the white point.</span></span> <span data-ttu-id="64d2e-115">Wenn der Ausgabe Farbskala eine angegebene Farbe nicht unterstützt, verwenden Sie die nächste unterstützte Farbe.</span><span class="sxs-lookup"><span data-stu-id="64d2e-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="64d2e-116">Siehe Rendering Intents.</span><span class="sxs-lookup"><span data-stu-id="64d2e-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="64d2e-117">schnelles \_ übersetzen</span><span class="sxs-lookup"><span data-stu-id="64d2e-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="64d2e-118">Nur Farbe suchen.</span><span class="sxs-lookup"><span data-stu-id="64d2e-118">Look up color only.</span></span> <span data-ttu-id="64d2e-119">Die Farbe kann nicht interpolieren werden.</span><span class="sxs-lookup"><span data-stu-id="64d2e-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="64d2e-120">Preserveblack</span><span class="sxs-lookup"><span data-stu-id="64d2e-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="64d2e-121">Fügt die entsprechende "Black Generation GMMP" als letztes GMMP in der Transformations Sequenz ein.</span><span class="sxs-lookup"><span data-stu-id="64d2e-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="64d2e-122">immer WCS \_</span><span class="sxs-lookup"><span data-stu-id="64d2e-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="64d2e-123">Verwenden Sie den WCS-Codepfad auch für ICC-Transformationen.</span><span class="sxs-lookup"><span data-stu-id="64d2e-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="64d2e-124">sequenzielle \_ Transformation</span><span class="sxs-lookup"><span data-stu-id="64d2e-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="64d2e-125">Transformations Erstellungs Flag zum Erstellen einer sequenziellen (nicht optimierten) Farb Transformation.</span><span class="sxs-lookup"><span data-stu-id="64d2e-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="64d2e-126">Das nieder wertige **Wort** kann einen der folgenden Konstanten Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="64d2e-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="64d2e-127">Konstante</span><span class="sxs-lookup"><span data-stu-id="64d2e-127">Constant</span></span>     | <span data-ttu-id="64d2e-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64d2e-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d2e-129">Nachweis \_ Modus</span><span class="sxs-lookup"><span data-stu-id="64d2e-129">PROOF\_MODE</span></span>  | <span data-ttu-id="64d2e-130">Die Transformation wird verwendet, um eine Vorschau des Bilds anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64d2e-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="64d2e-131">Niedrige Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="64d2e-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="64d2e-132">normaler \_ Modus</span><span class="sxs-lookup"><span data-stu-id="64d2e-132">NORMAL\_MODE</span></span> | <span data-ttu-id="64d2e-133">Die Transformation wird für die normale Bild Anzeige verwendet.</span><span class="sxs-lookup"><span data-stu-id="64d2e-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="64d2e-134">Durchschnittliche Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="64d2e-134">Average image quality.</span></span>                            |
| <span data-ttu-id="64d2e-135">Bester \_ Modus</span><span class="sxs-lookup"><span data-stu-id="64d2e-135">BEST\_MODE</span></span>   | <span data-ttu-id="64d2e-136">Die Transformation wird für die Anzeige des qualitativ hochwertigen Bilds verwendet, das auf dem Zielgerät möglich ist.</span><span class="sxs-lookup"><span data-stu-id="64d2e-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="64d2e-137">Wenn Sie vom Nachweis \_ Modus zum besten \_ Modus wechseln, wird die Ausgabequalität in der Regel verbessert, und die Transformations Geschwindigkeit wird</span><span class="sxs-lookup"><span data-stu-id="64d2e-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64d2e-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64d2e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d2e-139">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="64d2e-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="64d2e-140">ICM-Konstanten</span><span class="sxs-lookup"><span data-stu-id="64d2e-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




