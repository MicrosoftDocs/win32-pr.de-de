---
title: IMsRdpClientAdvancedSettings ConnectToServerConsole (Eigenschaft)
description: Diese Eigenschaft wird nicht unterstützt. Aufrufe von ConnectToServerConsole geben immer S \_ FALSE zurück.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- ConnectToServerConsole-Remotedesktopdienste
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
- ConnectToServerConsole-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , ConnectToServerConsole-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83c6b935c34dda3f8a676d025bc1995a30e1bbb3f11dd4db3c055f6e28437ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515280"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a>IMsRdpClientAdvancedSettings::ConnectToServerConsole (Eigenschaft)

Diese Eigenschaft wird nicht unterstützt. Aufrufe **von ConnectToServerConsole geben** immer S FALSE **\_ zurück.**

Verwenden Sie [**die ConnectToAd sessionServer-Eigenschaft,**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) um eine Verbindung mit der Sitzung herzustellen, die für administrative Zwecke verwendet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf **VARIANT \_ FALSE fest.** **VARIANT \_ TRUE** wird nicht unterstützt.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
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

 

 





