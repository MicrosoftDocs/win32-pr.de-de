---
title: IMsRdpClientAdvancedSettings EnableWindowsKey-Eigenschaft
description: Gibt an, ob der Windows Schlüssel in der Remotesitzung verwendet werden kann.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- EnableWindowsKey-Eigenschaft Remotedesktopdienste
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
- EnableWindowsKey-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , EnableWindowsKey-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c639ee9bb31a5ef0092ec6a2aef8c0235639896a6d6934d8dc9cbadc42f40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608600"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a>IMsRdpClientAdvancedSettings::EnableWindowsKey-Eigenschaft

Gibt an, ob der Windows Schlüssel in der Remotesitzung verwendet werden kann.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
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

 

 





