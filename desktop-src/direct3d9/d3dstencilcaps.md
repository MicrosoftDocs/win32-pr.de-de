---
description: Funktionsfunktionsflags der Treiber Schablone.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392970"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Funktionsfunktionsflags der Treiber Schablone.



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| \#definieren                 | Wert       | BESCHREIBUNG                                                                                           |
| D3DSTENCILCAPS \_ beibehalten     | 0x00000001L | Aktualisieren Sie den Eintrag nicht im Schablonen Puffer. Dies ist der Standardwert.                             |
| D3DSTENCILCAPS \_ 0     | 0x00000002L | Legen Sie den Schablone-Puffer Eintrag auf 0 fest.                                                                    |
| D3DSTENCILCAPS \_ ersetzen  | 0x00000004L | Ersetzen Sie den Stencil-Buffer-Eintrag durch den Verweis Wert.                                                |
| D3DSTENCILCAPS \_ incrsat  | 0x00000008L | Erhöhen Sie den Schablone-Puffer Eintrag, und legen Sie auf den maximalen Wert an.                                    |
| D3DSTENCILCAPS \_ decrsat  | 0x00000010L | Dekrement der Schablone-Puffer Eintrag, der auf 0 (null) gesetzt wird.                                                 |
| D3DSTENCILCAPS \_ umkehren   | 0x00000020l | Umkehren Sie die Bits im Schablone-Puffer Eintrag.                                                          |
| D3DSTENCILCAPS \_ INCR     | 0x00000040l | Erhöhen Sie den Schablonen Puffer Eintrag, wobei der Wert auf 0 (null) umwickelt wird, wenn der neue Wert den maximalen Wert überschreitet.      |
| D3DSTENCILCAPS- \_ decr     | 0x00000080l | Verringert den Schablonen Puffer Eintrag und umwickelt ihn in den maximalen Wert, wenn der neue Wert kleiner als 0 (null) ist. |
| D3DSTENCILCAPS \_ twoseitigem | 0x00000100l | Das Gerät unterstützt zweiseitige Schablonen.                                                                |



 

Schablone-Puffer Einträge sind ganzzahlige Werte im Bereich von 0 bis 2 ⁿ-1, wobei n die Bittiefe des Schablonen Puffers ist.

Diese Konstanten werden vom Schablone-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



