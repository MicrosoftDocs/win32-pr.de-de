---
title: Schleifenzählerregister (HLSL-PS-Referenz)
description: Informieren Sie sich über das Schleifenzählerregister für Pixel-Shader. Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405513"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Schleifenzählerregister (HLSL-PS-Referenz)

Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter). Bei jeder Ausführung der [Schleife](loop---ps.md)– ps / [endloop](endloop---ps.md) – ps block – wird sie automatisch erhöht. Daher kann sie im -Block bei Bedarf für die relative Adressierung verwendet werden und ist ungültig, um sie außerhalb der Schleife zu verwenden.



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Schleifenzählerregister |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




