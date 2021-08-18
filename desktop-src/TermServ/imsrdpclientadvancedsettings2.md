---
title: IMsRdpClientAdvancedSettings2-Schnittstelle
description: Verwaltet erweiterte Clienteinstellungen. Wird von der IMsRdpClientAdvancedSettings-Schnittstelle ableiten.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings2-Remotedesktopdienste
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97584aa3b37adc148672777e95fe0b2c8b101e09989bfa1ab5debbffe489640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001408"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>IMsRdpClientAdvancedSettings2-Schnittstelle

Verwaltet erweiterte Clienteinstellungen. Wird von der [**IMsRdpClientAdvancedSettings-Schnittstelle**](imsrdpclientadvancedsettings-interface.md) ableiten. Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX Steuerelement.

Um eine Instanz dieser Schnittstelle zu erhalten, verwenden Sie die [**IMsTscAx::AdvancedSettings-Eigenschaft,**](imstscax-advancedsettings.md) um einen [**IMsTscAdvancedSettings-Schnittstellenzeiger**](imstscadvancedsettings-interface.md) zu erhalten. Rufen Sie [**anschließend QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **IMsTscAdvancedSettings-Zeiger** auf, und übergeben Sie **\_ IID-IMsRdpClientAdvancedSettings2** an **QueryInterface.**

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings2-Schnittstelle** erbt von [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md). **IMsRdpClientAdvancedSettings2** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings2-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp           | BESCHREIBUNG                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutoReconnect**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob das Clientsteuer steuerelement im Falle einer Trennung der Netzwerkverbindung automatisch wieder eine Verbindung mit der aktuellen Sitzung herstellen kann.<br/>    |
| [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | Lesen/Schreiben<br/> | Gibt an, ob das Clientsteuersystem im Falle einer Trennung der Netzwerkverbindung automatisch wieder eine Verbindung mit einer Sitzung herstellen soll.<br/>            |
| [**MaxReconnectAttempts**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | Lesen/Schreiben<br/> | Gibt an, wie oft versucht werden soll, während der automatischen erneuten Verbindung erneut eine Verbindung herzustellen. Die gültigen Werte dieser Eigenschaft sind 0 bis einschließlich 200.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 ist als 9ac42117-2b76-4320-aa44-0e616ab8437b definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

