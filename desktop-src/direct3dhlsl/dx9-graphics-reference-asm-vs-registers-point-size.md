---
title: Punktgröße registrieren
description: Dieses Vertex-Shader-Ausgabe Register enthält Daten pro Scheitelpunkt Größe.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388219"
---
# <a name="point-size-register"></a><span data-ttu-id="888b1-103">Punktgröße registrieren</span><span class="sxs-lookup"><span data-stu-id="888b1-103">Point Size Register</span></span>

<span data-ttu-id="888b1-104">Dieses Vertex-Shader-Ausgabe Register enthält Daten pro Scheitelpunkt Größe.</span><span class="sxs-lookup"><span data-stu-id="888b1-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="888b1-105">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="888b1-105">Vertex shader versions</span></span> | <span data-ttu-id="888b1-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="888b1-106">1\_1</span></span> | <span data-ttu-id="888b1-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="888b1-107">2\_0</span></span> | <span data-ttu-id="888b1-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="888b1-108">2\_sw</span></span> | <span data-ttu-id="888b1-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="888b1-109">2\_x</span></span> | <span data-ttu-id="888b1-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="888b1-110">3\_0</span></span> | <span data-ttu-id="888b1-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="888b1-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="888b1-112">Punktgröße registrieren</span><span class="sxs-lookup"><span data-stu-id="888b1-112">Point Size Register</span></span>    | <span data-ttu-id="888b1-113">x</span><span class="sxs-lookup"><span data-stu-id="888b1-113">x</span></span>    | <span data-ttu-id="888b1-114">x</span><span class="sxs-lookup"><span data-stu-id="888b1-114">x</span></span>    | <span data-ttu-id="888b1-115">x</span><span class="sxs-lookup"><span data-stu-id="888b1-115">x</span></span>     | <span data-ttu-id="888b1-116">x</span><span class="sxs-lookup"><span data-stu-id="888b1-116">x</span></span>    | <span data-ttu-id="888b1-117">x</span><span class="sxs-lookup"><span data-stu-id="888b1-117">x</span></span>    | <span data-ttu-id="888b1-118">x</span><span class="sxs-lookup"><span data-stu-id="888b1-118">x</span></span>     |



 

<span data-ttu-id="888b1-119">Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.</span><span class="sxs-lookup"><span data-stu-id="888b1-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="888b1-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="888b1-120">Property</span></span>        | <span data-ttu-id="888b1-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="888b1-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="888b1-122">Name</span><span class="sxs-lookup"><span data-stu-id="888b1-122">Name</span></span>            | <span data-ttu-id="888b1-123">oPts</span><span class="sxs-lookup"><span data-stu-id="888b1-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="888b1-124">Anzahl</span><span class="sxs-lookup"><span data-stu-id="888b1-124">Count</span></span>           | <span data-ttu-id="888b1-125">1 Vektor, von dem nur eine Komponente verwendet werden kann und die von der Komponenten Maske angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="888b1-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="888b1-126">E/a-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="888b1-126">I/O permissions</span></span> | <span data-ttu-id="888b1-127">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="888b1-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="888b1-128">Es wird nur die skalare x-Komponente der Punktgröße verwendet.</span><span class="sxs-lookup"><span data-stu-id="888b1-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="888b1-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="888b1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="888b1-130">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="888b1-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




