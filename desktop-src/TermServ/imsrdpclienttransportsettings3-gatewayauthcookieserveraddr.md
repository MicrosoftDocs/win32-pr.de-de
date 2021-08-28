---
title: IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr-Eigenschaft
description: Die Serveradresse für die cookiebasierte Authentifizierung.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- GatewayAuthCookieServerAddr-Eigenschaft Remotedesktopdienste
- GatewayAuthCookieServerAddr-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste , GatewayAuthCookieServerAddr-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330a1ddb15d548988c23f8140ce848f7f68be5d1deb17fc51bd88eed23b9eec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000920"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a>IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr-Eigenschaft

Die Serveradresse für die cookiebasierte Authentifizierung.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Serveradresse für die cookiebasierte Authentifizierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





