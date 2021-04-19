---
title: Imstscaxevents OnAutoReconnecting2-Methode
description: Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet. | Imstscaxevents OnAutoReconnecting2-Methode
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting2-Methode Remotedesktopdienste
- OnAutoReconnecting2-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, OnAutoReconnecting2-Methode
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
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353321"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>Imstscaxevents:: OnAutoReconnecting2-Methode

Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet. Dies ist eine erweiterte Version der [**onautoreconnecting**](-imstscaxevents--onautoreconnecting.md) -Methode.

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

*disconnecverrat* \[ in\]
</dt> <dd>

Code, der den Grund für das letzte Trennen der Sitzung beschreibt.

</dd> <dt>

*NetworkAvailable* \[ in\]
</dt> <dd>

Gibt an, ob das Netzwerk verfügbar ist.

</dd> <dt>

*Anzahl* \[ der Versuche in\]
</dt> <dd>

Anzahl der Versuche, die im aktuellen automatischen erneuten Verbindungsvorgang durchgeführt wurden. Diese Anzahl wird für jeden erfolgten Versuch um eins erhöht.

</dd> <dt>

*maxder-Anzahl* \[ in\]
</dt> <dd>

Die maximale Anzahl der Versuche, die beim aktuellen automatischen erneuten Verbindungsvorgang durchgeführt werden.

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

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





