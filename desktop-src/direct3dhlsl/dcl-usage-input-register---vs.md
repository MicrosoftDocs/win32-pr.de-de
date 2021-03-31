---
title: dcl_usage Eingabe (SM1, SM2, SM3-vs ASM)
description: Deklarieren Sie die Zuordnung zwischen einer Vertex-Element Verwendung und einem Verwendungs Index für ein Vertex-Shader-Eingabe Register.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473533"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>DCL- \_ Verwendungs Eingabe (SM1, SM2, SM3-vs ASM)

Deklarieren Sie die Zuordnung zwischen einer Vertex-Element Verwendung und einem Verwendungs Index für ein Vertex-Shader-Eingabe Register.

## <a name="syntax"></a>Syntax



|                                |
|--------------------------------|
| DCL- \_ Verwendungs \[ Verwendungs \_ Index \] v\# |



 

Hierbei gilt:

-   die DCL-Verwendung gibt an, \_ wie die Register Daten verwendet werden. Dies ist der gleiche Wert wie die Member von [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) ohne das D3DDECLUSAGE-Präfix.
-   der Verwendungs \_ Index ist ein optionaler ganzzahliger Index zwischen 0 und 15. Sie ändert die Verwendungs Daten. Der Index entspricht dem Verwendungs Index in einer Scheitelpunkt Deklaration. Siehe [Vertex-Deklaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). Der Index wird an den Verwendungs Wert (DCL- \_ Verwendung) ohne Leerzeichen angehängt. Wenn Sie nicht angegeben wird, wird davon ausgegangen, dass Sie 0 ist.
-   v \# ist ein [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DCL- \_ Verwendung             | x    | x    | x    | x     | x    | x     |



 

Alle DCL- \_ Verwendungs Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 