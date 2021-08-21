---
title: IMsTscAxEvents OnAutoReconnecting2-Methode
description: Wird aufgerufen, wenn ein Client gerade eine Sitzung automatisch mit einem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) verbindet. | IMsTscAxEvents OnAutoReconnecting2-Methode
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting2-Methode Remotedesktopdienste
- OnAutoReconnecting2-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnAutoReconnecting2-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194c21fc8ddc6f93ac4816752956f8de5a1d5df71b3af98ddadf8aba48e421a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512490"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>IMsTscAxEvents::OnAutoReconnecting2-Methode

Wird aufgerufen, wenn ein Client gerade eine Sitzung automatisch mit einem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) verbindet. Dies ist eine erweiterte Version der [**OnAutoReconnecting-Methode.**](-imstscaxevents--onautoreconnecting.md)

## <a name="syntax"></a>Syntax


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*disconnectReason* \[ In\]
</dt> <dd>

Code, der den Grund für die letzte Sitzungstrennung beschreibt.

</dd> <dt>

*networkAvailable* \[ In\]
</dt> <dd>

Gibt an, ob das Netzwerk verfügbar ist.

</dd> <dt>

*attemptCount* \[ In\]
</dt> <dd>

Anzahl der Versuche, die im aktuellen prozess der automatischen Wiederherstellung der Verbindung unternommen wurden. Diese Anzahl erhöht sich für jeden unternommenen Versuch um eins.

</dd> <dt>

*maxAttemptCount* \[ In\]
</dt> <dd>

Die maximale Anzahl von Versuchen, die im aktuellen prozess der automatischen Wiederherstellung der Verbindung unternommen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





