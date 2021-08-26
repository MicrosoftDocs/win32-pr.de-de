---
title: Constant Integer Register (HLSL VS-Referenz)
description: Konstanten-Ganzzahlregister werden nur von Schleifen verwendet – vs. rep – vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b46390303b2ee3aae2243f25d2a5a76385b9e9dd275c2952e8aa93e18f999e9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949900"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Constant Integer Register (HLSL VS-Referenz)

Konstanten-Ganzzahlregister werden nur von [schleifenbasierten Registern (vs.](loop---vs.md) [und rep) im Vergleich zu verwendet.](rep---vs.md)

Sie können mit [defi](defi---vs.md) - vs oder [**SetVertexShaderConstantI festgelegt werden.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)

Bei Verwendung als Argument für die [Schleife – vs-Anweisung:](loop---vs.md)

-   .x ist die Iterationsanzahl. ([rep - vs verwendet](rep---vs.md) nur diese Komponente).
-   .y ist der Anfangswert für den Schleifenzähler.
-   .z ist der Inkrementschritt für den Schleifenzähler.

Das Verhalten von Shaderkonst constants hat sich zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen konstanten Konstanten, die mit defx festgelegt wurden, Werte dem konstanten Shaderraum zu. Die Lebensdauer einer mit defx deklarierten Konstante ist auf die Ausführung dieses Shaders beschränkt. Umgekehrt initialisieren Konstanten, die mithilfe der APIs SetXXXShaderConstantX festgelegt werden, Konstanten im globalen Raum. Konstanten im globalen Raum werden erst dann in den lokalen Raum kopiert (für den Shader sichtbar), wenn SetxxxShaderConstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt wurden, Werte dem konstanten Shaderraum zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von der Technik, mit der sie festgelegt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 