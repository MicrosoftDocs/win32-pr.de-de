---
title: IMsRdpClientAdvancedSettings6-Schnittstelle
description: Macht Eigenschaften verfügbar, die erweiterte ActiveX-Steuerelementeinstellungen verwalten.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste beschrieben
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
ms.openlocfilehash: cf4c108345e3dae0b5c8f4e45c3a1c07299cccdaed44404718e599c0ef973957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352127"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>IMsRdpClientAdvancedSettings6-Schnittstelle

Macht Eigenschaften verfügbar, die erweiterte ActiveX-Steuerelementeinstellungen verwalten. Die **IMsRdpClientAdvancedSettings6-Schnittstelle** wird von der [**IMsRdpClientAdvancedSettings5-Schnittstelle**](imsrdpclientadvancedsettings5.md) abgeleitet.

Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**IMsTscAx::AdvancedSettings-Eigenschaft,**](imstscax-advancedsettings.md) um einen [**IMsTscAdvancedSettings-Schnittstellenzeiger**](imstscadvancedsettings-interface.md) abzurufen. Rufen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **IMsTscAdvancedSettings-Zeiger** auf, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings6** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings6-Schnittstelle** erbt von [**IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md) **IMsRdpClientAdvancedSettings6** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings6-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                  | Zugriffstyp           | Beschreibung                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Lesen/Schreiben<br/> | Gibt den Dienstprinzipalnamen (Service Principal Name, SPN) an, der für die Authentifizierung beim Server verwendet werden soll.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Schreibgeschützt<br/>  | Gibt den Authentifizierungstyp an, der für diese Verbindung verwendet wird.<br/>                                                          |
| [**ConnectToAdogrammServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Lesen/Schreiben<br/> | Ruft ab oder gibt an, ob das ActiveX-Steuerelement zu Administrativen Zwecken versuchen soll, eine Verbindung mit dem Server herzustellen.<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Lesen/Schreiben<br/> | Gibt an, ob der Credential Security Service Provider (CredSSP) für diese Verbindung aktiviert ist.<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Lesen/Schreiben<br/> | Gibt den virtuellen Schlüsselcode an, der STRG+ALT hinzugefügt werden soll, um den Hotkey-Ersatz für STRG+ALT+NACH-LINKS-TASTE zu bestimmen.<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Lesen/Schreiben<br/> | Gibt den Virtuellen Schlüsselcode an, der STRG+ALT hinzugefügt werden soll, um den Hotkey-Ersatz für STRG+ALT+NACH-RECHTS-TASTE zu bestimmen.<br/>         |
| [**Pcb**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Lesen/Schreiben<br/> | Gibt die EINSTELLUNG FÜR DIE VORABVERBINDUNG (PREconnection BLOB) an, die vor dem Herstellen einer Verbindung für die Übertragung an den Server verwendet werden soll.<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob die Maus den relativen Modus verwenden soll.<br/>                                                                   |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde durch die [**IMsRdpClientAdvancedSettings7-Schnittstelle**](imsrdpclientadvancedsettings7.md) erweitert und erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen.

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

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

