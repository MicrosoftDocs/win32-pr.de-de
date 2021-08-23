---
title: Prädikatregister (HLSL VS-Referenz)
description: Dieses Vertex-Shader-Ausgaberegister enthält einen booleschen Wert pro Kanal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28392f7bb9c2f59bd766e42ec21fb87a854b08bedd8336ebb6f7249b7eccb940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119574"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Prädikatregister (HLSL VS-Referenz)

Dieses Vertex-Shader-Ausgaberegister enthält einen booleschen Wert pro Kanal.

Ein Prädikatregister wird von den folgenden Versionen unterstützt.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Prädikatregister     |      |      |       | x    | x    | x     |



 

Hier sind die Registereigenschaften.



| Registertyp | Anzahl | R/W | \# Lesen von Ports | \# Reads/inst | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicate(p)  | 1     | R/W | 1             | 1             | 4         | Nicht zutreffend     | Keine     | N            |



 

Das Prädikatregister kann mit setp comp im Vergleich zu [ \_ geändert werden.](setp-comp---vs.md) Es gibt keine Standardwerte für dieses Register. Eine Anwendung muss das Register festlegen, bevor es verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




