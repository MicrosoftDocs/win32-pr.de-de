---
title: Imstscaxevents onchannelreceiveddata-Methode
description: Wird aufgerufen, wenn der Client Daten eines Skript fähigen virtuellen Kanals empfängt.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Onchannelreceiveddata-Methode Remotedesktopdienste
- Onchannelreceiveddata-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onchannelreceiveddata-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103523"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>Imstscaxevents:: onchannelreceiveddata-Methode

Wird aufgerufen, wenn der Client Daten eines Skript fähigen virtuellen Kanals empfängt.

## <a name="syntax"></a>Syntax


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*channame* \[ in\]
</dt> <dd>

Der Name des virtuellen Kanals, auf dem Daten empfangen wurden. Dieser Name entspricht einem der Kanäle, die durch den Aufrufen von [**imstscax:: foratevirtualchannels**](imstscax-createvirtualchannels.md)erstellt wurden.

</dd> <dt>

*Daten* \[ in\]
</dt> <dd>

Die Daten, die auf dem Skript fähigen virtuellen Kanal empfangen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu diesem Ereignis finden Sie unter [Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





