---
description: Die TAPI-Zeilen- \_ agentspezifische Nachricht wird gesendet, wenn sich der Status eines ACD-Agents in einer Zeile ändert, die die Anwendung zurzeit geöffnet hat. Die Anwendung kann linegetagentstatus aufrufen, um den aktuellen Status des Agents zu ermitteln.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: LINE_AGENTSPECIFIC Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367734"
---
# <a name="line_agentspecific-message"></a>LINE- \_ agentspezifische Nachricht

Die TAPI- **Zeilen- \_ agentspezifische** Nachricht wird gesendet, wenn sich der Status eines ACD-Agents in einer Zeile ändert, die die Anwendung zurzeit geöffnet hat. Die Anwendung kann [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) aufrufen, um den aktuellen Status des Agents zu ermitteln.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Index im Array von handlererweiterungsbezeichnerwerten in der [**lineagentcaps**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) -Struktur der Handlererweiterung, der die Nachricht zugeordnet ist.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spezifisch für die Handlererweiterung. Im Allgemeinen wird dieser Wert verwendet, um die Anwendung dazu zu veranlassen, eine [**lineagentspecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) -Funktion aufzurufen, um weitere Details zur Nachricht abzurufen.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Spezifisch für die Handlererweiterung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeile \_ agentspecific** -Nachricht wird nicht an Anwendungen gesendet, die ältere Versionen von TAPI unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lineagentcaps**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineagentspecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




