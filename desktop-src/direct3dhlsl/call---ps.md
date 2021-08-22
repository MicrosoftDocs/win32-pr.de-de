---
title: call - ps
description: Führt einen Funktionsaufruf der Anweisung aus, die mit der angegebenen Bezeichnung markiert ist. | call - ps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ae1b8a19178b0a6633a98472814e225e9ac2f7de9e3e2f016720f2f5b1a9b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794084"
---
# <a name="call---ps"></a>call - ps

Führt einen Funktionsaufruf der Anweisung aus, die mit der angegebenen Bezeichnung markiert ist.

## <a name="syntax"></a>Syntax



| call l\# |
|----------|



 

Hierbei gilt:

-   l \# ist eine [Bezeichnung– ps,](label---ps.md) die den Anfang der aufzurufenden Unterroutine markiert.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Aufruf                  |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung führt folgende Schritte aus:

1.  Pushadresse der nächsten Anweisung an den Rückgabeadressstapel.
2.  Setzen Sie die Ausführung über die durch die Bezeichnung markierte Anweisung fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




