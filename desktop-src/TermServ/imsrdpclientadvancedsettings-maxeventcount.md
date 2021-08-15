---
title: IMsRdpClientAdvancedSettings maxEventCount-Eigenschaft
description: Diese Eigenschaft wird nicht unterstützt. | IMsRdpClientAdvancedSettings maxEventCount-Eigenschaft
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- maxEventCount-Eigenschaft Remotedesktopdienste
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
- maxEventCount-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , maxEventCount-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cb0ee5cb5d38f57619e54be56d3c6cab49641b9183f7771cefbbfaad0eec0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353029"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a>IMsRdpClientAdvancedSettings::maxEventCount-Eigenschaft

Diese Eigenschaft wird nicht unterstützt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neue Ereignisanzahl. Der Standardwert ist 100.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ FALSE zurück.**

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                                       |
| Ende des Supports (Server)<br/>    | Nicht unterstützt<br/>                                                                       |
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

 

 





