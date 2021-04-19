---
description: Ein Shader, der von einem anderen Shader mit der systeminternen Funktion callshader aufgerufen wird.
ms.assetid: ''
title: Callable-Shader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346629"
---
# <a name="callable-shader"></a><span data-ttu-id="50dbc-103">Callable-Shader</span><span class="sxs-lookup"><span data-stu-id="50dbc-103">Callable Shader</span></span>

<span data-ttu-id="50dbc-104">Ein Shader, der von einem anderen Shader mit der systeminternen Funktion [**callshader**](callshader-function.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50dbc-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="50dbc-105">An der **callshader** -Aufruf Site wird eine Parameter Struktur bereitgestellt, die der in dem Aufruf baren Shader verwendeten Parameter Struktur entsprechen muss, auf die der angeforderte Index in die Aufruf Bare shadertabelle verweist, die durch die [**dispatchrays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) -Methode bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50dbc-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="50dbc-106">Der Aufruf Bare Shader muss diesen Parameter als *INOUT* deklarieren.</span><span class="sxs-lookup"><span data-stu-id="50dbc-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="50dbc-107">Außerdem kann der Aufruf Bare Shader Start Index und Dimensions Eingaben lesen.</span><span class="sxs-lookup"><span data-stu-id="50dbc-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="50dbc-108">Weitere Informationen finden Sie unter [**System eigene System Wert**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md)Funktionen.</span><span class="sxs-lookup"><span data-stu-id="50dbc-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="50dbc-109">Shader Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="50dbc-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="50dbc-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="50dbc-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




