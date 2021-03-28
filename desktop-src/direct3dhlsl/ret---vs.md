---
title: Ret-vs
description: Rückgabe aus einer Unterroutine oder einer Main-Funktion.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313650"
---
# <a name="ret---vs"></a>Ret-vs

Rückgabe aus einer Unterroutine oder einer Main-Funktion.

## <a name="syntax"></a>Syntax



| TZI |
|-----|



 

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| TZI                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung übernimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort. Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.

Die ret-Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.

Wenn ein Shader keine Unterroutinen enthält, ist die Verwendung von Ret am Ende des Hauptprogramms optional.

Mehrere Return-Anweisungen sind im Hauptprogramm oder in einer Unterroutine nicht zulässig. die erste Return-Anweisung wird als Ende des Hauptprogramms oder der Unterroutine behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




