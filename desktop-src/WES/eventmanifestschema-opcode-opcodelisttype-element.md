---
title: Opcode (opcodelisttype)-Element
description: Enthält einen numerischen Wert, der die Aktivität oder einen Punkt innerhalb einer Aktivität identifiziert, der von der Anwendung beim Auslösung des Ereignisses (z. b. Initialisierung oder schließen) durchgeführt wurde.
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- Opcode-Element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106028"
---
# <a name="opcode-opcodelisttype-element"></a>Opcode (opcodelisttype)-Element

Enthält einen numerischen Wert, der die Aktivität oder einen Punkt innerhalb einer Aktivität identifiziert, der von der Anwendung beim Auslösung des Ereignisses (z. b. Initialisierung oder schließen) durchgeführt wurde.

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

Das **Opcode** -Element wird durch den komplexen [**opcodelisttype**](eventmanifestschema-opcodelisttype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnete Elemente**
</dt> <dt>

[**Opcodes (TaskType)**](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[**Opcodes (ProviderType)**](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[**Opcodes (metadataType)**](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





