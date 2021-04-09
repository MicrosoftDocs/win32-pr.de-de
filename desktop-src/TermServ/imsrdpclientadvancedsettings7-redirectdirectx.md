---
title: IMsRdpClientAdvancedSettings7 redirectdirectx (Eigenschaft)
description: Diese Eigenschaft wird nicht verwendet. | IMsRdpClientAdvancedSettings7 redirectdirectx (Eigenschaft)
ms.assetid: a027d8d7-994f-4b24-8c46-18651c8e200b
ms.tgt_platform: multiple
keywords:
- Redirectdirectx-Eigenschaft Remotedesktopdienste
- Redirectdirectx-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, redirectdirectx-Eigenschaft
- Redirectdirectx-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, redirectdirectx-Eigenschaft
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
ms.openlocfilehash: 68f7da3ecea0c5a5a77a45b48ff24038a5517dc1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869851"
---
# <a name="imsrdpclientadvancedsettings7redirectdirectx-property"></a>IMsRdpClientAdvancedSettings7:: redirectdirectx-Eigenschaft

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

Diese Eigenschaft wird nicht verwendet. Die Setter-Methode gibt **immer \_ false** zurück, und die Getter-Methode gibt immer **E \_ notimpl** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





