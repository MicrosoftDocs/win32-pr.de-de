---
title: Imstscax-Server Eigenschaft (asptlb. h)
description: Gibt den Namen des Servers an, mit dem das aktuelle Steuerelement verbunden ist.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Server Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949499"
---
# <a name="imstscaxserver-property"></a>Imstscax:: Server-Eigenschaft

Gibt den Namen des Servers an, mit dem das aktuelle Steuerelement verbunden ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des neuen Servers. Dieser Parameter kann ein DNS-Name oder eine IP-Adresse sein.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methoden erfolgreich sind, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss festgelegt werden, bevor die [**Connect**](imstscax-connect.md) -Methode aufgerufen wird. Es ist die einzige Eigenschaft, die vor dem Herstellen einer Verbindung festgelegt werden muss.

Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet. Diese Eigenschaft gibt **E \_ Fail** zurück, wenn Sie aufgerufen wird, wenn das Steuerelement verbunden ist. Mithilfe der [**verbundenen**](imstscax-connected.md) Eigenschaft können Sie den Status "verbunden" überprüfen.

Mit dieser Methode wird der erforderliche Arbeitsspeicher für den Puffer zugewiesen, auf den der *pserver* -Parameter verweist. Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden. Dies ist für Visual Basic-und Skript Clients nicht erforderlich.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Header<br/>                   | <dl> <dt>Asptlb. h</dt> </dl>    |
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

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

