---
title: IMsTscAx-Eigenschaft "StartConnected"
description: Gibt an, ob das Steuerelement die Remotedesktop-Sitzungshost (RD-Sitzungshost)-Serververbindung sofort nach dem Start herstellt.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- StartConnected-Eigenschaft Remotedesktopdienste
- StartConnected-Eigenschaft Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
- StartConnected-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , StartConnected-Eigenschaft
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
ms.openlocfilehash: 9bdae5535d079335354306e47ed8378fa09450d9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880056"
---
# <a name="imstscaxstartconnected-property"></a>IMsTscAx::StartConnected-Eigenschaft

Gibt an, ob das Steuerelement die Remotedesktop-Sitzungshost (RD-Sitzungshost)-Serververbindung sofort nach dem Start herstellt.

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

Legen Sie diesen Parameter auf **TRUE** fest, wenn das Steuerelement beim Start sofort eine Verbindung herstellen soll, **andernfalls FALSE.**

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist am nützlichsten, wenn die Steuerelementeigenschaften nicht &lt; über Skriptaufrufe, sondern in der Parameterliste eines OBJECT-Tags festgelegt &gt; werden.

Diese Eigenschaft kann nur verwendet werden, wenn der Servername auch mithilfe der Servereigenschaft angegeben wird. Dieser Parameter muss festgelegt werden, bevor das Steuerelement gestartet wird, z. B. durch Einschließen in die Parameterliste eines &lt; &gt; OBJECT-Tags, wenn das Steuerelement von einer Webseite verwendet wird.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx ist als 8C11EFAE-92C3-11D1-BC1E-00C04FA31489 definiert.<br/>            |



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

[Einbetten des Remotedesktop ActiveX-Steuerelements in eine Webseite](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





