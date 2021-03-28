---
title: ps_2_x
description: Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993503"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.

-   [die \_ Anweisungen für PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) enthalten eine Liste der verfügbaren Anweisungen.
-   [PS \_ 2 \_ x-Register](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) listet die verschiedenen Register Typen auf, die von Vertex Shader Alu verwendet werden.
-   [Modifiziererer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Wird verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   Die [Ziel Register-Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.
-   [Pixel-Shader-Quell Registrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.
-   Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.

## <a name="dynamic-flow-control"></a>Dynamische Fluss Steuerung

[**Dynamicflowcontroltiefe**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungs Tiefe dynamischer Fluss Steuerungs Anweisungen dar: [if](if-bool---ps.md), [if \_ Comp](if-comp---ps.md), [if \_ pred](if-pred---ps.md), [break-PS](break---ps.md)und [break \_ -PS unterbrechen](break-comp---ps.md). Der Wert ist gleich der Schachtelungs Tiefe des If- \_ Comp-Blocks. Wenn diese Obergrenze NULL ist, unterstützt das Gerät keine Anweisungen zur dynamischen Fluss Steuerung.

## <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

Die Anzahl der vom Gerät unterstützten temporären Register. Der Bereich liegt zwischen 12 und 32.

## <a name="static-flow-control-nesting-depth"></a>Schachtelungs Tiefe der statischen Fluss Steuerung

[**Staticflowcontroltiefe**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungs Tiefe von zwei Typen von statischen Fluss Steuerungs Anweisungen dar: [Loop](loop---ps.md)  / [Rep](rep---ps.md) und [](call---ps.md)  / [callnz](callnz-bool---ps.md)aufrufen. Schleife/Rep Anweisungen können in der Tiefe von **staticflowcontroldeep** verschachtelt werden. /Callnz-Anweisungen können unabhängig voneinander in " **staticflowcontroldeep** " verschachtelt werden.

## <a name="number-of-instruction-slots"></a>Anzahl der Anweisungs Slots

Die Anzahl der Anweisungs Slots kann zwischen 96 und einem Maximum von 512 liegen und wird durch [**maxpixelshaderinstructionslots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)angegeben. Die Gesamtanzahl der Anweisungen, die ausgeführt werden können, wird durch **maxpixelshaderinstructionsexecuted** definiert. Dieser Wert kann größer als die Anzahl der Anweisungs Slots aufgrund von Schleifen-und Unterroutine aufrufen sein.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Wenn [**D3DD3DPSHADERCAPS2 0 für das willkürliche \_ \_ aryswizzle**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird ein beliebiges Swizzle unterstützt. Weitere Informationen finden Sie unter [Quellen Register: schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Farbverlaufs Anweisungen

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, werden Farbverlaufs Anweisungen unterstützt. Siehe [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)und [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Prädikation

Wenn das [**D3DD3DPSHADERCAPS2 \_ 0- \_ Prädikat**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird das Anweisungs Prädikat unterstützt. Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Abhängiges Lese Limit

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine abhängigen Lese Limits.

## <a name="texture-instruction-limit"></a>Grenzwert für Textur Anweisung

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine Begrenzung der Textur Anweisungen.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Samplern ist 16.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 