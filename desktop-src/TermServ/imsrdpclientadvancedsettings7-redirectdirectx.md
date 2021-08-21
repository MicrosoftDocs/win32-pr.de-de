---
title: IMsRdpClientAdvancedSettings7 RedirectDirectX-Eigenschaft
description: Diese Eigenschaft wird nicht verwendet. | IMsRdpClientAdvancedSettings7 RedirectDirectX-Eigenschaft
ms.assetid: a027d8d7-994f-4b24-8c46-18651c8e200b
ms.tgt_platform: multiple
keywords:
- RedirectDirectX-Eigenschaft Remotedesktopdienste
- RedirectDirectX-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , RedirectDirectX-Eigenschaft
- RedirectDirectX-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , RedirectDirectX-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.RedirectDirectX
- IMsRdpClientAdvancedSettings7.get_RedirectDirectX
- IMsRdpClientAdvancedSettings7.put_RedirectDirectX
- IMsRdpClientAdvancedSettings8.RedirectDirectX
- IMsRdpClientAdvancedSettings8.get_RedirectDirectX
- IMsRdpClientAdvancedSettings8.put_RedirectDirectX
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb3b9db5badb8fb313d95cf04dc65681ff3f380dc1381e8b052ed7f2dee5c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130175"
---
# <a name="imsrdpclientadvancedsettings7redirectdirectx-property"></a>IMsRdpClientAdvancedSettings7::RedirectDirectX-Eigenschaft

Diese Eigenschaft wird nicht verwendet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectDirectX(
  [in]          VARIANT_BOOL fRedirectDirectX
);

HRESULT get_RedirectDirectX(
  [out, retval] VARIANT_BOOL *pfRedirectDirectX
);
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird nicht verwendet.

## <a name="error-codes"></a>Fehlercodes

Diese Eigenschaft wird nicht verwendet. Die Settermethode gibt immer **S \_ FALSE** zurück, und die Gettermethode gibt immer **E \_ NOTIMPL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 ist als 26036036-4010-4578-8091-0db9a1edf9c3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





