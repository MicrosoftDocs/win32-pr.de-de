---
title: atomic_imin (sm5 - asm)
description: Atomarer Ganzzahlwert mit Vorzeichen im Arbeitsspeicher.
ms.assetid: C30C7CDE-1024-4E69-959E-2D3122BF9AA7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a028fbca75046373e9fda13ed52e28313310de819a308fb93cd06429796695a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287743"
---
# <a name="atomic_imin-sm5---asm"></a>atomic \_ imin (sm5 - asm)

Atomarer Ganzzahlwert mit Vorzeichen im Arbeitsspeicher.



| atomic \_ imin dst, dstAddress \[ .swizzle, \] src0 \[ .select \_ component\] |
|----------------------------------------------------------------------|



 



| Element                                                                                                           | Beschreibung                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[in \] Die Komponenten, die mit *src0 verglichen werden.* Dieser Wert muss eine ungeordnete Zugriffsansicht (UAV) (u) \# sein. Im Compute-Shader kann es sich auch um gemeinsam genutzten Threadgruppenspeicher (g ) \# sein. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Die Speicheradresse.<br/>                                                                                                                                                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Die Komponenten, die mit *dst verglichen werden.*<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Mit dieser Anweisung wird ein einzelner 32-Bit-Bit-Mindestwert für den Operanden *src0* in *dst* bei einer 32-Bit-Adresse pro Komponente *dstAddress* ausgeführt, die atomisch ausgeführt wird.

Die Anzahl von Komponenten, die von der Adresse übernommen werden, wird durch die Dimensionalität von *dst* u \# oder g \# bestimmt.

Wenn *dst* ein u ist, kann es als unformatiert, \# typisch oder strukturiert deklariert werden. Bei Typ muss es als UINT/SINT deklariert werden, und das gebundene Ressourcenformat ist R32 \_ \_ UINT/SINT.

Wenn *dst* g \# ist, muss es als roh oder strukturiert deklariert werden.

An den Shader wird nichts zurückgegeben.

Wenn der Shaderaufruf inaktiv ist, z. B. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder wenn ein Pixel-/Beispielaufruf nur als Hilfs für ein echtes Pixel/Beispiel für Ableitungen vorhanden ist, ändert diese Anweisung den *dst-Speicher* überhaupt nicht (im Hintergrund).

Die Adressierung außerhalb der Grenzen für u bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn u strukturiert ist und der Byteoffset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der \# \# UAV nicht definiert.

Eine Nicht-Begrenzungs-Adressierung auf g (die Grenzen dieses bestimmten g im Gegensatz zum gesamten freigegebenen Speicher) führt dazu, dass der gesamte Inhalt des gesamten freigegebenen \# Speichers \# undefiniert wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8.



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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





