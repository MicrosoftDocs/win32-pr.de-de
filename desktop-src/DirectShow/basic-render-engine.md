---
description: Einfache Renderingengine
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Einfache Renderingengine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522219"
---
# <a name="basic-render-engine"></a><span data-ttu-id="24945-103">Einfache Renderingengine</span><span class="sxs-lookup"><span data-stu-id="24945-103">Basic Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="24945-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="24945-104">\[Deprecated.</span></span> <span data-ttu-id="24945-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="24945-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="24945-106">Das grundlegende Rendering-Engine-Objekt rendert eine nicht komprimierte Ausgabe aus einer Zeita</span><span class="sxs-lookup"><span data-stu-id="24945-106">The Basic Render Engine object renders uncompressed output from a timeline.</span></span> <span data-ttu-id="24945-107">Um dieses Objekt zu erstellen, rufen Sie **cokreateinstance** auf.</span><span class="sxs-lookup"><span data-stu-id="24945-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="24945-108">Verwenden Sie für die komprimierte Ausgabe die Smart-Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="24945-108">For compressed output, use the Smart Render Engine.</span></span> <span data-ttu-id="24945-109">Der Klassen Bezeichner ist CLSID- \_ Renderengine.</span><span class="sxs-lookup"><span data-stu-id="24945-109">The class identifier is CLSID\_RenderEngine.</span></span>

<span data-ttu-id="24945-110">Die einfache Renderingengine macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="24945-110">The Basic Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="24945-111">**Iameinterrorlog**</span><span class="sxs-lookup"><span data-stu-id="24945-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="24945-112">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="24945-112">IObjectWithSite</span></span>
-   [<span data-ttu-id="24945-113">**"Unenderengine"**</span><span class="sxs-lookup"><span data-stu-id="24945-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="24945-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="24945-114">**IRenderEngine2**</span></span>](irenderengine2.md)

## <a name="related-topics"></a><span data-ttu-id="24945-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24945-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24945-116">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="24945-116">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="24945-117">Smart-Rendering-Engine</span><span class="sxs-lookup"><span data-stu-id="24945-117">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> </dl>

 

 



