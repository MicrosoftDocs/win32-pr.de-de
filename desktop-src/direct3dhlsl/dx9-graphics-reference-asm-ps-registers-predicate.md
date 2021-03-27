---
title: Prädikat Register (HLSL PS-Referenz)
description: Dieses Pixel-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719530"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Prädikat Register (HLSL PS-Referenz)

Dieses Pixel-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.

Ein Prädikat Register wird von folgenden Versionen unterstützt:



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Prädikat Register    |      |      |      |      |      |       | x    | x    | x     |



 

Hier sind die Register Eigenschaften.



| Registriungstyp | Anzahl | R/W | \# Leseports | \# Lese-/inst- | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Prädikat (p)  | 1     | R/W | 1             | 1             | 4         | Nicht zutreffend     | Keine     | N            |



 

Das Prädikat Register kann mit [SETP \_ Comp-PS](setp-comp---ps.md)geändert werden. Es sind keine Standardwerte für dieses Register vorhanden. eine Anwendung muss das Register festlegen, bevor Sie verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




