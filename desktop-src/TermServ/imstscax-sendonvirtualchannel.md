---
title: Imstscax sendonvirtualchannel-Methode
description: Sendet Daten an den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) über einen virtuellen Kanal, der zuvor mithilfe der Methode "| atevirtualchannels" erstellt wurde.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Sendonvirtualchannel-Methode Remotedesktopdienste
- Sendonvirtualchannel-Methode Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
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
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475612"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>Imstscax:: sendonvirtualchannel-Methode

Sendet Daten an den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) über einen virtuellen Kanal, der zuvor mithilfe der Methode "| [**atevirtualchannels**](imstscax-createvirtualchannels.md) " erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Channame* \[ in\]
</dt> <dd>

Der Name des virtuellen Kanals, der im Aufrufen von " [**anatevirtualchannels**](imstscax-createvirtualchannels.md)" angegeben wurde.

</dd> <dt>

*Chandata* \[ in\]
</dt> <dd>

Die Daten, die über den virtuellen Kanal in **BSTR** -Form gesendet werden sollen. Es gibt keine Einschränkung, dass diese Daten Zeichen folgen mit null-terminierten Zeichen folgen müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Informationen zu Benennungs Einschränkungen für virtuelle Kanäle finden Sie unter [Virtual Channel Client-Registrierung](virtual-channel-client-registration.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
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

[**"Kreatevirtualchannels"**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





