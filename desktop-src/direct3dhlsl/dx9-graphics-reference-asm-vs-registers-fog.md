---
title: Nebelregister
description: Dieses Vertex-Shader-Ausgabe Register enthält eine pro-Scheitelpunkt-Nebelfarbe.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976104"
---
# <a name="fog-register"></a><span data-ttu-id="ce474-103">Nebelregister</span><span class="sxs-lookup"><span data-stu-id="ce474-103">Fog Register</span></span>

<span data-ttu-id="ce474-104">Dieses Vertex-Shader-Ausgabe Register enthält eine pro-Scheitelpunkt-Nebelfarbe.</span><span class="sxs-lookup"><span data-stu-id="ce474-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="ce474-105">Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.</span><span class="sxs-lookup"><span data-stu-id="ce474-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="ce474-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce474-106">Property</span></span>        | <span data-ttu-id="ce474-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce474-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce474-108">Name</span><span class="sxs-lookup"><span data-stu-id="ce474-108">Name</span></span>            | <span data-ttu-id="ce474-109">onebel</span><span class="sxs-lookup"><span data-stu-id="ce474-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="ce474-110">Anzahl</span><span class="sxs-lookup"><span data-stu-id="ce474-110">Count</span></span>           | <span data-ttu-id="ce474-111">Ein Vektor, von dem nur eine Komponente verwendet werden kann und die von der Komponenten Maske angegeben werden muss</span><span class="sxs-lookup"><span data-stu-id="ce474-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="ce474-112">E/a-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ce474-112">I/O permissions</span></span> | <span data-ttu-id="ce474-113">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ce474-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="ce474-114">Der Ausgabe Nebel Wert wird registriert.</span><span class="sxs-lookup"><span data-stu-id="ce474-114">The output fog value registers.</span></span> <span data-ttu-id="ce474-115">Der Wert ist der zu interinterdende Nebel Faktor und wird dann an die Tabelle mit den Nebel geroutet.</span><span class="sxs-lookup"><span data-stu-id="ce474-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="ce474-116">Es wird nur die skalarx-Komponente des Nebels verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce474-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce474-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce474-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce474-118">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="ce474-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




