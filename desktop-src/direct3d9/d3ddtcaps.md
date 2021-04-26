---
description: Konstanten, die die von einem Gerät unterstützten Scheitelpunktdatentypen beschreiben.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999447"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Konstanten, die die von einem Gerät unterstützten Scheitelpunktdatentypen beschreiben.



| \#Definieren              | Wert       | BESCHREIBUNG                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | 4D-Byte ohne Vorzeichen.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Normalisiertes, 4D-Byte ohne Vorzeichen. Jedes der vier Bytes wird durch Division in 255,0 normalisiert.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | Normalisiert 4D unsigned short, erweitert auf (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | 3D unsigned 10 10 10 format expanded to (value, value, value, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | 3D signiertes 10 10 10-Format normalisiert und erweitert auf (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | 2D-16-Bit-Gleitkommazahlen.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | 4D-16-Bit-Gleitkommazahlen.                                                                                             |



 

Diese Konstanten werden vom DeclTypes-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



