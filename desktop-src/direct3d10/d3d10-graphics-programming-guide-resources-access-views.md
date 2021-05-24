---
description: In Direct3D 10 wird mit einer Ansicht auf Texturressourcen zugegriffen. Dies ist ein Mechanismus für die Hardwareinterpretation einer Ressource im Arbeitsspeicher.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Texturansichten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83dd83b1a3896637ce73505de00027ea9dfadac4
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335584"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="e19c4-103">Texturansichten (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e19c4-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="e19c4-104">In Direct3D 10 wird mit einer Ansicht auf Texturressourcen zugegriffen. Dies ist ein Mechanismus für die Hardwareinterpretation einer Ressource im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e19c4-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="e19c4-105">Eine Ansicht ermöglicht einer bestimmten Pipelinephase, nur auf die [benötigten Unterressourcen](d3d10-graphics-programming-guide-resources-types.md) in der von der Anwendung gewünschten Darstellung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e19c4-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="e19c4-106">Eine Ansicht unterstützt das Konzept einer typfreien Ressource.</span><span class="sxs-lookup"><span data-stu-id="e19c4-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="e19c4-107">Eine ressource ohne Typ ist eine Ressource, die mit einer bestimmten Größe, aber nicht mit einem bestimmten Datentyp erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e19c4-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="e19c4-108">Die Daten werden dynamisch interpretiert, wenn sie an die Pipeline gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="e19c4-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="e19c4-109">Die folgende Abbildung zeigt ein Beispiel für die Bindung eines 2D-Texturarrays mit 6 Texturen als Shaderressource, indem eine Shaderressourcenansicht dafür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e19c4-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="e19c4-110">Die Ressource wird dann als Array von Texturen adressiert.</span><span class="sxs-lookup"><span data-stu-id="e19c4-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="e19c4-111">(Hinweis: Eine Unterressource kann nicht gleichzeitig als Eingabe und Ausgabe an die Pipeline gebunden werden.)</span><span class="sxs-lookup"><span data-stu-id="e19c4-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![Abbildung eines Texturarrays mit sechs Texturen](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="e19c4-113">Wenn Sie ein 2D-Texturarray als Renderziel verwenden, kann die Ressource als Array von 2D-Texturen (in diesem Beispiel 6) mit Mipmapebenen (in diesem Beispiel 3) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e19c4-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="e19c4-114">Erstellen Sie ein Ansichtsobjekt für ein Renderziel, indem Sie CreateRenderTargetView aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e19c4-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="e19c4-115">Rufen Sie dann OMSetRenderTargets auf, um die Renderzielansicht auf die Pipeline festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e19c4-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="e19c4-116">Rendern Sie in die Renderziele, indem Sie Draw aufrufen und renderTargetArrayIndex verwenden, um die richtige Textur im Array zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="e19c4-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="e19c4-117">Sie können eine Unterressource (mipmap-Ebene, Arrayindexkombination) verwenden, um eine Bindung an ein beliebiges Array von Unterressourcen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="e19c4-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="e19c4-118">Sie können also an die zweite Mipmapebene binden und diese bestimmte Mipmapebene nur aktualisieren, wenn Sie möchten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e19c4-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![Abbildung der Bindung nur an die zweite Mipmapebene eines Texturarrays](images/d3d10-cube-texture-faces-subresource.png)



<span data-ttu-id="e19c4-120">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e19c4-120">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="e19c4-121">In Direct3D 10 binden Sie eine Ressource nicht mehr direkt an die Pipeline, erstellen eine Ansicht einer Ressource und legen die Ansicht dann auf die Pipeline fest.</span><span class="sxs-lookup"><span data-stu-id="e19c4-121">In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="e19c4-122">Dies ermöglicht die Überprüfung und Zuordnung in der Laufzeit und im Treiber bei der Ansichtserstellung, wodurch die Typüberprüfung zur Bindungszeit minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="e19c4-122">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="e19c4-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e19c4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e19c4-124">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e19c4-124">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




