---
title: IMsRdpClientTransportSettings2-GatewayEncryptedOtpCookie-Eigenschaft
description: Gibt das verschlüsselte Einmalkennwortcookie (One-Time Password, OTP) an oder ruft es ab.
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedOtpCookie-Eigenschaft Remotedesktopdienste
- GatewayEncryptedOtpCookie-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste , GatewayEncryptedOtpCookie-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55f7f1cf0d73d6e18a119207e57e0aaf93729d5b25a7184f4a55110d045b189a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770740"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a>IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie-Eigenschaft

Gibt das verschlüsselte Einmalkennwortcookie (One-Time Password, OTP) an oder ruft es ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt das verschlüsselte OTP-Cookie an oder ruft es ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2E0489009319 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





