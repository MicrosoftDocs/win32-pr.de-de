---
description: Wird in einem beliebigen Treffer-Shader verwendet, um einen Commit für den aktuellen Treffer durchzusetzen und dann nach weiteren Treffern für den Strahl zu suchen.
ms.assetid: ''
title: AcceptHitAndEndSearch-Funktion
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343604"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="afaca-103">AcceptHitAndEndSearch-Funktion</span><span class="sxs-lookup"><span data-stu-id="afaca-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="afaca-104">Wird in einem [beliebigen Treffer-Shader](any-hit-shader.md) verwendet, um einen Commit für den aktuellen Treffer durchzusetzen und dann nach weiteren Treffern für den Strahl zu suchen.</span><span class="sxs-lookup"><span data-stu-id="afaca-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="afaca-105">Wenn ein Schnittstellen-Shader ausgeführt wird, wird die Ausführung angehalten.</span><span class="sxs-lookup"><span data-stu-id="afaca-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="afaca-106">Die Ausführung wird an den [nächstgelegenen Treffer-Shader](closest-hit-shader.md)weitergeleitet, sofern diese aktiviert ist, und der nächstgelegene Treffer wurde bisher aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="afaca-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="afaca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="afaca-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="afaca-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afaca-108">Return Value</span></span>

<span data-ttu-id="afaca-109">**void**</span><span class="sxs-lookup"><span data-stu-id="afaca-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="afaca-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afaca-110">Remarks</span></span>

<span data-ttu-id="afaca-111">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="afaca-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="afaca-112">**Callable-Shader**</span><span class="sxs-lookup"><span data-stu-id="afaca-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="afaca-113">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="afaca-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="afaca-114">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="afaca-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="afaca-115">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="afaca-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="afaca-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afaca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afaca-117">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="afaca-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




