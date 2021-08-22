---
title: opcode (OpcodeListType)-Element
description: Enthält einen numerischen Wert, der die Aktivität oder einen Punkt innerhalb einer Aktivität identifiziert, die die Anwendung ausgeführt hat, als sie das Ereignis ausgelöst hat (z. B. Initialisierung oder Schließen).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- opcode-Element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10d7ae91d29f3bee72ef43b11b9f30f6229d4a43df4ace213d943b333bffd3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136243"
---
# <a name="opcode-opcodelisttype-element"></a>opcode (OpcodeListType)-Element

Enthält einen numerischen Wert, der die Aktivität oder einen Punkt innerhalb einer Aktivität identifiziert, die die Anwendung ausgeführt hat, als sie das Ereignis ausgelöst hat (z. B. Initialisierung oder Schließen).

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

Das **opcode-Element** wird vom komplexen [**OpcodeListType-Typ**](eventmanifestschema-opcodelisttype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Übergeordnete Elemente**
</dt> <dt>

[**opcodes (TaskType)**](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[**opcodes (ProviderType)**](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[**opcodes (MetadataType)**](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





