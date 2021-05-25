---
description: Treiberschablonenfunktionsflags.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343055"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Treiberschablonenfunktionsflags.



| \#Definieren                 | Wert       | BESCHREIBUNG                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ KEEP     | 0x00000001L | Aktualisieren Sie den Eintrag im Schablonenpuffer nicht. Dies ist der Standardwert.                             |
| D3DSTENCILCAPS \_ ZERO     | 0x00000002L | Legen Sie den Eintrag stencil-buffer auf 0 fest.                                                                    |
| D3DSTENCILCAPS \_ REPLACE  | 0x00000004L | Ersetzen Sie den Eintrag stencil-buffer durch den Verweiswert.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Erhöhen Sie den Eintrag für den Schablonenpuffer, und legen Sie dabei den Maximalwert fest.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Dekrementieren Sie den Schablonenpuffereintrag, indem Sie auf 0 (null) klammern.                                                 |
| D3DSTENCILCAPS \_ INVERT   | 0x00000020L | Umkehren der Bits im Schablonenpuffereintrag.                                                          |
| D3DSTENCILCAPS \_ INCR     | 0x00000040L | Inkrementiert den Schablonenpuffereintrag und wird auf 0 (null) gesetzt, wenn der neue Wert den Maximalwert überschreitet.      |
| D3DSTENCILCAPS \_ DECR     | 0x00000080L | Dekrementierung des Schablonenpuffereintrags und Umschließen bis zum höchstwert, wenn der neue Wert kleiner als 0 (null) ist. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | Das Gerät unterstützt die zweiseitige Schablone.                                                                |



 

Schablonenpuffereinträge sind ganzzahlige Werte im Bereich von 0 bis 2ⁿ - 1, wobei n die Bittiefe des Schablonenpuffers ist.

Diese Konstanten werden vom StencilCaps-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



