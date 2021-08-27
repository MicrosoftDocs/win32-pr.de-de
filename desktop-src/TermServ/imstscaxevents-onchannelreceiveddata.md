---
title: IMsTscAxEvents OnChannelReceivedData-Methode
description: Wird aufgerufen, wenn der Client Daten in einem skriptfähigen virtuellen Kanal empfängt.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- OnChannelReceivedData-Methode Remotedesktopdienste
- OnChannelReceivedData-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnChannelReceivedData-Methode
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
ms.openlocfilehash: 72f411eae7e03f134f4adfd6fdc6108634e4e58c06bb8645e9f97f27e8489a3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125190"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>IMsTscAxEvents::OnChannelReceivedData-Methode

Wird aufgerufen, wenn der Client Daten in einem skriptfähigen virtuellen Kanal empfängt.

## <a name="syntax"></a>Syntax


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*chanName* \[ In\]
</dt> <dd>

Der Name des virtuellen Kanals, über den Daten empfangen wurden. Dieser Name entspricht einem der Kanäle, die durch den Aufruf von [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md)erstellt wurden.

</dd> <dt>

*Daten* \[ In\]
</dt> <dd>

Die auf dem skriptfähigen virtuellen Kanal empfangenen Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu diesem Ereignis finden Sie unter [Implementing Scriptable Virtual Channels using Remotedesktop-Webverbindung (Implementieren von skriptfähigen virtuellen Kanälen mit Remotedesktop-Webverbindung).](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





