---
title: Prädikat Register (HLSL vs-Referenz)
description: Dieses Vertex-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104038384"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Prädikat Register (HLSL vs-Referenz)

Dieses Vertex-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.

Ein Prädikat Register wird von den folgenden Versionen unterstützt.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Prädikat Register     |      |      |       | x    | x    | x     |



 

Hier sind die Register Eigenschaften.



| Registriungstyp | Anzahl | R/W | \# Leseports | \# Lese-/inst- | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Prädikat (p)  | 1     | R/W | 1             | 1             | 4         | Nicht zutreffend     | Keine     | N            |



 

Das Prädikat Register kann mit [SETP \_ Comp-vs](setp-comp---vs.md)geändert werden. Es sind keine Standardwerte für dieses Register vorhanden. eine Anwendung muss das Register festlegen, bevor Sie verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




