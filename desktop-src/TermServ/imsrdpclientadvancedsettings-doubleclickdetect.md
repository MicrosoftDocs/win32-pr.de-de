---
title: IMsRdpClientAdvancedSettings DoubleClickDetect-Eigenschaft
description: Gibt an, ob der Client Doppelklicks für den Server identifiziert.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- DoubleClickDetect-Eigenschaft Remotedesktopdienste
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
- DoubleClickDetect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , DoubleClickDetect-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2d7a292bf307ffeac538cafd31dc7fb3ceeb1a54b1e768239ee169b04e0fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608735"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a>IMsRdpClientAdvancedSettings::D oubleClickDetect-Eigenschaft

Gibt an, ob der Client Doppelklicks für den Server identifiziert.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf 0 fest, um das Feature zu deaktivieren, oder einen Wert ungleich 0 (null), um das Feature zu aktivieren.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
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

 

 





