---
description: Diese Klasse ist die Ereignistypklasse für ALPC-Empfangsnachrichtenereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98a565ea445ddd803ce217abca3993c2561d464829635bbb1a546824f27c3b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070360"
---
# <a name="alpc_receive_message-class"></a>ALPC \_ Receive \_ Message-Klasse

Diese Klasse ist die Ereignistypklasse für ALPC-Empfangsnachrichtenereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Member

Die **ALPC \_ Receive \_ Message-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ALPC \_ Receive \_ Message-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nachrichtenbezeichner.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




