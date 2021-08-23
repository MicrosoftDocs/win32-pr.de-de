---
description: Diese Klasse ist die Ereignistypklasse für ALPC-Sendenachrichtenereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: ALPC_Send_Message-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8a3e53e514f80f89f1b1e97c1edde9b86add0db7a29de9443c5a1b48085a40fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070330"
---
# <a name="alpc_send_message-class"></a>ALPC \_ Send \_ Message-Klasse

Diese Klasse ist die Ereignistypklasse für ALPC-Sendenachrichtenereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Member

Die **ALPC \_ Send \_ Message-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ALPC \_ Send \_ Message-Klasse** verfügt über diese Eigenschaften.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




