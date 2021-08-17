---
title: IMsRdpClientAdvancedSettings3-Schnittstelle
description: Verwaltet erweiterte Clienteinstellungen. Wird von der IMsRdpClientAdvancedSettings2-Schnittstelle ableiten.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings3-Remotedesktopdienste
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df13ccfb0d955714984af82daaf693522ee7d61af9c608107c53dc9f5464b591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001378"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a>IMsRdpClientAdvancedSettings3-Schnittstelle

Verwaltet erweiterte Clienteinstellungen. Wird von der [**IMsRdpClientAdvancedSettings2-Schnittstelle**](imsrdpclientadvancedsettings2.md) ableiten. Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX Steuerelement.

Um eine Instanz dieser Schnittstelle zu erhalten, verwenden Sie die [**IMsTscAx::AdvancedSettings-Eigenschaft,**](imstscax-advancedsettings.md) um einen [**IMsTscAdvancedSettings-Schnittstellenzeiger**](imstscadvancedsettings-interface.md) zu erhalten. Rufen Sie [**dann QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **IMsTscAdvancedSettings-Zeiger** auf, und übergeben Sie **\_ IID-IMsRdpClientAdvancedSettings3** an **QueryInterface.**

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings3-Schnittstelle** erbt von [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md). **IMsRdpClientAdvancedSettings3** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings3-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                            | Zugriffstyp           | Beschreibung                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [**ConnectionBarShowMinimizeButton**](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob die Schaltfläche **Minimieren auf** der Verbindungsleiste angezeigt werden soll.<br/> |
| [**ConnectionBarShowRestoreButton**](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | Lesen/Schreiben<br/> | Gibt an, ob die Schaltfläche **Wiederherstellen** auf der Verbindungsleiste angezeigt werden soll.<br/>  |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 ist als 19cd856b-c542-4c53-acee-f127e3be1a59 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

