---
title: dcl_usage Eingabe (sm1, sm2, sm3 – vs asm)
description: Deklarieren Sie die Zuordnung zwischen einer Vertexelementverwendung und einem Verwendungsindex für ein Vertex-Shader-Eingaberegister.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44bd976d05c0734ca2e498b5de405564f689e20d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998387"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>dcl \_ usage input (sm1, sm2, sm3 - vs asm) (dcl usage input (sm1, sm2, sm3 – vs asm))

Deklarieren Sie die Zuordnung zwischen einer Vertexelementverwendung und einem Verwendungsindex für ein Vertex-Shader-Eingaberegister.

## <a name="syntax"></a>Syntax



|                                |
|--------------------------------|
| dcl \_ usage usage index \[ \_ \] v\# |



 

Hierbei gilt:

-   dcl \_ usage gibt an, wie die Registerdaten verwendet werden. Dies ist der gleiche Wert wie die Member von [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) ohne das Präfix D3DDECLUSAGE.
-   Usage \_ Index ist ein optionaler ganzzahliger Index zwischen 0 und 15. Die Nutzungsdaten werden geändert. Der Index entspricht dem Verwendungsindex in einer Scheitelpunktdeklaration. Weitere Informationen finden Sie unter [Vertexdeklaration (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration) Der Index wird ohne Leerzeichen an den Verwendungswert (dcl \_ usage) angefügt. Wenn sie nicht angegeben wird, wird angenommen, dass sie 0 ist.
-   v \# ist ein [Eingaberegister.](dx9-graphics-reference-asm-vs-registers-input.md)

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ usage             | x    | x    | x    | x     | x    | x     |



 

Alle \_ dcl-Verwendungsanweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
