---
title: IMsRdpClientAdvancedSettings DisableCtrlAltDel (Eigenschaft)
description: Gibt an, ob der erste erläuternde Bildschirm in Winlogon angezeigt werden soll.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- DisableCtrlAltDel-Remotedesktopdienste
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
- DisableCtrlAltDel-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , DisableCtrlAltDel-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c524945afe4fbaaa0498f579641a32d3f55f37e88335be82e8fa308fae502f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871052"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a>IMsRdpClientAdvancedSettings::D isableCtrlAltDel-Eigenschaft

Gibt an, ob der erste erläuternde Bildschirm in Winlogon angezeigt werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf 0 fest, um das Feature oder einen Wert ungleich 0 (null) zu deaktivieren, um das Feature zu aktivieren.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

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

 

 





