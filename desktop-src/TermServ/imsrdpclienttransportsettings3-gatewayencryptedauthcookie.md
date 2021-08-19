---
title: IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookie-Eigenschaft
description: Das verschlüsselte Authentifizierungscookie.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedAuthCookie-Eigenschaft Remotedesktopdienste
- GatewayEncryptedAuthCookie-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste , GatewayEncryptedAuthCookie-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c05a83d3b6891bfb8173a45935dcd73ad9ad65db5643d093306eda6e5d1cb20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000880"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a>IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie-Eigenschaft

Das verschlüsselte Authentifizierungscookie. Die Größe der Eigenschaft wird von der [**GatewayEncryptedAuthCookieSize-Eigenschaft**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) angegeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a>Eigenschaftswert

Das neue verschlüsselte Authentifizierungscookie.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





