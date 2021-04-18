---
title: IMsRdpClientAdvancedSettings4-Schnittstelle
description: Verwaltet erweiterte Client Einstellungen. Wird von der IMsRdpClientAdvancedSettings3-Schnittstelle abgeleitet.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391877"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a>IMsRdpClientAdvancedSettings4-Schnittstelle

Verwaltet erweiterte Client Einstellungen. Wird von der [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle abgeleitet. Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX-Steuerelement.

Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten. Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings4** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings4** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md). **IMsRdpClientAdvancedSettings4** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings4** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                    | Zugriffstyp           | BESCHREIBUNG                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [**AuthenticationLevel**](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | Lesen/Schreiben<br/> | Gibt die Authentifizierungs Ebene an, die für die Verbindung verwendet werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                                     |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings4 ist als FBA7F64E-7345-4405-AE50-FA4A763DC0DE definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

