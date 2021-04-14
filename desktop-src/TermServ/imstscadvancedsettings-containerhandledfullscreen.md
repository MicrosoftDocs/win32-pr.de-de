---
title: Imstscadvancedsettings containerhandledfullscreen-Eigenschaft
description: Gibt an, ob der vom Container behandelte Vollbildmodus aktiviert ist.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392027"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>Imstscadvancedsettings:: containerhandledfullscreen-Eigenschaft

Gibt an, ob der vom Container behandelte Vollbildmodus aktiviert ist.

> [!Note]  
> Der Wert der **containerhandledfullscreen** -Eigenschaft hat keine Auswirkung, wenn das Remotedesktop ActiveX-Steuerelement für die Skripterstellung sicher ist, und gibt **\_ false** zurück, wenn versucht wird, den Wert zu ändern.

 

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf " **true** " fest, um den Modus oder einen anderen Wert zum Deaktivieren des Modus zu aktivieren.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück. Gibt **\_ false** zurück, wenn dies nicht unterstützt wird.

## <a name="remarks"></a>Bemerkungen

Wenn dieser Modus aktiviert ist, verarbeitet der aktuelle Container den Wechsel in den und aus dem Vollbildmodus. Diese Methode sollte nur verwendet werden, wenn der aktuelle Container eine umfassende Kontrolle über das Verhalten im Vollbildmodus benötigt. Wenn diese Eigenschaft festgelegt ist, wird das Steuerelement nicht in der Antwort auf die Tastenkombination für den Vollbildmodus (Strg + Alt + untlos) angezeigt oder verlässt den Vollbildmodus. Stattdessen werden die Ereignisse [**imstscaxevents:: onrequestgofullscreen**](imstscaxevents-onrequestgofullscreen.md) und [**imstscaxevents:: onrequestleavefullscreen**](imstscaxevents-onrequestleavefullscreen.md) aufgerufen. Weitere Informationen zu diesen Ereignissen finden Sie unter [**imstscaxevents**](imstscaxevents-interface.md) .

Die meisten Container Anwendungen müssen den im Container behandelten Vollbildmodus nicht verwenden.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





