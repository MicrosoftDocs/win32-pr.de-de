---
description: Die Bump-Zuordnung ist eine spezielle Form der Glanz-oder diffusen Umgebungs Zuordnung, die die Reflektionen von fein Mosaik Objekten simuliert, ohne dass extrem hohe Polygon Zahlen erforderlich sind.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Bump-Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127389"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="ff147-103">Bump-Zuordnung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ff147-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="ff147-104">Die Bump-Zuordnung ist eine spezielle Form der Glanz-oder diffusen Umgebungs Zuordnung, die die Reflektionen von fein Mosaik Objekten simuliert, ohne dass extrem hohe Polygon Zahlen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ff147-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="ff147-105">Die von Direct3D implementierte Bump-Zuordnung kann genau als Pixel übergreifende Textur Koordinate für Glanz-oder diffuse Umgebungs Zuordnungen beschrieben werden, da Sie Informationen über die Kontur der Bump Map in Bezug auf Delta Werte bereitstellen, die das System für die Texturkoordinaten eines Umgebungs Diagramms in der nächsten Textur Phase anwendet.</span><span class="sxs-lookup"><span data-stu-id="ff147-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="ff147-106">Die Delta Werte werden im Pixel Format der Bump Map-Oberfläche codiert (Weitere Informationen finden Sie unter [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span><span class="sxs-lookup"><span data-stu-id="ff147-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="ff147-107">Die Bump-Zuordnung basiert auf der Mischung mehrerer Texturen.</span><span class="sxs-lookup"><span data-stu-id="ff147-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="ff147-108">Dies bedeutet, dass das Gerät mindestens zwei Mischungs Phasen unterstützen muss. eine für die Bump Map und eine für eine Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ff147-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="ff147-109">Mindestens drei Textur Mischungs Phasen sind erforderlich, um eine zusätzliche Basis Textur Zuordnung anzuwenden. Dies ist der häufigste Fall.</span><span class="sxs-lookup"><span data-stu-id="ff147-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="ff147-110">Im folgenden Diagramm werden die Beziehungen zwischen der Basis Textur, der Bump Map und der Umgebungs Zuordnung in der Textur Mischungs kaskadieren angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff147-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![Diagramm der Textur Mischungs kaskadieren](images/bumpmap-tcascade.png)

<span data-ttu-id="ff147-112">Sie müssen die Textur Stufen entsprechend vorbereiten, um die Bump-Zuordnung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ff147-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="ff147-113">In den folgenden Themen wird die Bump-Zuordnung eingeführt, und es wird erläutert, wie Sie Sie in Ihren Anwendungen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="ff147-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="ff147-114">Peermap-Pixel Formate</span><span class="sxs-lookup"><span data-stu-id="ff147-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="ff147-115">Bump-Mapping-Formeln</span><span class="sxs-lookup"><span data-stu-id="ff147-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="ff147-116">Verwenden der Bump-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="ff147-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="ff147-117">Direct3D bietet keine Unterstützung für Höhen Zuordnungen. Sie sind lediglich ein nützliches Format, in dem Sie die Konturdaten speichern und visualisieren können.</span><span class="sxs-lookup"><span data-stu-id="ff147-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="ff147-118">In Ihrer Anwendung können Sie die Informationen in einem beliebigen Format speichern oder sogar eine prozedurale Bump Map generieren.</span><span class="sxs-lookup"><span data-stu-id="ff147-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff147-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff147-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff147-120">Pixel Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff147-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



