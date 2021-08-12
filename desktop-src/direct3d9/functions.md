---
description: Eine Funktion ist der Baustein für einen Shader, der in der übergeordneten Sprache erstellt wurde. Wenn Sie Shader lieber in einer Sprache im C-Stil statt in der Assemblysprache schreiben möchten, sollten Sie Funktionen schreiben.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Effect-Funktionssyntax (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9de680f2f892e59f49e1dfd0850a128ca9ba34e2588e416059251d5058c44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297108"
---
# <a name="effect-function-syntax-direct3d-9"></a>Effect-Funktionssyntax (Direct3D 9)

Eine Funktion ist der Baustein für einen Shader, der in der übergeordneten Sprache erstellt wurde. Wenn Sie Shader lieber in einer Sprache im C-Stil statt in der Assemblysprache schreiben möchten, sollten Sie Funktionen schreiben.

## <a name="syntax"></a>Syntax


```
type id ( [ parameters ] )  
    { body }
```



Funktionen ändern keine Parameterwerte in einem Effekt.

-   type: Ein beliebiger gültiger [Verweis für den HLSL-Typ.](../direct3dhlsl/dx-graphics-hlsl-reference.md)
-   id: Ein eindeutiger Name.
-   parameters: Funktionsparameter.
-   body: Der Text der Funktion.

Funktionen werden aus der übergeordneten Sprache erstellt. Weitere Informationen finden Sie [unter Referenz für HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
