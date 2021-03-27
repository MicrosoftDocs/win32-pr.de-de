---
title: Schachtelungs Limits der Fluss Steuerung
description: Die Anweisungen für die Vertex-Shader-Fluss Steuerung haben zwei besondere Einschränkungen.
ms.assetid: c9f80a97-8245-4974-a284-7974e2d2e504
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebb5b491e074c2275081aa3fe629a2486a24c6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714490"
---
# <a name="flow-control-nesting-limits"></a>Schachtelungs Limits der Fluss Steuerung

Die Anweisungen für die Vertex-Shader-Fluss Steuerung haben zwei besondere Einschränkungen. Die Schachtelungs Tiefe schränkt die Anzahl der Anweisungen ein, die in einander aufgerufen werden können. Außerdem verfügt jede Anweisung über eine Anweisungs Slot-Anzahl, die für die maximale Anzahl von Anweisungen gilt, die ein Shader unterstützen kann.

> [!Note]  
> Wenn Sie die \* \_ \_ HLSL-Shader-Profile der 4 0- \_ Ebene \_ 9 \_ x verwenden, verwenden Sie implizit die [Shader Model 2. x](dx-graphics-hlsl-sm2.md) -Profile zur Unterstützung von Direct3D 9-fähiger Hardware. Shader Model 2. x-Profile unterstützen ein eingeschränktes Verhalten der Fluss Steuerung als das [Shader-Modell 4. x](dx-graphics-hlsl-sm4.md) und spätere Profile.

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Tiefen Anzahl pro Anweisung für vs \_ 2 \_ 0

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert:



