---
title: Einschränkungen der Fluss Steuerung
description: Die Anweisungen für die Fluss Steuerung von Pixel Shader haben Beschränkungen, die beeinflussen, wie viele Schachtelungs Ebenen in den Anweisungen enthalten sein können. Außerdem gibt es einige Einschränkungen bei der Implementierung der Datenflusssteuerung pro Pixel mit Farbverlaufs Anweisungen.
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34891e29a1bb27aead629db2cc7473c7d4329af5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856960"
---
# <a name="flow-control-limitations"></a>Einschränkungen der Fluss Steuerung

Die Anweisungen für die Fluss Steuerung von Pixel Shader haben Beschränkungen, die beeinflussen, wie viele Schachtelungs Ebenen in den Anweisungen enthalten sein können. Außerdem gibt es einige Einschränkungen bei der Implementierung der Datenflusssteuerung pro Pixel mit Farbverlaufs Anweisungen.

> [!Note]  
> Wenn Sie die \* \_ \_ HLSL-Shader-Profile der 4 0- \_ Ebene \_ 9 \_ x verwenden, verwenden Sie implizit die [Shader Model 2. x](dx-graphics-hlsl-sm2.md) -Profile zur Unterstützung von Direct3D 9-fähiger Hardware. Shader Model 2. x-Profile unterstützen ein eingeschränktes Verhalten der Fluss Steuerung als das [Shader-Modell 4. x](dx-graphics-hlsl-sm4.md) und spätere Profile.

 

