---
description: In Direct3D 10 erfolgt der Zugriff auf Textur Ressourcen mit einer Ansicht, bei der es sich um einen Mechanismus zur Hardware Interpretation einer Ressource im Arbeitsspeicher handelt.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Textur Sichten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06cd98a00782b826713e68304ad7cc132e4e0fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958462"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="05a1a-103">Textur Sichten (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="05a1a-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="05a1a-104">In Direct3D 10 erfolgt der Zugriff auf Textur Ressourcen mit einer Ansicht, bei der es sich um einen Mechanismus zur Hardware Interpretation einer Ressource im Arbeitsspeicher handelt.</span><span class="sxs-lookup"><span data-stu-id="05a1a-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="05a1a-105">Eine Ansicht ermöglicht es einer bestimmten Pipeline Stufe, nur auf die benötigten unter [Ressourcen](d3d10-graphics-programming-guide-resources-types.md) zuzugreifen, die in der von der Anwendung gewünschten Darstellung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="05a1a-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="05a1a-106">Eine Ansicht unterstützt das Konzept einer Ressource ohne Typ.</span><span class="sxs-lookup"><span data-stu-id="05a1a-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="05a1a-107">Eine Ressource vom Typ "less" ist eine Ressource, die mit einer bestimmten Größe erstellt wurde, jedoch nicht mit einem bestimmten Datentyp.</span><span class="sxs-lookup"><span data-stu-id="05a1a-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="05a1a-108">Die Daten werden dynamisch interpretiert, wenn Sie an die Pipeline gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="05a1a-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="05a1a-109">Die folgende Abbildung zeigt ein Beispiel für die Bindung eines 2D-Textur Arrays mit 6 Texturen als Shaderressource, indem eine Shader-Ressourcen Ansicht dafür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="05a1a-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="05a1a-110">Die Ressource wird dann als Array von Texturen adressiert.</span><span class="sxs-lookup"><span data-stu-id="05a1a-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="05a1a-111">(Hinweis: eine untergeordnete Quelle kann nicht gleichzeitig als Eingabe und Ausgabe an die Pipeline gebunden werden.)</span><span class="sxs-lookup"><span data-stu-id="05a1a-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![Abbildung eines Textur Arrays mit sechs Texturen](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="05a1a-113">Wenn ein 2D-Textur Array als Renderziel verwendet wird, kann die Ressource als Array von 2D-Texturen (in diesem Beispiel 6) mit MipMap-Ebenen (in diesem Beispiel 3) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05a1a-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="05a1a-114">Erstellen Sie ein Ansichts Objekt für ein Renderziel durch Aufrufen von createrendertargetview.</span><span class="sxs-lookup"><span data-stu-id="05a1a-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="05a1a-115">Anschließend wird omsetrendertargets aufgerufen, um die renderzielansicht auf die Pipeline festzulegen.</span><span class="sxs-lookup"><span data-stu-id="05a1a-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="05a1a-116">Rendern Sie die Renderziele, indem Sie Draw aufrufen und den rendertargetarrayindex verwenden, um die richtige Textur im Array zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="05a1a-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="05a1a-117">Sie können einen unter Bericht (eine MipMap-Ebene, Array Index Kombination) verwenden, um eine Bindung an ein beliebiges Array von unter Ressourcen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="05a1a-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="05a1a-118">Sie könnten also an die zweite MipMap-Ebene binden und diese bestimmte MipMap-Ebene nur aktualisieren, wenn Sie möchten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05a1a-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![Darstellung der Bindung nur an die zweite MipMap-Ebene eines Textur Arrays](images/d3d10-cube-texture-faces-subresource.png)



|                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a1a-120">Unterschiede zwischen Direct3D 9 und Direct3D 10: in Direct3D 10 binden Sie eine Ressource nicht mehr direkt an die Pipeline, sondern erstellen eine Ansicht einer Ressource und legen dann die Ansicht auf die Pipeline fest.</span><span class="sxs-lookup"><span data-stu-id="05a1a-120">Differences between Direct3D 9 and Direct3D 10: In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="05a1a-121">Dies ermöglicht die Validierung und Zuordnung in der Laufzeit und im Treiber bei der Ansichts Erstellung, wodurch die Typüberprüfung zur Bindungs Zeit minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="05a1a-121">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="05a1a-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05a1a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05a1a-123">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="05a1a-123">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




