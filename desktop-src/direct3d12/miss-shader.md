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
# <a name="miss-shader"></a>Miss-Shader

Ein Shader, der aufgerufen wird, wenn keine Ray-Schnittmengen gefunden oder akzeptiert werden. Dies ist nützlich für die Hintergrund-oder Himmel Schattierung.  Der übersehen-Shader kann [**callshader**](callshader-function.md) und **traceray** verwenden, um mehr Arbeit zu planen.

Der Miss-Shader muss einen mit einer benutzerdefinierten Struktur typisierten Nutz Last Parameter einschließen, der mit dem für [**traceray**](traceray-function.md)angegebenen Parameter übereinstimmt.


## <a name="shader-type-attribute"></a>Shader Type-Attribut


```
[shader("miss")]
```



## <a name="example"></a>Beispiel

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

 

 




