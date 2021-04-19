---
description: Die Validierung wird während der Kompilierung durchgeführt. Um das aktuelle Verfahren zu überprüfen, geben Sie NULL als Technik Handle an, das überprüft werden soll.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validierung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345586"
---
# <a name="validation-direct3d-9"></a><span data-ttu-id="3563a-104">Validierung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3563a-104">Validation (Direct3D 9)</span></span>

<span data-ttu-id="3563a-105">Die Validierung wird während der Kompilierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3563a-105">Validation is performed during the effect compile.</span></span> <span data-ttu-id="3563a-106">Um das aktuelle Verfahren zu überprüfen, geben Sie **null** als Technik Handle an, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="3563a-106">To validate the current technique, specify **NULL** as the technique handle to be validated.</span></span>

<span data-ttu-id="3563a-107">Die Überprüfung kann für folgende Aktionen nicht ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="3563a-107">Validation will fail for any of the following:</span></span>

-   <span data-ttu-id="3563a-108">, Wenn das angegebene Techniken Handle nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3563a-108">If the specified technique handle does not exist.</span></span>
-   <span data-ttu-id="3563a-109">Wenn die Anwendung eines beliebigen Zustands in einem beliebigen Schritt der Technik fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="3563a-109">If the application of any state in any pass of the technique fails.</span></span>
-   <span data-ttu-id="3563a-110">, Wenn die Gerätevalidierung nach der Anwendung aller Zustände in einem beliebigen Schritt der Technik fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="3563a-110">If device validation fails after the application of all the states in any pass of the technique.</span></span>
-   <span data-ttu-id="3563a-111">Wenn dem Pixelshader-oder dem Vertexshader-Effekt Status bei jedem Durchlauf der Technik ungültige Shader zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3563a-111">If the PIXELSHADER or VERTEXSHADER effect states are assigned invalid shaders in any pass of the technique.</span></span>
-   <span data-ttu-id="3563a-112">Wenn die Geräte Obergrenzen die cubezuordnung nicht unterstützen, und einem textureffekt Zustand wird ein Wert des Typs "texturecube" bei jedem Durchlauf der Technik zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3563a-112">If the device caps do not support cube mapping, and a TEXTURE effect state is assigned a value of type textureCUBE in any pass of the technique.</span></span>
-   <span data-ttu-id="3563a-113">Wenn die Geräte Obergrenzen die volumezuordnung nicht unterstützen und in jedem Durchlauf der Technik ein Wert vom Typ texture3D zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3563a-113">If the device caps do not support volume mapping and a TEXTURE effect state is assigned a value of type texture3D in any pass of the technique.</span></span>

<span data-ttu-id="3563a-114">Weitere Informationen finden Sie unter [Effect States (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="3563a-114">For more information, see [Effect States (Direct3D 9)](effect-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3563a-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3563a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3563a-116">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="3563a-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



