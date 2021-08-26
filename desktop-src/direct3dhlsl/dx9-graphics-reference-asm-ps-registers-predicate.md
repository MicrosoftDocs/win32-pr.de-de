---
title: Prädikatregister (HLSL-PS-Referenz)
description: Dieses Pixel-Shader-Ausgaberegister enthält einen booleschen Wert pro Kanal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cc8404c9a6be87951142ff3473b283a57f4814b729a8ad5a462f9069b20f3ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950030"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Prädikatregister (HLSL-PS-Referenz)

Dieses Pixel-Shader-Ausgaberegister enthält einen booleschen Wert pro Kanal.

Ein Prädikatregister wird von den folgenden Versionen unterstützt:



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Prädikatregister    |      |      |      |      |      |       | x    | x    | x     |



 

Hier sind die Registereigenschaften.



| Registertyp | Anzahl | R/W | \# Leseports | \# Lese-/Inst-Lesefunktionen | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicate(p)  | 1     | R/W | 1             | 1             | 4         | Nicht zutreffend     | Keine     | N            |



 

Das Prädikatregister kann mit [setp \_ comp - ps](setp-comp---ps.md)geändert werden. Es gibt keine Standardwerte für dieses Register. Eine Anwendung muss das Register festlegen, bevor sie verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




