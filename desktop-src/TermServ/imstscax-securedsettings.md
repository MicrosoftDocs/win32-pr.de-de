---
title: Imstscax securedsettings (Eigenschaft)
description: Ruft einen imstscsecuredsettings-Schnittstellen Zeiger ab.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Securedsettings-Eigenschaft Remotedesktopdienste
- Securedsettings-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, securedsettings-Eigenschaft
- Securedsettings-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, securedsettings-Eigenschaft
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103683"
---
# <a name="imstscaxsecuredsettings-property"></a>Imstscax:: securedsettings-Eigenschaft

Ruft einen [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstellen Zeiger ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstellen Zeiger.

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement auf einer Webseite gehostet wird und die aktuelle Internet Explorer-URL-Sicherheitszone das Abrufen der Schnittstellen Adresse nicht zulässt, gibt diese Methode **E \_ Fail** zurück.

Einschränkungen bei der Verfügbarkeit der [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle finden Sie unter [**securedsettingsenabled**](imstscax-securedsettingsenabled.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
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
</dt> <dt>

[**Imstscsecuredsettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





