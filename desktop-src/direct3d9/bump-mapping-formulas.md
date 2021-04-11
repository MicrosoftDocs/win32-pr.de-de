---
description: Direct3D wendet die folgenden Formeln auf die du-und DV-Komponenten in jedem Bump Map-Pixel an.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Bump-mappinenformeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127780"
---
# <a name="bump-mapping-formulas-direct3d-9"></a><span data-ttu-id="9b2cb-103">Bump-mappinenformeln (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9b2cb-103">Bump Mapping Formulas (Direct3D 9)</span></span>

<span data-ttu-id="9b2cb-104">Direct3D wendet die folgenden Formeln auf die Komponenten "D<sub>U</sub> " und "d<sub>V</sub> " in jedem Bump Map-Pixel an.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-104">Direct3D applies the following formulas to the D<sub>U</sub> and D<sub>V</sub> components in each bump map pixel.</span></span>

![Formeln für die Transformationen der Bump-mappingmatrix](images/dudv-transform.png)

<span data-ttu-id="9b2cb-106">In diesen Formeln werden die Variablen d<sub>u</sub> und d<sub>v</sub> direkt von einem Bump-Karten Pixel entnommen und durch eine 2 x 2-Matrix transformiert, um die Ausgabe Delta Werte d<sub>u</sub>' und d<sub>v</sub>' zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-106">In these formulas, the D<sub>U</sub> and D<sub>V</sub> variables are taken directly from a bump map pixel and transformed by a 2x2 matrix to produce the output delta values D<sub>U</sub>' and D<sub>V</sub>'.</span></span> <span data-ttu-id="9b2cb-107">Das System verwendet die Ausgabewerte, um die Texturkoordinaten zu ändern, die die Umgebungs Zuordnung in der nächsten Textur Phase adressieren.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-107">The system uses the output values to modify the texture coordinates that address the environment map in the next texture stage.</span></span> <span data-ttu-id="9b2cb-108">Die Koeffizienten der Transformationsmatrix werden auch in den \_ Zuständen D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 und D3DTSS \_ BUMPENVMAT11 Texture festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-108">The coefficients of the transformation matrix are set though the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT10, D3DTSS\_BUMPENVMAT01, and D3DTSS\_BUMPENVMAT11 texture stage states.</span></span>

<span data-ttu-id="9b2cb-109">Zusätzlich zu den Delta Werten von "You" und "v" kann das System einen leuchtwert berechnen, der zum modulieren der Farbe der Umgebungs Zuordnung in der nächsten Mischungs Stufe verwendet wird, wie in der folgenden Formel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-109">In addition to the u and v delta values, the system can compute a luminance value that it uses to modulate the color of the environment map in the next blending stage, as shown in the following formula.</span></span>

![Formel für Ausgabe Beleuchtung, berechnet von Skalierungsfaktor und Offset](images/l-transform.png)

<span data-ttu-id="9b2cb-111">In dieser Formel ist L ' die Ausgabe Helligkeit, die berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-111">In this formula, L' is the output luminance being computed.</span></span> <span data-ttu-id="9b2cb-112">Die L-Variable ist der von einem Bump-Karten Pixel ergriffene Glanz Wert, der mit dem Skalierungsfaktor multipliziert wird und dem Wert in der Variablen O entspricht. In den \_ Textur Phasen "D3DTSS bumpenvlscale" und "D3DTSS \_ bumpenvloffset" werden die Werte für die e-und O-Variablen in der Formel gesteuert.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-112">The L variable is the luminance value taken from a bump map pixel, which is multiplied by the scaling factor, S, and offset by the value in the variable O. The D3DTSS\_BUMPENVLSCALE and D3DTSS\_BUMPENVLOFFSET texture stage states control the values for the S and O variables in the formula.</span></span> <span data-ttu-id="9b2cb-113">Diese Formel wird nur angewendet, wenn der Textur Mischungs Vorgang für die Stufe, die die Bump Map enthält, auf D3DTOP \_ bumpenvmapluminance festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-113">This formula is only applied when the texture blending operation for the stage that contains the bump map is set to D3DTOP\_BUMPENVMAPLUMINANCE.</span></span> <span data-ttu-id="9b2cb-114">Bei Verwendung \_ von D3DTOP bumpenvmap verwendet das System den Wert 1,0 für L '.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-114">When using D3DTOP\_BUMPENVMAP, the system uses a value of 1.0 for L'.</span></span>

<span data-ttu-id="9b2cb-115">Nach dem Berechnen der Ausgabe Delta Werte D<sub>U</sub>' and d<sub>V</sub>' werden diese in der nächsten Textur Phase den Texturkoordinaten hinzugefügt, und die ausgewählte Farbe wird von der Leuchtkraft zur Erstellung der auf das Polygon angewendeten Farbe modusiert.</span><span class="sxs-lookup"><span data-stu-id="9b2cb-115">After computing the output delta values D<sub>U</sub>' and D<sub>V</sub>', the system adds them to the texture coordinates in the next texture stage, and modulates the chosen color by the luminance to produce the color applied to the polygon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b2cb-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b2cb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2cb-117">Bump-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9b2cb-117">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



