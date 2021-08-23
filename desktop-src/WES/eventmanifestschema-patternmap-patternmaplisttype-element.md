---
title: patternMap (PatternMapListType)-Element
description: Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu finden, und der andere wird verwendet, um die Zeichenfolge zu ändern, bevor der Dienst sie wieder in der Nachrichtenzeichenfolge platziert.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- patternMap-Element EventLog
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9206726bb960762d482c5a966fce6fb5a89b094249f247c2617c051d76d7e7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055968"
---
# <a name="patternmap-patternmaplisttype-element"></a>patternMap (PatternMapListType)-Element

Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu finden, und der andere wird verwendet, um die Zeichenfolge zu ändern, bevor der Dienst sie wieder in der Nachrichtenzeichenfolge platziert.

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

Das **patternMap-Element** wird vom komplexen [**PatternMapListType-Typ**](eventmanifestschema-patternmaplisttype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**patternMaps (NamedQueryType)**](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





