---
description: Die TAPI LINE AGENTSPECIFIC-Meldung wird gesendet, wenn sich der Status eines ACD-Agents in einer Zeile ändert, in der \_ die Anwendung derzeit geöffnet ist. Die Anwendung kann lineGetAgentStatus aufrufen, um den aktuellen Status des Agents zu ermitteln.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: LINE_AGENTSPECIFIC (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87b0e6f5c6c96842f70ebe46c0b72e33e6767c996fa2cc5b4d8e95ff0f08cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867160"
---
# <a name="line_agentspecific-message"></a>LINE \_ AGENTSPECIFIC-Meldung

Die TAPI **LINE \_ AGENTSPECIFIC-Meldung** wird gesendet, wenn sich der Status eines ACD-Agents in einer Zeile ändert, in der die Anwendung derzeit geöffnet ist. Die Anwendung kann [**lineGetAgentStatus aufrufen,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) um den aktuellen Status des Agents zu ermitteln.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Das Handle der Anwendung für das Liniengerät.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile des Aufrufs angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Index im Array von Handlererweiterungsbezeichnern in der [**LINEAGENTCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) der Handlererweiterung, der die Meldung zugeordnet ist.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spezifisch für die Handlererweiterung. Im Allgemeinen wird dieser Wert verwendet, um zu bewirken, dass die Anwendung eine [**lineAgentSpecific-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) aufruft, um weitere Details zur Nachricht zu erhalten.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Spezifisch für die Handlererweiterung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ AGENTSPECIFIC-Meldung** wird nicht an Anwendungen gesendet, die ältere Versionen von TAPI unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




