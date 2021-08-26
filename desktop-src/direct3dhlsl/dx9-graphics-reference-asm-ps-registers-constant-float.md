---
title: Constant float register (HLSL PS-Referenz)
description: Pixel-Shader-Eingaberegister für eine 4D-Gleitkommakonstige.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 025c7e7609e7e0d19c15dfa24e27b9f174114e9287a9e09d01d2436b4ef2ef8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982850"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Constant float register (HLSL PS-Referenz)

Pixel-Shader-Eingaberegister für eine 4D-Gleitkommakonstige.

Sie können mit def - [ps oder](def---ps.md) [**SetPixelShaderConstantF festgelegt werden.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

Das Verhalten von Shaderkonst constants hat sich zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen konstanten Konstanten, die mit defx festgelegt wurden, Werte dem konstanten Shaderraum zu. Die Lebensdauer einer mit defx deklarierten Konstante ist auf die Ausführung dieses Shaders beschränkt. Umgekehrt initialisieren Konstanten, die mithilfe der APIs SetXXXShaderConstantX festgelegt werden, Konstanten im globalen Raum. Konstanten im globalen Raum werden erst dann in den lokalen Raum kopiert (für den Shader sichtbar), wenn SetxxxShaderConstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt wurden, Werte dem konstanten Shaderraum zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von der Technik, mit der sie festgelegt wurden.

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel, in dem zwei Gleitkommakonst constants innerhalb eines Shaders deklariert werden.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Diese Konstanten werden jedes Mal geladen, wenn [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) aufgerufen wird.

Wenn Sie konstante Werte mit der API festlegen, ist keine Shaderdeklaration erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 