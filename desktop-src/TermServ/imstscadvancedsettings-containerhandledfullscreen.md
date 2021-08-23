---
title: IMsTscAdvancedSettings ContainerHandledFullScreen (Eigenschaft)
description: Gibt an, ob der containerverhandete Vollbildmodus aktiviert ist.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- ContainerHandledFullScreen-Remotedesktopdienste
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsTscAdvancedSettings-Schnittstelle
- IMsTscAdvancedSettings-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
- ContainerHandledFullScreen-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , ContainerHandledFullScreen-Eigenschaft
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
ms.openlocfilehash: 975581aaca4aad2511396e8ec426a7bf2a4720ff54202d42fbe932c0c2e9464d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513120"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>IMsTscAdvancedSettings::ContainerHandledFullScreen (Eigenschaft)

Gibt an, ob der containerverhandete Vollbildmodus aktiviert ist.

> [!Note]  
> Der Wert der **ContainerHandledFullScreen-Eigenschaft** hat keine Auswirkungen, wenn das Remotedesktop ActiveX-Steuerelement für Skripts sicher ist, und gibt **S \_ FALSE** zurück, wenn versucht wird, den Wert zu ändern.

 

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

Legen Sie diesen Parameter auf **TRUE** fest, um den Modus oder einen anderen Wert zum Deaktivieren des Modus zu aktivieren.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich. Gibt **S \_ FALSE zurück,** wenn dies nicht unterstützt wird.

## <a name="remarks"></a>Hinweise

Wenn dieser Modus aktiviert ist, verarbeitet der aktuelle Container den Wechsel in den und aus dem Vollbildmodus. Diese Methode sollte nur verwendet werden, wenn der aktuelle Container umfassende Kontrolle über das Verhalten des Vollbildmodus benötigt. Wenn diese Eigenschaft festgelegt ist, wird das Steuerelement als Reaktion auf die Tastenkombination für den Vollbildmodus (STRG+ALT+BREAK) nicht in den Vollbildmodus wechseln oder den Vollbildmodus verlassen. Stattdessen werden die [**Ereignisse IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) und [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) aufgerufen. Weitere Informationen zu diesen Ereignissen finden Sie unter [**IMsTscAxEvents.**](imstscaxevents-interface.md)

Die meisten Containeranwendungen müssen nicht den containerbasierten Vollbildmodus verwenden.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings ist als 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





