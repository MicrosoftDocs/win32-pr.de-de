---
title: IMsRdpClientAdvancedSettings6 AuthenticationType-Eigenschaft
description: Gibt den Authentifizierungstyp an, der für diese Verbindung verwendet wird.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der AuthenticationType-Eigenschaft
- AuthenticationType-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , AuthenticationType-Eigenschaft
- AuthenticationType-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , AuthenticationType-Eigenschaft
- AuthenticationType-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , AuthenticationType-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35fe580ce780a51c3a203ff22b4043bbbe423dc4e821de1aaa2ba378485e719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138843"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a>IMsRdpClientAdvancedSettings6::AuthenticationType-Eigenschaft

Gibt den Authentifizierungstyp an, der für diese Verbindung verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt einen Wert, der den Für diese Verbindung verwendeten Authentifizierungstyp angibt. Dies kann einer der folgenden Werte sein.

<dt>

0
</dt> <dd>

Es wird keine Authentifizierung verwendet.

</dd> <dt>

1
</dt> <dd>

Die Zertifikatauthentifizierung wird verwendet.

</dd> <dt>

2
</dt> <dd>

Die Kerberos-Authentifizierung wird verwendet.

</dd> <dt>

3
</dt> <dd>

Sowohl die Zertifikat- als auch die Kerberos-Authentifizierung werden verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





