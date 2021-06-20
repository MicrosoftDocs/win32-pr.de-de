---
title: Schleifenzählerregister (HLSL VS-Referenz)
description: Informieren Sie sich über das Schleifenzählerregister für Vertex-Shader. Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405773"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Schleifenzählerregister (HLSL VS-Referenz)

Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter). Sie wird bei jeder Ausführung der [Schleife](loop---vs.md)automatisch erhöht – im Vergleich zu ... [endloop – vs](endloop---vs.md) block. Daher kann sie im -Block bei Bedarf für die relative Adressierung verwendet werden und ist ungültig, um sie außerhalb der Schleife zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




