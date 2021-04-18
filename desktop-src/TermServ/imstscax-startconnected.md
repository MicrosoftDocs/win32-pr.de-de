---
title: Imstscax startconnected (Eigenschaft)
description: Gibt an, ob das-Steuerelement die Server Verbindung des Remotedesktop-Sitzungshost (RD-Sitzungshost) unmittelbar nach dem Start herstellen soll.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Startconnected-Eigenschaften Remotedesktopdienste
- Startconnected-Eigenschaften Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, startconnected-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340977"
---
# <a name="imstscaxstartconnected-property"></a>Imstscax:: startconnected (Eigenschaft)

Gibt an, ob das-Steuerelement die Server Verbindung des Remotedesktop-Sitzungshost (RD-Sitzungshost) unmittelbar nach dem Start herstellen soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf **true** fest, wenn das Steuerelement beim Start sofort eine Verbindung herstellen soll, und andernfalls **false** .

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist besonders nützlich, wenn die Steuerelement Eigenschaften in der Parameterliste eines <OBJECT> Tags anstelle von Skript aufrufen festgelegt werden.

Diese Eigenschaft kann nur verwendet werden, wenn der Servername auch mit der Server-Eigenschaft angegeben wird. Dieser Parameter muss festgelegt werden, bevor das-Steuerelement beispielsweise gestartet wird, indem es in der Parameterliste eines Tags eingeschlossen wird, <OBJECT> Wenn das Steuerelement auf einer Webseite verwendet wird.

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

[Einbetten des Remotedesktop ActiveX-Steuer Elements in eine Webseite](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





