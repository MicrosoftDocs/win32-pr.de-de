---
title: Schablone-Test
description: Der Schablone-Test verwirft bedingt ein Fragment basierend auf dem Ergebnis eines Vergleichs zwischen dem Wert im Schablonen Puffer und einem Verweis Wert.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- OpenGL-Verarbeitungs Pipeline, Schablone-Test
- Schablone-Test OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713931"
---
# <a name="stencil-test"></a><span data-ttu-id="1818b-105">Schablone-Test</span><span class="sxs-lookup"><span data-stu-id="1818b-105">Stencil Test</span></span>

<span data-ttu-id="1818b-106">Der Schablone-Test verwirft bedingt ein Fragment basierend auf dem Ergebnis eines Vergleichs zwischen dem Wert im Schablonen Puffer und einem Verweis Wert.</span><span class="sxs-lookup"><span data-stu-id="1818b-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="1818b-107">Die Funktion " [**glstencilfunc**](glstencilfunc.md) " gibt die Vergleichsfunktion und den Verweis Wert an.</span><span class="sxs-lookup"><span data-stu-id="1818b-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="1818b-108">Unabhängig davon, ob das Fragment den Schablonen Test übergibt oder fehlschlägt, wird der Wert im Schablonen Puffer entsprechend den in [**glstencilop**](glstencilop.md)angegebenen Anweisungen geändert.</span><span class="sxs-lookup"><span data-stu-id="1818b-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




