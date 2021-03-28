---
title: Ret-PS
description: Nimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort. Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976345"
---
# <a name="ret---ps"></a>Ret-PS

Nimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort. Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.

## <a name="syntax"></a>Syntax



| TZI |
|-----|



 

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| TZI                   |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung übernimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort. Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.

Die ret-Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.

Wenn ein Shader keine Unterroutinen enthält, ist die Verwendung von Ret am Ende des Hauptprogramms optional.

Mehrere Return-Anweisungen sind im Hauptprogramm oder in einer Unterroutine nicht zulässig. die erste Return-Anweisung wird als Ende des Hauptprogramms oder der Unterroutine behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




