---
title: IMsTscAx Verbinden-Methode
description: Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das Steuerelement festgelegt sind.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Verbinden-Methode Remotedesktopdienste
- Verbinden-Methode Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , Verbinden-Methode
- Verbinden-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , Verbinden-Methode
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4372b19c9dba51714c6927d5e54468e143033689bfd9c74db78bbff8812e45ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513110"
---
# <a name="imstscaxconnect-method"></a>IMsTscAx::Verbinden-Methode

Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das Steuerelement festgelegt sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Die einzige erforderliche Eigenschaft ist der Servername. Weitere Informationen [](imstscax-server.md) finden Sie in der Server-Eigenschaft.

Das Steuerelement stellt eine asynchrone Verbindung her, sodass eine Rückgabe von einem Verbinden Aufruf nur angibt, dass die Verbindung erfolgreich initiiert wurde und nicht, dass sie abgeschlossen wurde. Sie sollten auf Ereignisse auf der [**IMsTscAxEvents-Schnittstelle**](imstscaxevents-interface.md) reagieren, um zu bestimmen, wann das Steuerelement erfolgreich verbunden wurde (oder getrennt wurde).

Diese Methode gibt **E \_ FAIL** zurück, wenn sie aufgerufen wird, während das Steuerelement bereits verbunden ist oder sich im Verbindungszustand befindet.

Nachdem **Verbinden** aufgerufen wurde, können die meisten Steuerelementeigenschaften nicht mehr festgelegt werden, bis das Steuerelement in den nicht verbundenen Zustand zurückkehrt.

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

[**Trennen**](imstscax-disconnect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





