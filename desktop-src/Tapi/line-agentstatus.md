---
description: Die TAPI-Line- \_ agentstatusmeldung wird gesendet, wenn sich der Status eines ACD-Agents in einer von der Anwendung geöffneten Zeile ändert. Die Anwendung kann linegetagentstatus aufrufen, um den aktuellen Status des Agents zu ermitteln.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: LINE_AGENTSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365717"
---
# <a name="line_agentstatus-message"></a>Zeile \_ Agentstatus-Meldung

Die TAPI- **line- \_ agentstatusmeldung** wird gesendet, wenn sich der Status eines ACD-Agents in einer von der Anwendung geöffneten Zeile ändert. Die Anwendung kann [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) aufrufen, um den aktuellen Status des Agents zu ermitteln.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät, auf dem sich der Agentstatus geändert hat.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Bezeichner der Adresse in der Zeile, in der sich der Agentstatus geändert hat. Ein Adress Bezeichner ist dauerhaft einer Adresse zugeordnet. der Bezeichner bleibt bei Betriebssystem Upgrades konstant.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den Agent-Status an, der geändert wurde. kann eine Kombination aus [**lineagentstatus- \_ Konstanten**](lineagentstatus--constants.md)sein.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Wenn *dwParam2* das Status Bit lineagentstatus enthält \_ , gibt *dwParam3* den neuen Wert des Elements **dwstate** in [**lineagentstatus**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)an. Andernfalls wird dieser Parameter auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeile \_ Agentstatus** -Nachricht wird nicht an Anwendungen gesendet, die ältere Versionen von TAPI unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lineagentstatus**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