| Anweisung                              | Statische Schachtelung | Dynamische Schachtelung | Schleife/Rep-Schachtelung | Rückruf Schachtelung | Anzahl statischer Flows                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [Wenn bool-vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [Wenn \_ Comp-vs](if-comp---vs.md)        | –            | –             | –              | –          | –                                      |
| [Wenn pred-vs](if-pred---vs.md)         | –            | –             | –              | –          | –                                      |
| [Else-vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1 (nur für[bool-vs](if-bool---vs.md) ) |
| [umdif-vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [Rep-vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [ENDREP-vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [Schleifen-vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [Break-vs](break---vs.md)             | –            | –             | –              | –          | –                                      |
| [" \_ Comp-vs" Abbrechen](break-comp---vs.md)  | –            | –             | –              | –          | –                                      |
| [Break p-vs](breakp---vs.md)           | –            | –             | –              | –          | –                                      |
| [callvs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz pred-vs](callnz-pred---vs.md) | –            | –             | –              | –          | –                                      |
| [Ret-vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [SETP \_ -Comp-vs](setp-comp---vs.md)    | –            | –             | –              | –          | –                                      |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe legen Sie fest, wie viele Anweisungen in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf:



| Anweisungstypen  | Maximum                               |
|-------------------|---------------------------------------|
| Statische Schachtelung    | Nur durch die statische Datenfluss Anzahl beschränkt |
| Dynamische Schachtelung   | –                                   |
| Schleife/Rep-Schachtelung  | 1                                     |
| Rückruf Schachtelung      | 1                                     |
| Anzahl statischer Flows | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Tiefen Anzahl pro Anweisung für vs \_ 2 \_ x

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert:



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung | Anzahl statischer Flows                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [Wenn bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [Wenn \_ Comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [Wenn pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1 (nur für[bool-vs](if-bool---vs.md) ) |
| [umdif-vs](endif---vs.md)             | -1 ([Wenn bool-vs](if-bool---vs.md)) | -1 ([Wenn pred-vs](if-pred---vs.md) oder [if \_ Comp-vs](if-comp---vs.md)) | 0                | 0            | 0                                        |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [ENDREP-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [Schleifen-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [" \_ Comp-vs" Abbrechen](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | 0                                        |
| [Break p-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [callvs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [Ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                             | 0                | -1           | 0                                        |
| [SETP \_ -Comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe legen Sie fest, wie viele Anweisungen in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf:



| Anweisungstypen  | Maximum                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| Statische Schachtelung    | Nur durch die statische Datenfluss Anzahl beschränkt                                                |
| Dynamische Schachtelung   | 0 oder 24 finden Sie unter D3DCAPS9. VS20Caps. dynamicflowcontroltiefe                               |
| Schleife/Rep-Schachtelung  | 1 bis 4 finden Sie unter D3DCAPS9. VS20Caps. staticflowcontroltiefe                                 |
| Rückruf Schachtelung      | 1 bis 4 finden Sie unter D3DCAPS9. VS20Caps. staticflowcontroltiefe (unabhängig von Schleife/Rep-Limit) |
| Anzahl statischer Flows | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Tiefen Anzahl pro Anweisung für vs \_ 2 \_ SW

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert:



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung | Anzahl statischer Flows |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Wenn bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | –               |
| [Wenn \_ Comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | –               |
| [Wenn pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | –               |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | –               |
| [umdif-vs](endif---vs.md)             | -1 ([Wenn bool-vs](if-bool---vs.md)) | -1 ([Wenn pred-vs](if-pred---vs.md) oder [if \_ Comp-vs](if-comp---vs.md)) | 0                | 0            | –               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | –               |
| [ENDREP-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | –               |
| [Schleifen-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | –               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | –               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | –               |
| [" \_ Comp-vs" Abbrechen](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | –               |
| [Break p-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | –               |
| [callvs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | –               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | –               |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | –               |
| [Ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                             | 0                | -1           | –               |
| [SETP \_ -Comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | –               |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe legen Sie fest, wie viele Anweisungen in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf:



| Anweisungstypen  | Maximum  |
|-------------------|----------|
| Statische Schachtelung    | 24       |
| Dynamische Schachtelung   | 24       |
| Schleife/Rep-Schachtelung  | 4        |
| Rückruf Schachtelung      | 4        |
| Anzahl statischer Flows | Keine Begrenzung |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Tiefen Anzahl pro Anweisung für vs \_ 3 \_ 0

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert:



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung | Anzahl statischer Flows |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Wenn bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | –               |
| [Wenn \_ Comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | –               |
| [Wenn pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | –               |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | –               |
| [umdif-vs](endif---vs.md)             | -1 ([Wenn bool-vs](if-bool---vs.md)) | -1 ([Wenn pred-vs](if-pred---vs.md) oder [if \_ Comp-vs](if-comp---vs.md)) | 0                | 0            | –               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | –               |
| [ENDREP-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | –               |
| [Schleifen-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | –               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | –               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | –               |
| [" \_ Comp-vs" Abbrechen](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | –               |
| [Break p-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | –               |
| [callvs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | –               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | –               |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | –               |
| [Ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                             | 0                | -1           | –               |
| [SETP \_ -Comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | –               |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe legen Sie fest, wie viele Anweisungen in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf:



| Anweisungstypen  | Maximum  |
|-------------------|----------|
| Statische Schachtelung    | 24       |
| Dynamische Schachtelung   | 24       |
| Schleife/Rep-Schachtelung  | 4        |
| Rückruf Schachtelung      | 4        |
| Anzahl statischer Flows | Keine Begrenzung |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Tiefen Anzahl pro Anweisung für vs \_ 3 \_ SW

Jede Anweisung wird für eine oder mehrere Schachtelungs tiefen Limits gezählt. Diese Tabelle zeigt die tiefen Anzahl, die jede Anweisung der vorhandenen Tiefe hinzufügt oder subtrahiert:



| Anweisung                              | Statische Schachtelung                       | Dynamische Schachtelung                                                           | Schleife/Rep-Schachtelung | Rückruf Schachtelung | Anzahl statischer Flows |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Wenn bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | –               |
| [Wenn \_ Comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | –               |
| [Wenn pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | –               |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | –               |
| [umdif-vs](endif---vs.md)             | -1 ([Wenn bool-vs](if-bool---vs.md)) | -1 ([Wenn pred-vs](if-pred---vs.md) oder [if \_ Comp-vs](if-comp---vs.md)) | 0                | 0            | –               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | –               |
| [ENDREP-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | –               |
| [Schleifen-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | –               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | –               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | –               |
| [" \_ Comp-vs" Abbrechen](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | –               |
| [Break p-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | –               |
| [callvs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | –               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | –               |
| [callnz pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | –               |
| [Ret-vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred-vs](callnz-pred---vs.md))                             | 0                | -1           | –               |
| [SETP \_ -Comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | –               |



 

### <a name="nesting-depth"></a>Schachtelungs Tiefe

Schachtelungs Tiefe legen Sie fest, wie viele Anweisungen in einander aufgerufen werden können. Jeder Anweisungstyp weist mindestens eine Schachtelungs Grenze auf:



| Anweisungstypen  | Maximum  |
|-------------------|----------|
| Statische Schachtelung    | 24       |
| Dynamische Schachtelung   | 24       |
| Schleife/Rep-Schachtelung  | 4        |
| Rückruf Schachtelung      | 4        |
| Anzahl statischer Flows | Keine Begrenzung |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




