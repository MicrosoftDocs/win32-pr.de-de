---
title: Konstantes boolesches Register (HLSL vs-Referenz)
description: Dieses Register ist eine Auflistung von Bits, die in statischen Fluss Steuerungs Anweisungen verwendet werden (z. b. if bool-vs-else-vs-endif-vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976752"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a>Konstantes boolesches Register (HLSL vs-Referenz)

Bei diesem Register handelt es sich um eine Auflistung von Bits, die in statischen Fluss Steuerungs Anweisungen verwendet werden (z. [b. bei "bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [EndIf-vs](endif---vs.md)"). Es gibt 16 von Ihnen. Daher kann ein Shader 16 unabhängige Verzweigungs Bedingungen haben. Sie können mithilfe von [DEFB-vs](defb---vs.md) oder [**setvertexshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)festgelegt werden.

Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu. Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt. Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren. Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 