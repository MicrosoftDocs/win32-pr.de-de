---
title: Farbraum-Typbezeichner
description: Diese Konstanten geben den Typ eines Zeichen Arrays für die Zeichenfolge 2 an. Bei den folgenden Werten handelt es sich um gültige Farb Raum Array Typen.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "106351183"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="a0747-104">Farbraum-Typbezeichner</span><span class="sxs-lookup"><span data-stu-id="a0747-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="a0747-105">Diese Konstanten geben den Typ eines Zeichen Arrays für die Zeichenfolge 2 an.</span><span class="sxs-lookup"><span data-stu-id="a0747-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="a0747-106">Bei den folgenden Werten handelt es sich um gültige Farb Raum Array Typen.</span><span class="sxs-lookup"><span data-stu-id="a0747-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="a0747-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**</span><span class="sxs-lookup"><span data-stu-id="a0747-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-108">Ein ciebaseda-Farb Raum Array aus dem monochrome Profil erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0747-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA \_ grau**</span><span class="sxs-lookup"><span data-stu-id="a0747-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-110">Ein ciebaseda-Farb Raum Array aus dem monochrome Profil erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0747-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**</span><span class="sxs-lookup"><span data-stu-id="a0747-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-112">Ein ciebasedabc-Farbraum-Array aus dem RGB-oder L- <sup>\*</sup> a- <sup>\*</sup> b-Profil erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0747-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="a0747-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-114">Ein ciebaseddef-Farbraum-Array aus dem RGB-oder L- <sup>\*</sup> a- <sup>\*</sup> b-Profil erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0747-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="a0747-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-116">Holen Sie sich ein ciebaseddef-Farbraum, gefolgt von einem ciebasedabc-Farbraum-Array aus dem RGB-Profil.</span><span class="sxs-lookup"><span data-stu-id="a0747-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="a0747-117">Bei der Ausführung verwendet die Funktion die ciebasedabc-Definition, wenn der Drucker keine ciebaseddef-Farbraum unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0747-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA- \_ Labor**</span><span class="sxs-lookup"><span data-stu-id="a0747-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-119">Ruft ein ciebasedabc-Farbraum-Array aus dem L <sup>\*</sup> a <sup>\*</sup> b-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="a0747-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA- \_ DEFG**</span><span class="sxs-lookup"><span data-stu-id="a0747-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-121">Ein ciebaseddefg-Farbraum-Array aus dem CMYK-Profil wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a0747-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0747-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**</span><span class="sxs-lookup"><span data-stu-id="a0747-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a0747-123">Ein ciebasedcmyk-Farbraum aus dem CMYK-Profil erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0747-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a0747-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0747-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0747-125">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="a0747-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="a0747-126">ICM-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a0747-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




