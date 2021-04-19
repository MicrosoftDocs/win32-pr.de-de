---
title: Imstscaxevents onnetworkstatuschangi-Methode
description: Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. | Imstscaxevents onnetworkstatuschangi-Methode
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Onnetworkstatuschangi-Methode Remotedesktopdienste
- Onnetworkstatuschangi-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onnetworkstatuschangi-Methode
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
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363909"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>Imstscaxevents:: onnetworkstatuschangi-Methode

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

*qualitylevel* \[ in\]
</dt> <dd>

Gibt die neue Verbindungsgeschwindigkeit an. Dabei handelt es sich um einen der folgenden Werte.

<dt>

1
</dt> <dd>

Weniger als 512 Kilobyte pro Sekunde (Kbit/s).

</dd> <dt>

2
</dt> <dd>

512 bis 1.999 Kbit/s.

</dd> <dt>

3
</dt> <dd>

2.000 bis 9.999 Kbit/s.

</dd> <dt>

4
</dt> <dd>

Größer oder gleich 10.000 Kbit/s.

</dd> </dl> </dd> <dt>

*Bandbreite* \[ in\]
</dt> <dd>

Gibt die Verbindungs Bandbreite an.

</dd> <dt>

*RTT* \[ in\]
</dt> <dd>

Gibt die Verbindungs Latenz an.

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
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





