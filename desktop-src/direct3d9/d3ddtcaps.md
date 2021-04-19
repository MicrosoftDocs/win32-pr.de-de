---
description: Konstanten, die die von einem Gerät unterstützten Scheitelpunkt Datentypen beschreiben.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346639"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Konstanten, die die von einem Gerät unterstützten Scheitelpunkt Datentypen beschreiben.



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| \#definieren              | Wert       | BESCHREIBUNG                                                                                                                   |
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | 4D-Byte ohne Vorzeichen.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Normalisiertes, 4D-Byte ohne Vorzeichen. Alle vier Bytes werden normalisiert, indem Sie auf 255,0 dividiert werden.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normalized, 2D signed Short, erweitert auf (erstes Byte/32767.0, zweites Byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalized, 4D signed Short, erweitert auf (erstes Byte/32767.0, zweites Byte/32767.0, Drittes Byte/32767.0, viertes Byte/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalized, 2D Ganzzahl ohne Vorzeichen Short, erweitert auf (First Byte/65535.0, Second Byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020l | Normalisierte 4D (Ganzzahl ohne Vorzeichen Short), erweitert auf (erstes Byte/65535.0, zweites Byte/65535.0, Drittes Byte/65535.0, viertes Byte/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040l | 3D-Format ohne Vorzeichen 10 10 10 erweitert auf (Wert, Wert, Wert, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080l | 3D-signiertes 10 10 10-Format normalisiert und erweitert auf (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100l | 2D-16-Bit-Gleit Komma Zahlen.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200l | 4D-16-Bit-Gleit Komma Zahlen.                                                                                             |



 

Diese Konstanten werden vom decltypes-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



