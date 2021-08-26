---
description: Diese Klasse ist die Ereignistypklasse für ALPC wait for new message events (ALPC-Warte auf neue Nachrichtenereignisse). Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67b3e52e59345eea95db7485e0764f31f88669241159ffc857d46cf230a5e8b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901550"
---
# <a name="alpc_wait_for_new_message-class"></a>ALPC \_ Wait For New \_ \_ \_ Message-Klasse

Diese Klasse ist die Ereignistypklasse für ALPC wait for new message events (ALPC-Warte auf neue Nachrichtenereignisse).

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a>Member

Die **ALPC \_ Wait For \_ New \_ \_ Message-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ALPC \_ Wait For \_ New \_ \_ Message-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**IsServerPort**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Port ein Serverport ist.

</dd> <dt>

**Portname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Namen des Ports enthält, auf den ALPC wartet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




