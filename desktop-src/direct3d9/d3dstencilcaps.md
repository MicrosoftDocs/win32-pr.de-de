---
description: Treiber-Schablonenfunktionsflags.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6716748d77fe4c3620413f43ae4a4ae48076c09f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997377"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Treiber-Schablonenfunktionsflags.



| \#Definieren                 | Wert       | BESCHREIBUNG                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ KEEP     | 0x00000001L | Aktualisieren Sie den Eintrag im Schablonenpuffer nicht. Dies ist der Standardwert.                             |
| D3DSTENCILCAPS \_ 0 (NULL)     | 0x00000002L | Legen Sie den Schablonenpuffereintrag auf 0 fest.                                                                    |
| D3DSTENCILCAPS \_ REPLACE  | 0x00000004L | Ersetzen Sie den Schablonenpuffereintrag durch den Verweiswert.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Erhöhen Sie den Schablonenpuffereintrag, und klammern Sie sich an den Maximalwert.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Dekrementieren Sie den Schablonenpuffereintrag, und klammern Sie an 0 (null).                                                 |
| D3DSTENCILCAPS \_ INVERT   | 0x00000020L | Invertiert die Bits im Schablonenpuffereintrag.                                                          |
| D3DSTENCILCAPS \_ INCR     | 0x00000040L | Erhöhen Sie den Eintrag stencil-buffer, und umschließen Sie diesen auf 0 (null), wenn der neue Wert den Maximalwert überschreitet.      |
| D3DSTENCILCAPS \_ DECR     | 0x00000080L | Dekrementen Sie den Eintrag stencil-buffer, und umschließen Sie den Maximalen Wert, wenn der neue Wert kleiner als 0 (null) ist. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | Das Gerät unterstützt die zweiseitige Schablone.                                                                |



 

Schablonenpuffereinträge sind ganzzahlige Werte im Bereich von 0 bis 2ⁿ – 1, wobei n die Bittiefe des Schablonenpuffers ist.

Diese Konstanten werden vom StencilCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstanteninformationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



