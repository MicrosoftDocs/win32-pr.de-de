---
title: Imsrdpclient getvirtualchanneloptions-Methode
description: Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Getvirtualchanneloptions-Methode Remotedesktopdienste
- Getvirtualchanneloptions-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
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
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346758"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a>Imsrdpclient:: getvirtualchanneloptions-Methode

Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Channame* \[ in\]
</dt> <dd>

Der Name eines virtuellen Kanals, der im Aufrufen der Methode " [**kreatevirtualchannels**](imstscax-createvirtualchannels.md) " angegeben wurde.

</dd> <dt>

*pchanoptions* \[ vorgenommen\]
</dt> <dd>

Die Optionen, die für den durch den *channame* -Parameter angegebenen virtuellen Kanal festgelegt wurden. Eine Beschreibung möglicher Optionen finden Sie unter [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**"Kreatevirtualchannels"**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**Setvirtualchanneloptions**](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





