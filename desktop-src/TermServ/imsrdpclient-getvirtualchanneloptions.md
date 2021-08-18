---
title: IMsRdpClient GetVirtualChannelOptions-Methode
description: Ruft die für einen virtuellen Kanal festgelegten Optionen ab.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- GetVirtualChannelOptions-Methode Remotedesktopdienste
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
- GetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , GetVirtualChannelOptions-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d51ad6ccd1924c78817f76f385d65e1963b68c1b1329c3d6ba924f25a827a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059088"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a>IMsRdpClient::GetVirtualChannelOptions-Methode

Ruft die für einen virtuellen Kanal festgelegten Optionen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ChanName* \[ In\]
</dt> <dd>

Der Name eines virtuellen Kanals, der im Aufruf der [**CreateVirtualChannels-Methode**](imstscax-createvirtualchannels.md) angegeben wurde.

</dd> <dt>

*pOptions* \[ out\]
</dt> <dd>

Die optionen, die für den virtuellen Kanal festgelegt sind, der durch den *Parameter "HanName"* angegeben wird. Eine Beschreibung der möglichen Optionen finden Sie unter [**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**\_KANAL-DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





