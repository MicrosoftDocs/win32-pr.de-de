---
description: Ein Shader, der aufgerufen wird, wenn keine Ray-Schnittmengen gefunden oder akzeptiert werden.
ms.assetid: ''
title: Miss-Shader
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343017"
---
# <a name="miss-shader"></a><span data-ttu-id="51642-103">Miss-Shader</span><span class="sxs-lookup"><span data-stu-id="51642-103">Miss Shader</span></span>

<span data-ttu-id="51642-104">Ein Shader, der aufgerufen wird, wenn keine Ray-Schnittmengen gefunden oder akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="51642-104">A shader that is invoked when no ray intersections are found or accepted.</span></span> <span data-ttu-id="51642-105">Dies ist nützlich für die Hintergrund-oder Himmel Schattierung.</span><span class="sxs-lookup"><span data-stu-id="51642-105">This is useful for background or sky shading.</span></span>  <span data-ttu-id="51642-106">Der übersehen-Shader kann [**callshader**](callshader-function.md) und **traceray** verwenden, um mehr Arbeit zu planen.</span><span class="sxs-lookup"><span data-stu-id="51642-106">The miss shader may use [**CallShader**](callshader-function.md) and **TraceRay** to schedule more work.</span></span>

<span data-ttu-id="51642-107">Der Miss-Shader muss einen mit einer benutzerdefinierten Struktur typisierten Nutz Last Parameter einschließen, der mit dem für [**traceray**](traceray-function.md)angegebenen Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="51642-107">The miss shader must include a user-defined structure typed payload parameter matching the one supplied to [**TraceRay**](traceray-function.md).</span></span>


## <a name="shader-type-attribute"></a><span data-ttu-id="51642-108">Shader Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="51642-108">Shader Type attribute</span></span>


```
[shader("miss")]
```



## <a name="example"></a><span data-ttu-id="51642-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="51642-109">Example</span></span>

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




