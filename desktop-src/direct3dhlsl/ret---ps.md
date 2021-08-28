---
title: ret – ps
description: Übernimmt die Adresse einer Anweisung aus dem Rückgabeadressenstapel und setzt die Ausführung davon fort. Im Fall der main-Funktion beendet diese Anweisung die Shaderausführung.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77d2bb63655a83716d74621a5ece097259b0a90461f902801c375a079f118f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853780"
---
# <a name="ret---ps"></a>ret – ps

Übernimmt die Adresse einer Anweisung aus dem Rückgabeadressenstapel und setzt die Ausführung davon fort. Im Fall der main-Funktion beendet diese Anweisung die Shaderausführung.

## <a name="syntax"></a>Syntax



| Ret |
|-----|



 

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Ret                   |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung verwendet die Adresse einer Anweisung aus dem Rückgabeadressenstapel und setzt die Ausführung davon fort. Im Fall der main-Funktion beendet diese Anweisung die Shaderausführung.

Die ret-Anweisung verwendet einen Vertex-Shaderanweisungsslot.

Wenn ein Shader keine Unterroutinen enthält, ist die Verwendung von ret am Ende des Hauptprogramms optional.

Mehrere Return-Anweisungen sind im Hauptprogramm oder in einer Unterroutine nicht zulässig. Die erste return-Anweisung wird als Das Ende des Hauptprogramms oder der Unterroutine behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




