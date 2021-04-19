---
description: Ein Effekt wird erstellt, indem er in das Effects-Framework geladen wird.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Erstellen eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346843"
---
# <a name="create-an-effect-direct3d-10"></a>Erstellen eines Effekts (Direct3D 10)

Ein Effekt wird erstellt, indem er in das Effects-Framework geladen wird. Wenn der Effekt noch nie kompiliert wurde, wird er kompiliert, wenn er erstellt wird. Effekte, die bereits in den Arbeitsspeicher geladen wurden, können durch Aufrufen von [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)erstellt werden. Im folgenden Codebeispiel wird [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) verwendet, um einen Effekt aus einer Datei zu erstellen.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



Das Lesen eines Effekts erfordert dieselben Parameter wie das Kompilieren eines Effekts sowie eines Geräts und eines Pools.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



