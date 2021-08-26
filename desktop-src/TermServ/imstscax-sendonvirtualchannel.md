---
title: IMsTscAx-Methode "SendOnVirtualChannel"
description: Sendet Daten an den server Remotedesktop-Sitzungshost (RD-Sitzungshost) über einen virtuellen Kanal, der zuvor mit der CreateVirtualChannels-Methode erstellt wurde.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- SendOnVirtualChannel-Methode Remotedesktopdienste
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
- SendOnVirtualChannel-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , SendOnVirtualChannel-Methode
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03c5b84ff9cb272d5560f3b6588301a05a3e9a003db1b28f841a77b2e0618b37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125300"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>IMsTscAx::SendOnVirtualChannel-Methode

Sendet Daten an den server Remotedesktop-Sitzungshost (RD-Sitzungshost) über einen virtuellen Kanal, der zuvor mit der [**CreateVirtualChannels-Methode**](imstscax-createvirtualchannels.md) erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ChanName* \[ In\]
</dt> <dd>

Der Name des virtuellen Kanals, der im Aufruf von [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)angegeben wurde.

</dd> <dt>

*ChanData* \[ In\]
</dt> <dd>

Die Daten, die über den virtuellen Kanal im **BSTR-Format** gesendet werden sollen. Es gibt keine Einschränkung, dass diese Daten NULL-terminierte Zeichenfolgen sein müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Informationen zu Namenseinschränkungen für virtuelle Kanäle finden Sie unter [Clientregistrierung](virtual-channel-client-registration.md) für virtuelle Kanäle.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx ist als 8C11EFAE-92C3-11D1-BC1E-00C04FA31489 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





