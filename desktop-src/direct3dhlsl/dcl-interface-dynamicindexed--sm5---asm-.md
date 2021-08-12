---
title: dcl_interface_dynamicindexed (sm5 - asm)
description: Deklarieren Sie Funktionstabellenzeker (Schnittstellen). | dcl_interface_dynamicindexed (sm5 - asm)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bc52dc841b2e6de3c5af9725faac2c6dc5900b95117a28f77d8bc5087248df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286052"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a>dcl \_ interface \_ dynamicindexed (sm5 - asm)

Deklarieren Sie Funktionstabellenzeker (Schnittstellen).



| dcl \_ interface \_ dynamicindexed fp \# \[ arraySize \] \[ numCallSites \] = {ft, \# \# ft, ...} |
|--------------------------------------------------------------------------------------|



 



| Element                                                          | Beschreibung                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/> | \[in \] Die Funktionstabellenzeer.<br/> |



 

## <a name="remarks"></a>Hinweise

Jede Schnittstelle muss von der API gebunden werden, bevor der Shader verwendet werden kann. Die Bindung gibt einen Verweis auf eine der Funktionstabellen zurück, damit die Methodenslots ausgefüllt werden können. Der Compiler generiert keine Zeiger für Nichtreferenzierte Objekte.

Ein Funktionstabellenzeiger verfügt über einen vollständigen Satz von Methodenslots, um die zusätzliche Deskriptionsebene zu vermeiden, die eine C++-Zeiger-zu-VTable-Darstellung erfordern würde. Dies würde auch erfordern, dass diese Zeiger 5-Tupel sind. Im virtuellen HLSL-Inliningmodell ist immer bekannt, welche globale Variable/Eingabe für einen Aufruf verwendet wird, damit wir Tabellen pro Stammobjekt einrichten können.

Funktionszeigerdeklarationen geben an, welche Funktionstabellen mit ihnen verwendet werden können. Dies ermöglicht auch die Ableitung von Methodenkorrelationsinformationen.

Die erste \[ \] einer Schnittstellendeklaration ist die Arraygröße. Wenn die dynamische Indizierung verwendet wird, gibt die Deklaration dies wie gezeigt an. Ein Array von Schnittstellenze0ern kann auch statisch indiziert werden. Es ist nicht erforderlich, dass Arrays von Schnittstellenze0ern eine dynamische Indizierung bedeuten.

Die Nummerierung von Schnittstellenzeigern beginnt bei 0 für die erste Deklaration und berücksichtigt anschließend die Arraygröße, sodass der erste Zeiger nach einem vier Eintragsarray fp0 \[ 4 \] \[ 1 \] fp4 \[ \] \[ \] wäre.

Die zweite einer Schnittstellendeklaration ist die Anzahl der Aufrufstandorte, die mit der Anzahl von Körpern in jeder Tabelle übereinstimmen müssen, auf die \[ \] in der Deklaration verwiesen wird.

Es gibt keine Begrenzungen dafür, wie viele Funktionstabellenoptionen \# (ft) in einer Schnittstellendeklaration aufgelistet werden können.

Eine bestimmte Funktionstabelle (ft) kann in einer oder mehr Schnittstellendeklarationen mehr als \# einmal angezeigt werden.

### <a name="restrictions"></a>Beschränkungen

-   Die Anzahl der Objektstandorte in einem Shader, die die Summe aller FP-Deklarationen *\#* ihrer arraySize-Deklarationen ist, darf nicht mehr als \[ \] 253 sein. Diese Zahl entspricht der Anzahl **dieser** Zeiger. Die Runtime erzwingt diesen Grenzwert von 253, um die Größe der DDI für die Kommunikation dieser Zeigerdaten zu begrenzen.
-   Die Anzahl der Aufrufstandorte in einem Shader, also die Summe aller fcall-Anweisungen der Anzahl potenzieller Verzweigungsziele, darf nicht mehr als 4096 sein.

    Ein [fcall,](fcall--sm5---asm-.md) der einen statischen Index für die erste *\[ \] \[ \] fp-Dimension* verwendet, zählt beispielsweise als eins:

    `                       fcall fp0[0][0]         // +1`

    Ein **Fcall,** der einen dynamischen Index verwendet, zählt als Anzahl der Elemente im Array (erster \[ \] der **dcl-Schnittstelle): \_**

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Dieser Grenzwert hilft einigen Implementierungen dabei, Tabellen der Funktionskörperauswahl einfach in konstanten pufferbasierten Speicher zu passen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





