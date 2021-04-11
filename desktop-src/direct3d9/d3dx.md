---
description: D3DX ist eine Bibliothek von Tools, die für die Bereitstellung zusätzlicher Grafikfunktionen zusätzlich zu Direct3D konzipiert ist. D3DX wird als Dynamic Link Library (dll) bereitgestellt.
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342209"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="69098-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="69098-104">D3DX (Direct3D 9)</span></span>

<span data-ttu-id="69098-105">D3DX ist eine Bibliothek von Tools, die für die Bereitstellung zusätzlicher Grafikfunktionen zusätzlich zu Direct3D konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="69098-105">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="69098-106">D3DX wird als Dynamic Link Library (dll) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="69098-106">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="69098-107">In dieser Version des DirectX SDK wird nur eine Version von D3DX bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="69098-107">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="69098-108">Die Retail D3DX-dll ist in der verteilbaren Datei enthalten, die im SDK bereitgestellt wird, und wird automatisch als Teil der [Installation von DirectX mit DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx)installiert.</span><span class="sxs-lookup"><span data-stu-id="69098-108">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span></span> <span data-ttu-id="69098-109">Die in dieser Version enthaltene D3DX-Bibliothek ist abhängig von den Direct3D-Laufzeiten, die mit diesem SDK ausgeliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="69098-109">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="69098-110">Anwendungen, die mit der Version von D3DX in dieser Version verknüpft sind, müssen auch die Laufzeit von diesem SDK verteilen.</span><span class="sxs-lookup"><span data-stu-id="69098-110">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="69098-111">Mehrere Versionen von D3DX können sich unabhängig voneinander auf einem einzelnen System befinden.</span><span class="sxs-lookup"><span data-stu-id="69098-111">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="69098-112">Wenn eine Anwendung statisch mit D3dx9. lib verknüpft wird, wird die Anwendung dynamisch zur Laufzeit mit der entsprechenden D3DX-dll für den Einzelhandel verknüpft.</span><span class="sxs-lookup"><span data-stu-id="69098-112">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="69098-113">Diese DLL entspricht den D3DX-Headern, mit denen die Anwendung kompiliert wird (mit der D3DX \_ SDK- \_ Versions Konstante in D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="69098-113">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="69098-114">Wenn neue Versionen von D3DX in zukünftigen Versionen des DirectX SDK ausgeliefert werden, bleiben Anwendungen, die mit früheren D3DX-Bibliotheken verknüpft sind, unverändert.</span><span class="sxs-lookup"><span data-stu-id="69098-114">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="69098-115">Die D3DX-Bibliothek behandelt diese allgemeinen Funktionsbereiche:</span><span class="sxs-lookup"><span data-stu-id="69098-115">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="69098-116">Zeilen Zeichnungs Unterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="69098-116">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="69098-117">Gitter Unterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="69098-117">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="69098-118">Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="69098-118">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="69098-119">Textur Unterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="69098-119">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="69098-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69098-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69098-121">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="69098-121">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



