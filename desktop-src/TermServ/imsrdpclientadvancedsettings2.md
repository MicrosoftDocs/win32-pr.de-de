---
title: IMsRdpClientAdvancedSettings2-Schnittstelle
description: Verwaltet erweiterte Client Einstellungen. Wird von der imsrdpclientadvancedsettings-Schnittstelle abgeleitet.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340877"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>IMsRdpClientAdvancedSettings2-Schnittstelle

Verwaltet erweiterte Client Einstellungen. Wird von der [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle abgeleitet. Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX-Steuerelement.

Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten. Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings2** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings2** -Schnittstelle erbt von [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md). **IMsRdpClientAdvancedSettings2** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings2** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp           | BESCHREIBUNG                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canautoreconnetct**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob das Client Steuerelement automatisch eine Verbindung mit der aktuellen Sitzung herstellen kann, wenn eine Netzwerkverbindung getrennt wird.<br/>    |
| [**Enableautoreconnetct**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | Lesen/Schreiben<br/> | Gibt an, ob das Client Steuerelement das automatische erneute Herstellen einer Verbindung mit einer Sitzung im Falle einer Netzwerk Trennung aktivieren soll.<br/>            |
| [**Maxreconnectattempts**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | Lesen/Schreiben<br/> | Gibt an, wie oft versucht werden soll, während der automatischen erneuten Verbindung erneut eine Verbindung herzustellen. Gültige Werte für diese Eigenschaft sind 0 bis einschließlich 200.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

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

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

