---
title: IMsTscAxEvents OnNetworkStatusChanged-Methode
description: Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. | IMsTscAxEvents OnNetworkStatusChanged-Methode
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- OnNetworkStatusChanged-Remotedesktopdienste
- OnNetworkStatusChanged-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnNetworkStatusChanged-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c139dc314453d6ad921471857410285813afc9c9b48691bcc9c82bf33c8b517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138403"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>IMsTscAxEvents::OnNetworkStatusChanged-Methode

Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.

## <a name="syntax"></a>Syntax


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*qualityLevel* \[ In\]
</dt> <dd>

Gibt die neue Verbindungsgeschwindigkeit an. Dies ist einer der folgenden Werte.

<dt>

1
</dt> <dd>

Weniger als 512 Kilobyte pro Sekunde (KBit/s).

</dd> <dt>

2
</dt> <dd>

512 bis 1.999 KBit/s.

</dd> <dt>

3
</dt> <dd>

2.000 bis 9.999 KBit/s.

</dd> <dt>

4
</dt> <dd>

Größer als oder gleich 10.000 KBit/s.

</dd> </dl> </dd> <dt>

*Bandbreite* \[ In\]
</dt> <dd>

Gibt die Verbindungsbandbreite an.

</dd> <dt>

*rtt* \[ In\]
</dt> <dd>

Gibt die Verbindungslatenz an.

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
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





