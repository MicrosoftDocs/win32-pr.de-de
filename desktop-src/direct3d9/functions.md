---
description: Eine Funktion ist der Baustein für einen Shader, der in der Sprache auf hoher Ebene erstellt wird. Wenn Sie Shader lieber in einer Sprache im C-Stil schreiben möchten, anstatt Sie in der Assemblysprache zu verwenden, sollten Sie Funktionen schreiben.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Effekt Funktions Syntax (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520907"
---
# <a name="effect-function-syntax-direct3d-9"></a>Effekt Funktions Syntax (Direct3D 9)

Eine Funktion ist der Baustein für einen Shader, der in der Sprache auf hoher Ebene erstellt wird. Wenn Sie Shader lieber in einer Sprache im C-Stil schreiben möchten, anstatt Sie in der Assemblysprache zu verwenden, sollten Sie Funktionen schreiben.

## <a name="syntax"></a>Syntax


```
type id ( [ parameters ] )  
    { body }
```



Funktionen ändern die Parameterwerte nicht in einem Effekt.

-   Type: ein beliebiger gültiger [Verweis für den HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) -Typ.
-   ID: ein eindeutiger Name.
-   Parameter-Funktionsparameter.
-   Body: der Hauptteil der Funktion.

Funktionen werden aus der Sprache auf hoher Ebene erstellt. Weitere Informationen finden Sie unter [Referenz für HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
