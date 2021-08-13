---
title: IMsRdpClientAdvancedSettings GrabFocusOnConnect-Eigenschaft
description: Gibt an, ob das Clientsteuerelement beim Herstellen der Verbindung den Fokus haben soll.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
- GrabFocusOnConnect-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , GrabFocusOnConnect-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e759dd6bbd297dcd13eb9885b228f1a8257c293c099eaba3a6a8f1cf46c2a3f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475470"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a>IMsRdpClientAdvancedSettings::GrabFocusOnConnect-Eigenschaft

Gibt an, ob das Clientsteuerelement beim Herstellen der Verbindung den Fokus haben soll. Das Steuerelement versucht nicht, den Fokus aus einem Fenster zu ziehen, das in einem anderen Prozess ausgeführt wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf **VARIANT \_ FALSE** fest, um das Feature zu deaktivieren, oder **VARIANT \_ TRUE,** um das Feature zu aktivieren. Wenn Sie diese Eigenschaft auf **VARIANT \_ FALSE** festlegen, wird verhindert, dass das Steuerelement beim Herstellen einer Verbindung den Fokus greift.

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

 

 





