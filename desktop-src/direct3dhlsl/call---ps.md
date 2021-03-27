---
title: callps
description: Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist. | callps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995494"
---
# <a name="call---ps"></a>callps

Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist.

## <a name="syntax"></a>Syntax



| l anrufen\# |
|----------|



 

Hierbei gilt:

-   l \# ist eine [Bezeichnung-PS](label---ps.md) , die den Anfang der aufzurufenden Unterroutine markiert.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Aufruf                  |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:

1.  Die pushadresse der nächsten Anweisung in den Rückgabe Adress Stapel.
2.  Setzen Sie die Ausführung mit der von der Bezeichnung markierten Anweisung fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




