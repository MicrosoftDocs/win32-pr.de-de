---
title: IMsRdpClientAdvancedSettings5 RedirectPOSDevices (Eigenschaft)
description: Legt die Konfiguration für die Point of Service-Geräteumleitung fest oder ruft sie ab.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- RedirectPOSDevices-Remotedesktopdienste
- RedirectPOSDevices-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , RedirectPOSDevices-Eigenschaft
- RedirectPOSDevices-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , RedirectPOSDevices-Eigenschaft
- RedirectPOSDevices-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , RedirectPOSDevices-Eigenschaft
- RedirectPOSDevices-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , RedirectPOSDevices-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4279d4edd5bc7667f54472d5d06eaaaf089da4420756eef2d951e5ac8561922c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941620"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a>IMsRdpClientAdvancedSettings5::RedirectPOSDevices (Eigenschaft)

Legt die Konfiguration für die Point of Service-Geräteumleitung fest oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt den Point of Service-Geräteumleitungsmodus auf **TRUE** oder **FALSE fest.** Wenn diese Option auf **TRUE festgelegt** ist, ist der Point of Service-Geräteumleitungsmodus aktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





