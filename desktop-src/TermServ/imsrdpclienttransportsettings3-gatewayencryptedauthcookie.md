---
title: IMsRdpClientTransportSettings3 gatewayverschlüsseltedauthcookie (Eigenschaft)
description: Das verschlüsselte Authentifizierungs Cookie.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Gatewayverschlüsseltedauthcookie-Eigenschaft Remotedesktopdienste
- Gatewayverschlüsseltedauthcookie-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, gatewayverschlüsseltedauthcookie (Eigenschaft)
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
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340687"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a>IMsRdpClientTransportSettings3:: gatewayverschlüsseltedauthcookie (Eigenschaft)

Das verschlüsselte Authentifizierungs Cookie. Die Größe der Eigenschaft wird durch die [**gatewayverschlüsseltedauthcookiesize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) -Eigenschaft angegeben.

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

Das neue verschlüsselte Authentifizierungs Cookie.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Gatewayverschlüsseltedauthcookiesize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





