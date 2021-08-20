---
title: imm_atomic_iadd (sm5 – asm)
description: Sofortige atomare ganze Zahl wird dem Arbeitsspeicher hinzugefügt. Gibt den Wert im Arbeitsspeicher vor dem Hinzufügen zurück.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80a24fad3731f3d55c09f232ec61f4b3b09828cc7abd698e74259efe907c6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511415"
---
# <a name="imm_atomic_iadd-sm5---asm"></a>imm \_ atomic \_ iadd (sm5 – asm)

Sofortige atomare ganze Zahl wird dem Arbeitsspeicher hinzugefügt. Gibt den Wert im Arbeitsspeicher vor dem Hinzufügen zurück.



| imm \_ atomic \_ iadd dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                           | Beschreibung                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Enthält den Wert in *dst1* vor dem Schreibvorgang. <br/>                                                                           |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | Bei diesem Wert muss es sich um eine ungeordnete Zugriffsansicht (UAV) \# (u) handelt. Im Compute-Shader kann es sich auch um freigegebenen Speicher der Threadgruppe \# (g) befinden. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Die Speicheradresse.<br/>                                                                                                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Der Wert, der *dst1* hinzugefügt werden soll.<br/>                                                                                               |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine einzelne 32-Bit-Ganzzahl der Komponente aus, die den Operanden *src0* mit *dst1* bei 32-Bit pro Komponentenadresse *dstAddress* hinzufüge. Signieren ist nicht erforderlich.

Wenn *dst1* ein u \# ist, wurde er möglicherweise als roh, typisiert oder strukturiert deklariert. Wenn sie typisiert ist, muss sie als UINT/SINT deklariert werden, wobei das gebundene Ressourcenformat R32 \_ \_ UINT/SINT ist.

Wenn *dst1* g \# ist, muss es als roh oder strukturiert deklariert werden.

Der Wert im *dst1-Speicher,* bevor das Hinzufügen zu *dst0* zurückgegeben wird.

Die Anzahl der Von der Adresse entnommenen Komponenten wird durch die Dimensionalität von *dst1* bestimmt.

Der gesamte Vorgang wird atomar ausgeführt.

Wenn der Shaderaufruf inaktiv ist, z. B. wenn das Pixel zuvor bei der Ausführung verworfen wurde, oder ein Pixel-/Beispielaufruf nur als Hilfselement für ein echtes Pixel/Sample für Ableitungen vorhanden ist, ändert diese Anweisung den *dst1-Speicher* überhaupt nicht, und der zurückgegebene Wert ist nicht definiert.

Die Adressierung außerhalb der Grenzen für u bewirkt, dass nichts in \# den Arbeitsspeicher geschrieben wird, außer wenn das u strukturiert ist und der \# Byteoffset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt des UAV nicht definiert.

Die Adressierung außerhalb der Grenzen für u \# oder g \# bewirkt, dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





