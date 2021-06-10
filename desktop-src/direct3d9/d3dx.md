---
description: D3DX ist eine Bibliothek von Tools, die zusätzlich zu Direct3D zusätzliche Grafikfunktionen bereitstellen. D3DX wird als Dynamic Link Library (DLL) bereitgestellt.
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910245"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="d4e73-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4e73-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="d4e73-105">Die D3DX-Bibliothek ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4e73-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="d4e73-106">Wenn ein Upgrade auf eine neuere Version von Direct3D und zugeordneter Hilfsprogrammcode keine Option ist, können Sie das NuGet-Paket [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) verwenden, anstatt sich auf das ältere DirectX SDK oder DirectSetup zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="d4e73-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="d4e73-107">D3DX ist eine Bibliothek von Tools, die zusätzlich zu Direct3D zusätzliche Grafikfunktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d4e73-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="d4e73-108">D3DX wird als Dynamic Link Library (DLL) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d4e73-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="d4e73-109">In dieser Version des DirectX SDK wird nur eine Version von D3DX bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d4e73-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="d4e73-110">Die D3DX-Einzelhandels-DLL ist in der im SDK bereitgestellten redistributable-Datei enthalten und wird automatisch im Rahmen der Installation von **DirectX mit DirectSetup** installiert.</span><span class="sxs-lookup"><span data-stu-id="d4e73-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="d4e73-111">Die in diesem Release enthaltene D3DX-Bibliothek ist von den Direct3D-Runtimes abhängig, die mit diesem SDK ausgeliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="d4e73-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="d4e73-112">Anwendungen, die mit der D3DX-Version in diesem Release verknüpft sind, müssen auch die Runtime aus diesem SDK neu verteilen.</span><span class="sxs-lookup"><span data-stu-id="d4e73-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="d4e73-113">Mehrere Releases von D3DX können sich unabhängig voneinander gleichzeitig auf einem einzelnen System befinden.</span><span class="sxs-lookup"><span data-stu-id="d4e73-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="d4e73-114">Durch statisches Verknüpfen einer Anwendung mit D3dx9.lib wird die Anwendung zur Laufzeit dynamisch mit der entsprechenden D3DX-Einzelhandels-DLL verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d4e73-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="d4e73-115">Diese DLL entspricht den D3DX-Headern, für die die Anwendung kompiliert wird (benannt mit der VERSION-Konstante des D3DX \_ SDK \_ in D3dx9core.h).</span><span class="sxs-lookup"><span data-stu-id="d4e73-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="d4e73-116">Da neue Versionen von D3DX in zukünftigen Versionen des DirectX SDK ausgeliefert werden, bleiben Anwendungen, die mit früheren D3DX-Bibliotheken verknüpft sind, nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="d4e73-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="d4e73-117">Die D3DX-Bibliothek behandelt diese allgemeinen Funktionsbereiche:</span><span class="sxs-lookup"><span data-stu-id="d4e73-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="d4e73-118">Unterstützung für Strichzeichnungen in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4e73-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="d4e73-119">Mesh-Unterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4e73-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="d4e73-120">Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4e73-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="d4e73-121">Texturunterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4e73-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="d4e73-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4e73-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4e73-123">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="d4e73-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



