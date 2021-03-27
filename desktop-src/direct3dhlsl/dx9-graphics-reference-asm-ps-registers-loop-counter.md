---
title: Schleifen Zählers-Register (HLSL PS-Referenz)
description: Das einzige Register in dieser Bank ist das aktuelle Loop Counter-Register (Al).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719541"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Schleifen Zählers-Register (HLSL PS-Referenz)

Das einzige Register in dieser Bank ist das aktuelle Loop Counter-Register (Al). Sie wird bei jeder Ausführung des [Loop-PS](loop---ps.md)- / [ENDLOOP-PS-](endloop---ps.md) Blocks automatisch inkrementiert. Daher kann Sie bei Bedarf im-Block für die relative Adressierung verwendet werden und ist nicht für die Verwendung außerhalb der-Schleife ungültig.



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Schleifen-Counter-Register |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




