---
title: IMsRdpClientAdvancedSettings4 AuthenticationLevel-Eigenschaft
description: Gibt die Authentifizierungsebene an, die für die Verbindung verwendet werden soll.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , AuthenticationLevel-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01bed28e22f22e1dd14da4941027d5a99550cee49a45f40bf887ab27d7b940d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352567"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a>IMsRdpClientAdvancedSettings4::AuthenticationLevel-Eigenschaft

Gibt die Authentifizierungsebene an, die für die Verbindung verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Wert der **AuthenticationLevel-Eigenschaft.**

<dt>

0
</dt> <dd>

Keine Authentifizierung des Servers.

</dd> <dt>

1
</dt> <dd>

Die Serverauthentifizierung ist erforderlich und muss erfolgreich abgeschlossen werden, damit die Verbindung fortgesetzt werden kann.

</dd> <dt>

2
</dt> <dd>

Versuchen Sie, den Server zu authentifizieren. Wenn die Authentifizierung fehlschlägt, wird der Benutzer aufgefordert, die Verbindung abzubrechen oder ohne Serverauthentifizierung fortzufahren.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                                     |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings4 ist als FBA7F64E-7345-4405-AE50-FA4A763DC0DE definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





