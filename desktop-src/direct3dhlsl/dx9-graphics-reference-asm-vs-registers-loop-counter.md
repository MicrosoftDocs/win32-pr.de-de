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
ms.openlocfilehash: aa0bf4d44d33f6939c8c45af4509e15e96adf9c4c36a611e049097120db2ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023940"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Schleifenzählerregister (HLSL VS-Referenz)

Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter). Sie wird bei jeder Ausführung der [Schleife](loop---vs.md)automatisch erhöht – im Vergleich zu ... [endloop – vs](endloop---vs.md) block. Daher kann sie im -Block bei Bedarf für die relative Adressierung verwendet werden und ist ungültig, um sie außerhalb der Schleife zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




