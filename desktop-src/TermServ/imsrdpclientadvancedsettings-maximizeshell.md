---
title: IMsRdpClientAdvancedSettings MaximizeShell-Eigenschaft
description: Gibt an, ob Programme, die mit der StartProgram-Eigenschaft gestartet werden, maximiert werden sollen.
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- MaximizeShell-Eigenschaft Remotedesktopdienste
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
- MaximizeShell-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , MaximizeShell-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00e73210407b6011c2cfd3dbb0ccc514306915a903710fa4ae90d7ebe2b3f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058998"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a>IMsRdpClientAdvancedSettings::MaximizeShell-Eigenschaft

Gibt an, ob Programme, die mit der [**StartProgram-Eigenschaft**](imstscsecuredsettings-startprogram.md) gestartet werden, maximiert werden sollen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
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

 

 





