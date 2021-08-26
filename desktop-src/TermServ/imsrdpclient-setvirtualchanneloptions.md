---
title: IMsRdpClient SetVirtualChannelOptions-Methode
description: Legt die Optionen für den virtuellen Kanal für das Remotedesktop ActiveX-Steuerelement fest.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- SetVirtualChannelOptions-Methode Remotedesktopdienste
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
- SetVirtualChannelOptions-Methode Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , SetVirtualChannelOptions-Methode
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
ms.openlocfilehash: 804d4bde2fec9cb6273cc78f79d733f61a08772746439aa1cbb6e7b2d3c29716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871581"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>IMsRdpClient::SetVirtualChannelOptions-Methode

Legt die Optionen für den virtuellen Kanal für das Remotedesktop ActiveX-Steuerelement fest.

Rufen Sie diese Methode auf, nachdem Sie die [**CreateVirtualChannels-Methode**](imstscax-createvirtualchannels.md) aufgerufen haben, aber bevor Sie eine Verbindung mit der [**Verbinden-Methode**](imstscax-connect.md) herstellen. Diese Methode legt zusätzliche Optionen für virtuelle Kanäle fest, die mit **CreateVirtualChannels** erstellt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ChanName* \[ In\]
</dt> <dd>

Der Name des virtuellen Kanals, der im Aufruf der [**CreateVirtualChannels-Methode**](imstscax-createvirtualchannels.md) angegeben wurde.

</dd> <dt>

*options* \[ In\]
</dt> <dd>

Die Optionen, die für den virtuellen Kanal festgelegt werden sollen, der durch den *Parameter "ChanName"* angegeben wird. Eine Beschreibung der möglichen Optionen finden Sie unter [**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Ein Beispiel für die Verwendung dieser Methode wäre das Deklarieren des Kanals als remote control persistent durch Festlegen des **CHANNEL OPTION REMOTE CONTROL \_ \_ \_ PERSISTENT-Flags. \_** Dies bedeutet, dass der Kanal nicht geschlossen wird, wenn eine Remotesteuerung eine Verbindung mit der Mit dem Client verbundenen Sitzung herstellt oder diese trennt. Weitere Informationen finden Sie unter [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**\_KANAL-DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





