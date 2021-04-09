---
description: Klonen und freigeben (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Klonen und freigeben (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861631"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="ef92e-103">Klonen und freigeben (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ef92e-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="ef92e-104">Klonen von Parametern</span><span class="sxs-lookup"><span data-stu-id="ef92e-104">Cloning Parameters</span></span>

<span data-ttu-id="ef92e-105">Für das Klonen gelten die folgenden Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ef92e-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="ef92e-106">Klone erben den ursprünglichen Effekt Pool.</span><span class="sxs-lookup"><span data-stu-id="ef92e-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="ef92e-107">Weitere Informationen finden Sie im Abschnitt Freigabe Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef92e-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="ef92e-108">Klone erben die Techniken, Pass, Parameter und Anmerkungen des ursprünglichen Effekts (einschließlich aller Anmerkungen, die mit [**ID3DXEffect**](id3dxeffect.md)hinzugefügt wurden).</span><span class="sxs-lookup"><span data-stu-id="ef92e-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="ef92e-109">Klone erben die dynamisch hinzugefügten Anmerkungen des ursprünglichen Effekts.</span><span class="sxs-lookup"><span data-stu-id="ef92e-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="ef92e-110">Das Klonen auf einem neuen Gerät schlägt fehl, wenn der Pool des ursprünglichen Effekts nicht **null** war und der ursprüngliche Effekt einen freigegebenen geräteabhängigen Parameter enthielt (z. b. eine Textur oder ein Shader).</span><span class="sxs-lookup"><span data-stu-id="ef92e-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="ef92e-111">Freigabe Parameter</span><span class="sxs-lookup"><span data-stu-id="ef92e-111">Sharing Parameters</span></span>

<span data-ttu-id="ef92e-112">Ein Pool ist ein Puffer, der Effektparameter zwischen unterschiedlichen Effekten freigibt.</span><span class="sxs-lookup"><span data-stu-id="ef92e-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="ef92e-113">Zum Hinzufügen von Parametern zu einem Pool geben Sie eine freigegebene Verwendung an, wenn der Effekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef92e-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="ef92e-114">Für einen Pool gelten die folgenden Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ef92e-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="ef92e-115">Dem Pool wird ein Parameter hinzugefügt, wenn dem Pool das erste Mal ein Effekt hinzugefügt wird, der diesen Parameter (Shared) enthält.</span><span class="sxs-lookup"><span data-stu-id="ef92e-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="ef92e-116">Ein Pool ruft Anfangswerte aus dem ersten freigegebenen Parameter ab. Parameter, die anschließend freigegeben werden, erhalten ihre Werte aus dem Pool.</span><span class="sxs-lookup"><span data-stu-id="ef92e-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="ef92e-117">Ein Parameter wird aus dem Pool gelöscht, wenn alle Auswirkung-Verweise auf den freigegebenen Parameter freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef92e-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="ef92e-118">Alle Effekte im Pool, die denselben (gemeinsam genutzten) geräteabhängigen Parameter enthalten, müssen das gleiche Gerät aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ef92e-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="ef92e-119">**Null** kann verwendet werden, um keinen Pool anzugeben. in diesem Fall werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ef92e-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="ef92e-120">Dies entspricht fast der Angabe eines eindeutigen Pools nur für diesen Effekt.</span><span class="sxs-lookup"><span data-stu-id="ef92e-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="ef92e-121">Der einzige Unterschied besteht darin, dass der Klon seine freigegebenen Parameter nicht mit dem Original gemeinsam verwendet, wenn der Effekt geklont wird.</span><span class="sxs-lookup"><span data-stu-id="ef92e-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef92e-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef92e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef92e-123">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="ef92e-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



