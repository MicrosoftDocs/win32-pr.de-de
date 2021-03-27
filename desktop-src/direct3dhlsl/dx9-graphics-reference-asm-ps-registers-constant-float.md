---
title: Konstantes float-Register (HLSL PS-Referenz)
description: Pixel-Shader-Eingabe Register für eine 4D-Gleit Komma Konstante.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390753"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Konstantes float-Register (HLSL PS-Referenz)

Pixel-Shader-Eingabe Register für eine 4D-Gleit Komma Konstante.

Sie können mithilfe von [DEF-PS](def---ps.md) oder [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)festgelegt werden.

Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu. Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt. Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren. Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel für das Deklarieren von zwei Gleit Komma Konstanten innerhalb eines Shaders.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Diese Konstanten werden jedes Mal geladen, wenn [**setpixelshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) aufgerufen wird.

Wenn Sie Konstante Werte mit der API festlegen, ist keine Shader-Deklaration erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 