---
title: Imsrdpclient extendeddisconnecverrat (Eigenschaft)
description: Enthält erweiterte Informationen über den Grund für die Trennung der Verbindung.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518839"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a>Imsrdpclient:: extendeddisconnecverrat (Eigenschaft)

Enthält erweiterte Informationen über den Grund für die Trennung der Verbindung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf den [**extendeddisconnecweroncode**](extendeddisconnectreasoncode.md) -Wert, der den Grund für die Trennung der Verbindung des Clients angibt.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

In der Regel wird diese Methode im [**imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md) -Ereignishandler aufgerufen, um zusätzliche Informationen über das Ereignis zum Trennen der Verbindung abzurufen.

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

[**Imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





