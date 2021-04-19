---
title: Ray-Nutz Last Struktur
description: Eine benutzerdefinierte Struktur, die als ein INOUT-Argument in einem traceray-Befehl bereitgestellt wird, und als INOUT-Parameter in den shadertypen, die möglicherweise auf die Ray-Nutzlast zugreifen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106363830"
---
# <a name="ray-payload-structure"></a><span data-ttu-id="aef78-103">Ray-Nutz Last Struktur</span><span class="sxs-lookup"><span data-stu-id="aef78-103">Ray payload structure</span></span> 

<span data-ttu-id="aef78-104">Eine benutzerdefinierte Struktur, die als ein INOUT-Argument in einem [**traceray**](traceray-function.md) -Befehl bereitgestellt wird, und als INOUT-Parameter in den shadertypen, die möglicherweise auf die Ray-Nutzlast zugreifen, einschließlich [Treffer](any-hit-shader.md), [nächster Treffer](closest-hit-shader.md)und [fehlshader](miss-shader.md) .</span><span class="sxs-lookup"><span data-stu-id="aef78-104">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload, which include [any hit](any-hit-shader.md), [closest hit](closest-hit-shader.md), and [miss](miss-shader.md) shaders.</span></span> <span data-ttu-id="aef78-105">Alle Shader, die auf die Ray-Nutzlast zugreifen, müssen dieselbe Struktur wie die des ursprünglichen **traceray** -Aufrufes verwenden.</span><span class="sxs-lookup"><span data-stu-id="aef78-105">Any shaders that access the ray payload must use the same structure as the one provided at the originating **TraceRay** call.</span></span>  <span data-ttu-id="aef78-106">Auch wenn einer dieser Shader überhaupt nicht auf die Ray-Nutzlast verweist, muss er trotzdem die passende Nutzlast als ursprünglichen **traceray** -Aufrufwert angeben.</span><span class="sxs-lookup"><span data-stu-id="aef78-106">Even if one of these shaders doesn’t reference the ray payload at all, it still must specify the matching payload as the originating **TraceRay** call.</span></span>

