---
title: ret – im Vergleich zu
description: Gibt von einer Unterroutine oder einer Main-Funktion zurück.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bec0356f2f1542da421a807598707e4857033c13cda2077d9281ac24e4fc3e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853770"
---
# <a name="ret---vs"></a>ret – im Vergleich zu

Gibt von einer Unterroutine oder einer Main-Funktion zurück.

## <a name="syntax"></a>Syntax



| Ret |
|-----|



 

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Ret                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung übernimmt die Adresse einer Anweisung aus dem Rückgabeadressstapel und setzt ihre Ausführung fort. Im Fall der Main-Funktion beendet diese Anweisung die Shaderausführung.

Die Ret-Anweisung verwendet einen Vertex-Shaderanweisungsslot.

Wenn ein Shader keine Unterroutinen enthält, ist die Verwendung von ret am Ende des Hauptprogramms optional.

Mehrere Rückgabeanweisungen sind im Hauptprogramm oder in einer Unterroutine nicht zulässig. Die erste return-Anweisung wird als Ende des Hauptprogramms oder der Unterroutine behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