-   [Anzahl der Anweisungs Tiefen der Pixel-Shader](#pixel-shader-instruction-depth-counts)
-   [Interaktion von Per-Pixel Fluss Steuerung mit Bildschirm Farbverläufen](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>Anzahl der Anweisungs Tiefen der Pixel-Shader

PS \_ 2 \_ 0 bietet keine Unterstützung für die Fluss Steuerung. Die Einschränkungen für die anderen Pixel-Shader-Versionen sind unten aufgeführt.

### <a name="instruction-depth-count-for-ps_2_x"></a>Anweisungs Tiefe für PS \_ 2 \_ x

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. In der folgenden Tabelle sind die tiefen Zähler aufgelistet, die von jeder Anweisung der vorhandenen Tiefe hinzugefügt oder subtrahiert werden.



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Wenn bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Wenn \_ Comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Wenn pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [in-PS-PS](endif---ps.md)             | -1 ([Wenn bool-PS](if-bool---ps.md)) | -1 ([Wenn pred-PS](if-pred---ps.md) oder [if \_ Comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [ENDREP-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [\_Comp-PS Abbrechen](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [callps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [Ret-PS](ret---ps.md)                 | 0                                    | -1 ([callnz pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ -Comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe definiert die Anzahl der Anweisungen, die innerhalb zueinander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf, wie in der folgenden Tabelle angegeben.



| Anweisungstypen | Maximum                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| Statische Schachtelung   | 24 if (D3DCAPS9). D3DPSHADERCAPS2 \_ 0. staticflowcontroltiefe > 0); andernfalls 0            |
| Dynamische Schachtelung  | 0 bis 24 finden Sie unter D3DCAPS9. D3DPSHADERCAPS2 \_ 0. dynamicflowcontroltiefe                          |
| Rep Schachtelung      | 0 bis 4 finden Sie unter D3DCAPS9. D3DPSHADERCAPS2 \_ 0. staticflowcontroltiefe                            |
| Rückruf Schachtelung     | 0 bis 4 finden Sie unter D3DCAPS9. D3DPSHADERCAPS2 \_ 0. staticflowcontroltiefe (unabhängig von Rep-Limit) |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Anweisungs Tiefe für PS \_ 2 \_ SW

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl an, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert.



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Wenn bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Wenn pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Wenn \_ Comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [in-PS-PS](endif---ps.md)             | -1 ([Wenn bool-PS](if-bool---ps.md)) | -1 ([Wenn pred-PS](if-pred---ps.md) oder [if \_ Comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [ENDREP-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Schleife-PS](loop---ps.md)               | –                                  | –                                                                       | –              | –          |
| [ENDLOOP-PS](endloop---ps.md)         | –                                  | –                                                                       | –              | –          |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [\_Comp-PS Abbrechen](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [callps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [Ret-PS](ret---ps.md)                 | 0                                    | -1 ([callnz pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ -Comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe definiert die Anzahl der Anweisungen, die in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf, wie in der folgenden Tabelle angegeben.



| Anweisungstypen | Maximum |
|------------------|---------|
| Statische Schachtelung   | 24      |
| Dynamische Schachtelung  | 24      |
| Rep Schachtelung      | 4       |
| Rückruf Schachtelung     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Anweisungs Tiefe für PS \_ 3 \_ 0

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl an, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert.



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Wenn bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Wenn pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Wenn \_ Comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [in-PS-PS](endif---ps.md)             | -1 ([Wenn bool-PS](if-bool---ps.md)) | -1 ([Wenn pred-PS](if-pred---ps.md) oder [if \_ Comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [ENDREP-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Schleife-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [\_Comp-PS Abbrechen](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [callps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [Ret-PS](ret---ps.md)                 | 0                                    | -1 ([callnz pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ -Comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe definiert die Anzahl der Anweisungen, die in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf, wie in der folgenden Tabelle angegeben.



| Anweisungstypen | Maximum |
|------------------|---------|
| Statische Schachtelung   | 24      |
| Dynamische Schachtelung  | 24      |
| Schleife/Rep-Schachtelung | 4       |
| Rückruf Schachtelung     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Anweisungs tiefen Anzahl für PS \_ 3 \_ SW

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl an, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert.



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Wenn bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Wenn pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Wenn \_ Comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [in-PS-PS](endif---ps.md)             | -1 ([Wenn bool-PS](if-bool---ps.md)) | -1 ([Wenn pred-PS](if-pred---ps.md) oder [if \_ Comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [ENDREP-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Schleife-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [\_Comp-PS Abbrechen](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [callps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [Ret-PS](ret---ps.md)                 | 0                                    | -1 ([callnz pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ -Comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe definiert die Anzahl der Anweisungen, die in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf, wie in der folgenden Tabelle angegeben.



| Anweisungstypen | Maximum |
|------------------|---------|
| Statische Schachtelung   | 24      |
| Dynamische Schachtelung  | 24      |
| Schleife/Rep-Schachtelung | 4       |
| Rückruf Schachtelung     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Interaktion von Per-Pixel Fluss Steuerung mit Bildschirm Farbverläufen

Der Pixelshader-Anweisungs Satz umfasst mehrere Anweisungen, mit denen in Bezug auf den Bildschirmbereich x und y Farbverläufe erzeugt oder verwendet werden. Die häufigste Verwendung für Farbverläufe ist das Berechnen von Detail Berechnungen für die Textur Stichprobe und das Auswählen von Beispielen auf der Achse von Anisotropie im Fall von anisotrope filtern. In der Regel führen Hardware Implementierungen den Pixel-Shader gleichzeitig auf mehreren Pixeln aus (z. b. ein 2 x 2-Raster), sodass Farbverläufe der im Shader berechneten Mengen in angemessener Weise als Delta der Werte zum gleichen Zeitpunkt der Ausführung in angrenzenden Pixeln gleich sind.

Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel separate Fluss Steuerungs Pfade ausführen können. Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann.

Alle pixelshaderanweisungen werden in die zulässigen Vorgänge und in diejenigen, die in der Fluss Steuerung nicht zulässig sind, partitioniert:

-   Szenario A: Vorgänge, die innerhalb der Fluss Steuerung nicht zulässig sind und die in einem primitiven über die Pixel abweichen können. Dies schließt die in der folgenden Tabelle aufgeführten Vorgänge ein. 

    | Anweisung                                                                                                      | Ist in der Fluss Steuerung zulässig, wenn Folgendes gilt:                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) und [texldp-PS](texldp---ps.md) | Ein temporäres Register wird für die Textur Koordinate verwendet. |
    | [DSX-PS](dsx---ps.md) und [DSY-PS](dsy---ps.md)                                                            | Für den Operanden wird ein temporäres Register verwendet.            |

    

     

-   Szenario B: an beliebiger Stelle zulässige Vorgänge. Dies schließt die in der folgenden Tabelle aufgeführten Vorgänge ein. 

    | Anweisung                                                                                                      | Ist an jedem Ort zulässig, wenn:                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) und [texldp-PS](texldp---ps.md) | Für die Textur Koordinate wird eine schreibgeschützte Menge verwendet (kann je nach Pixel variieren, z. b. interpoliert-Texturkoordinaten). |
    | [DSX-PS](dsx---ps.md) und [DSY-PS](dsy---ps.md)                                                            | Für den Eingabe Operanden wird eine schreibgeschützte Menge verwendet (kann je nach Pixel variieren, z. b. interpoliert-Texturkoordinaten).      |
    | [texldl-PS](texldl---ps.md)                                                                                   | Der Benutzer stellt Detailinformationen als Argument bereit. es gibt also keine Farbverläufe und somit kein Problem mit der Fluss Steuerung.       |
    | [texldd-PS](texldd---ps.md)                                                                                   | Der Benutzer stellt Farbverläufe als Eingabeargumente bereit, sodass kein Problem mit der Fluss Steuerung vorliegt.                                 |

    

     

Diese Einschränkungen werden in der Shader-Validierung streng erzwungen. Szenarien, die eine Verzweigungs Bedingung aufweisen, die so aussieht, dass Sie in einem primitiven einheitlich verzweigt, obwohl ein Operand im Bedingungs Ausdruck eine Pixel-Shader-berechnete Menge ist, aber trotzdem in Szenario a fällt und nicht zulässig ist. Ebenso werden Szenarios, in denen Farbverläufe für eine vom Shader berechnete Menge x aus der dynamischen Fluss Steuerung angefordert werden, aber der Anschein nach, dass x nicht in den Verzweigungen geändert wird, trotzdem in Szenario A fallen und nicht zulässig sind.

Das Prädikat ist in diesen Einschränkungen für die Fluss Steuerung enthalten, sodass Implementierungen den Austausch der Implementierung von Verzweigungs Anweisungen mit prädikationsanweisungen trivial austauschen können.

Der Benutzer kann die Anweisungen aus den Szenarien A und B gleichzeitig verwenden. Nehmen wir beispielsweise an, dass der Benutzer ein anisotrope Textur Beispiel benötigt, bei dem eine berechnete Shader-Textur Koordinate der Textur Ladevorgang wird jedoch nur für Pixel benötigt, die eine pro-Pixel-Bedingung erfüllen. Um diese Anforderungen zu erfüllen, kann der Benutzer die Textur Koordinate für alle Pixel berechnen, und zwar außerhalb der Pixel-unterschiedlichen Fluss Steuerung, indem er mit [DSX-PS](dsx---ps.md) und [DSY-PS-](dsy---ps.md) Anweisungen sofort Farbverläufe berechnet. Anschließend kann der Benutzer in einem pro-Pixel- [if bool-PS](if-bool---ps.md)-Block " / [SDIF-PS](endif---ps.md) " [texldd-PS](texldd---ps.md) (Textur Auslastung mit vom Benutzer bereitgestellten Farbverläufen) verwenden und dabei die vorab berechneten Farbverläufe übergeben. Eine andere Möglichkeit, dieses Verwendungs Muster zu beschreiben, besteht darin, dass alle Pixel im primitiven die Texturkoordinaten berechnen müssen und mit der Farbverlaufs Berechnung einbezogen werden müssen, nur die Pixel, die für eine Textur eine Textur benötigt haben.

Unabhängig von diesen Regeln besteht die Belastung des Benutzers darin, dass vor dem Berechnen eines Farbverlaufs (oder dem Durchführen eines Textur Beispiels, das implizit einen Farbverlauf berechnet) das Register, das die Quelldaten enthält, für alle Ausführungs Pfade vorher initialisiert werden muss. Die Initialisierung temporärer Register wird im Allgemeinen nicht überprüft oder erzwungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




