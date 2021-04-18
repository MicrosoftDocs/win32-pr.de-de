---
title: IMsRdpClientAdvancedSettings6-Schnittstelle
description: Macht Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340347"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>IMsRdpClientAdvancedSettings6-Schnittstelle

Macht Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten. Die **IMsRdpClientAdvancedSettings6** -Schnittstelle wird von der [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) -Schnittstelle abgeleitet.

Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten. Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings6** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings6** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md). **IMsRdpClientAdvancedSettings6** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings6** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Authenticationserviceclass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Lesen/Schreiben<br/> | Gibt den Dienst Prinzipal Namen (SPN) an, der für die Authentifizierung beim Server verwendet werden soll.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Schreibgeschützt<br/>  | Gibt den für diese Verbindung verwendeten Authentifizierungstyp an.<br/>                                                          |
| [**Connectum Administration Server**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Lesen/Schreiben<br/> | Ruft ab oder legt fest, ob das ActiveX-Steuerelement versuchen soll, eine Verbindung mit dem Server zu Verwaltungszwecken herzustellen.<br/> |
| [**Enablekredsspsupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Lesen/Schreiben<br/> | Gibt an, ob der Credential Security Service Provider (kredssp) für diese Verbindung aktiviert ist.<br/>                    |
| [**Hotkeyfocareleaseleft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Lesen/Schreiben<br/> | Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-Links zu bestimmen.<br/>          |
| [**Hotkeyfocareleaseright**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Lesen/Schreiben<br/> | Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-rechts zu bestimmen.<br/>         |
| [**PCB**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Lesen/Schreiben<br/> | Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll.<br/>               |
| [**Relativemousmode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob die Maus den relativen Modus verwenden soll.<br/>                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wurde von der [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) -Schnittstelle erweitert und erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

