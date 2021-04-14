---
title: Imsrdpclient setvirtualchanneloptions-Methode
description: Legt die Optionen des virtuellen Kanals für das Remotedesktop ActiveX-Steuerelement fest.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Setvirtualchanneloptions-Methode Remotedesktopdienste
- Setvirtualchanneloptions-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391684"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>Imsrdpclient:: setvirtualchanneloptions-Methode

Legt die Optionen des virtuellen Kanals für das Remotedesktop ActiveX-Steuerelement fest.

Rufen Sie diese Methode nach dem Aufrufen der [**createvirtualchannels**](imstscax-createvirtualchannels.md) -Methode auf, aber vor dem Herstellen einer Verbindung mit der [**Connect**](imstscax-connect.md) -Methode. Mit dieser Methode werden zusätzliche Optionen für virtuelle Kanäle festgelegt, die mit " **kreatevirtualchannels**" erstellt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Channame* \[ in\]
</dt> <dd>

Der Name des virtuellen Kanals, der im Aufrufen der Methode " [**kreatevirtualchannels**](imstscax-createvirtualchannels.md) " angegeben wurde.

</dd> <dt>

*chanoptions* \[ in\]
</dt> <dd>

Die Optionen, die für den durch den *channame* -Parameter angegebenen virtuellen Kanal festgelegt werden sollen. Eine Beschreibung möglicher Optionen finden Sie unter [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Ein Beispiel für die Verwendung dieser Methode wäre, den Kanal als persistente Remote Steuerung zu deklarieren, indem Sie die **Kanal \_ Option \_ \_ \_ persistentes** Flag für die Remote Steuerung festlegen. Dies bedeutet, dass der Kanal nicht geschlossen wird, wenn eine Remote Steuerung eine Verbindung mit der Sitzung herstellt, die mit dem Client verbunden ist, oder die Verbindung trennt. Weitere Informationen finden Sie unter [permanente virtuelle Kanäle für die Remote Steuerung](remote-control-persistent-virtual-channels.md).

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

[**Getvirtualchanneloptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





