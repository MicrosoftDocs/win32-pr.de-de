---
title: IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookieSize (Eigenschaft)
description: Die Größe der GatewayEncryptedAuthCookie-Eigenschaft in Zeichen.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedAuthCookieSize-Remotedesktopdienste
- GatewayEncryptedAuthCookieSize-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste , GatewayEncryptedAuthCookieSize (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e26e4d15c134bcd8a2dd5bbf74b574f38ce56627d0f7e7840547ed1d56a67a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606935"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a>IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookieSize (Eigenschaft)

Die Größe der [**GatewayEncryptedAuthCookie-Eigenschaft in**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) Zeichen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein **ULONG-Wert,** der den neuen Größenwert enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





