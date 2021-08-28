---
title: IMsRdpClientAdvancedSettings SmoothScroll (Eigenschaft)
description: Diese Eigenschaft wird nicht unterstützt. | IMsRdpClientAdvancedSettings SmoothScroll (Eigenschaft)
ms.assetid: 7f1ce439-0b6e-4426-8dd6-3748509130e1
ms.tgt_platform: multiple
keywords:
- SmoothScroll-Remotedesktopdienste
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
- SmoothScroll-Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , SmoothScroll-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmoothScroll
- IMsRdpClientAdvancedSettings.get_SmoothScroll
- IMsRdpClientAdvancedSettings.put_SmoothScroll
- IMsRdpClientAdvancedSettings2.SmoothScroll
- IMsRdpClientAdvancedSettings2.get_SmoothScroll
- IMsRdpClientAdvancedSettings2.put_SmoothScroll
- IMsRdpClientAdvancedSettings3.SmoothScroll
- IMsRdpClientAdvancedSettings3.get_SmoothScroll
- IMsRdpClientAdvancedSettings3.put_SmoothScroll
- IMsRdpClientAdvancedSettings4.SmoothScroll
- IMsRdpClientAdvancedSettings4.get_SmoothScroll
- IMsRdpClientAdvancedSettings4.put_SmoothScroll
- IMsRdpClientAdvancedSettings5.SmoothScroll
- IMsRdpClientAdvancedSettings5.get_SmoothScroll
- IMsRdpClientAdvancedSettings5.put_SmoothScroll
- IMsRdpClientAdvancedSettings6.SmoothScroll
- IMsRdpClientAdvancedSettings6.get_SmoothScroll
- IMsRdpClientAdvancedSettings6.put_SmoothScroll
- IMsRdpClientAdvancedSettings7.SmoothScroll
- IMsRdpClientAdvancedSettings7.get_SmoothScroll
- IMsRdpClientAdvancedSettings7.put_SmoothScroll
- IMsRdpClientAdvancedSettings8.SmoothScroll
- IMsRdpClientAdvancedSettings8.get_SmoothScroll
- IMsRdpClientAdvancedSettings8.put_SmoothScroll
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58009b0f63e82439ad34ebe774f72dc4a4de443a87bbe0a300c7fcec0206118d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990270"
---
# <a name="imsrdpclientadvancedsettingssmoothscroll-property"></a>IMsRdpClientAdvancedSettings::SmoothScroll (Eigenschaft)

Diese Eigenschaft wird nicht unterstützt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SmoothScroll(
  [in]  LONG smoothScroll
);

HRESULT get_SmoothScroll(
  [out] LONG *psmoothScroll
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf 0 fest, um smooth scrolling oder einen Wert ungleich 0 (null) zu deaktivieren, um einen reibungslosen Bildlauf zu ermöglichen.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ FALSE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





