---
title: Imstscax Connect-Methode
description: Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Connect-Methode Remotedesktopdienste
- Connect-Methode Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Connect-Methode
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
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949623"
---
# <a name="imstscaxconnect-method"></a>Imstscax:: Connect-Methode

Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.

## <a name="syntax"></a>Syntax


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Die einzige erforderliche Eigenschaft ist der Servername. Weitere Informationen finden Sie in der [**Server**](imstscax-server.md) -Eigenschaft.

Das-Steuerelement stellt eine asynchrone Verbindung her, sodass eine Rückgabe von einem Connect-Befehl nur anzeigt, dass die Verbindung erfolgreich initiiert wurde, und nicht, dass Sie abgeschlossen wurde. Sie sollten auf Ereignisse auf der [**imstscaxevents**](imstscaxevents-interface.md) -Schnittstelle reagieren, um zu bestimmen, wann das Steuerelement erfolgreich eine Verbindung hergestellt hat (oder ob es getrennt wurde).

Diese Methode gibt " **E \_ Fail** " zurück, wenn Sie aufgerufen wird, während das Steuerelement bereits verbunden ist oder sich im Verbindungs Zustand befindet.

Nachdem **Connect** aufgerufen wurde, können die meisten Steuerelement Eigenschaften erst dann festgelegt werden, wenn das Steuerelement in den getrennten Zustand zurückkehrt.

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

[**Trennen**](imstscax-disconnect.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





