---
title: IMsRdpClient9-Schnittstelle
description: Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der IMsRdpClient8-Schnittstelle abgeleitet.
ms.assetid: 353f0328-d8a3-4466-bf23-c6d6b8a47e5d
ms.tgt_platform: multiple
keywords:
- IMsRdpClient9-Schnittstelle Remotedesktopdienste
- IMsRdpClient9 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350fd4b9153319f9a1084ffc3fd37784eb6ad3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475951"
---
# <a name="imsrdpclient9-interface"></a>IMsRdpClient9-Schnittstelle

Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der [**IMsRdpClient8**](imsrdpclient8.md) -Schnittstelle abgeleitet.

## <a name="members"></a>Member

Die **IMsRdpClient9** -Schnittstelle erbt von [**IMsRdpClient8**](imsrdpclient8.md). **IMsRdpClient9** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClient9** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"AttachEvent"**](imsrdpclient9-attachevent.md)                                   | Fügt ein Ereignis an.<br/>                                                                                                                                                               |
| [**Verbinden**](imstscax-connect.md)                                                | Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.<br/>                                                                                                        |
| [**"Kreatevirtualchannels"**](imstscax-createvirtualchannels.md)                    | Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.<br/>                                                                                            |
| [**DetachEvent**](imsrdpclient9-detachevent.md)                                   | Trennt ein Ereignis.<br/>                                                                                                                                                               |
| [**Trennen**](imstscax-disconnect.md)                                          | Trennt die aktive Verbindung.<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Ruft die Fehlerbeschreibung für die Sitzungs Trennungs Ereignisse ab.<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Ruft den Status Text für den angegebenen Statuscode ab.<br/>                                                                                                                         |
| [**Getvirtualchanneloptions**](imsrdpclient-getvirtualchanneloptions.md)          | Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.<br/>                                                                                                                                 |
| [**Verbindung wiederherstellen**](imsrdpclient8-reconnect.md)                                       | Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuer Elements an.<br/>                                                                                                              |
| [**Sendonvirtualchannel**](imstscax-sendonvirtualchannel.md)                      | Sendet Daten an den RD-Sitzungshost-Server über einen virtuellen Kanal, der zuvor mithilfe der Methode "| [**atevirtualchannels**](imstscax-createvirtualchannels.md) " erstellt wurde.<br/> |
| [**Sendremoteaction**](imsrdpclient8-sendremoteaction.md)                         | Bewirkt, dass eine Aktion in der Remote Sitzung ausgeführt wird.<br/>                                                                                                                          |
| [**Setvirtualchanneloptions**](imsrdpclient-setvirtualchanneloptions.md)          | Legt die Optionen des virtuellen Kanals für das Remotedesktop ActiveX-Steuerelement fest.<br/>                                                                                                         |
| [**Syncsessiondisplaysettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Synchronisiert Sitzungs Anzeigeeinstellungen.<br/>                                                                                                                                           |
| [**Updatesessiondisplaysettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Aktualisiert die Sitzungs Anzeigeeinstellungen.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient9** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Advancedsettings**](imstscax-advancedsettings.md)<br/>                     | Schreibgeschützt<br/>  | Ruft einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger ab.<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle ab. Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) -Schnittstelle ab. Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle ab.<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf eine [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) -Schnittstelle ab.<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) -Schnittstelle ab.<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) -Schnittstelle ab.<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) -Schnittstelle unterstützt.<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Schreibgeschützt<br/>  | Enthält ein Objekt, das die [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) -Schnittstelle unterstützt.<br/>                                                                                                                      |
| [**Chiffrierung**](imstscax-cipherstrength.md)<br/>                         | Schreibgeschützt<br/>  | Ruft die maximale Verschlüsselungsstärke des aktuellen Steuer Elements ab.<br/>                                                                                                                                                                           |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Die Farbtiefe (in Bits pro Pixel) für die Verbindung des-Steuer Elements.<br/>                                                                                                                                                                           |
| [**Verbunden**](imstscax-connected.md)<br/>                                   | Schreibgeschützt<br/>  | Ruft den Verbindungsstatus des aktuellen Steuer Elements ab.<br/>                                                                                                                                                                                      |
| [**Connectedstatustext**](imsrdpclient2-connectedstatustext.md)<br/>          | Lesen/Schreiben<br/> | Enthält den Text, der im Client Bereich des-Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                                                                                          |
| [**Connectingtext**](imstscax-connectingtext.md)<br/>                         | Lesen/Schreiben<br/> | Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lesen/Schreiben<br/> | Gibt die Höhe des aktuellen Steuer Elements auf dem anfänglichen Remote Desktop in Pixel an.<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lesen/Schreiben<br/> | Gibt die Breite des aktuellen Steuer Elements auf dem ersten Remote Desktop in Pixel an.<br/>                                                                                                                                                            |
| [**Disconnectedtext**](imstscax-disconnectedtext.md)<br/>                     | Lesen/Schreiben<br/> | Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/>                                                                                                                                                  |
| [**Domain**](imstscax-domain.md)<br/>                                         | Lesen/Schreiben<br/> | Gibt die Domäne an, an der der aktuelle Benutzer sich anmeldet.<br/>                                                                                                                                                                                     |
| [**Extendeddisconnecverrat**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Enthält erweiterte Informationen über den Grund für die Trennung der Verbindung.<br/>                                                                                                                                                                 |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Bestimmt, ob sich das Client Steuerelement im Vollbildmodus befindet.<br/>                                                                                                                                                                               |
| [**Fullscrebereberechtigen**](imstscax-fullscreentitle.md)<br/>                       | Lesegeschützt<br/> | Gibt den Fenstertitel an, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                                                                               |
| [**Horizontalscrollbarvisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine horizontale Schiebe Leiste angezeigt hat.<br/>                                                                                                                                                                        |
| [**Msrdpclientshell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Schreibgeschützt<br/>  | Ruft die Skript fähige-Client Einstellungs Schnittstelle [**imsrdpclientshell**](imsrdpclientshell.md)ab.<br/>                                                                                                                                           |
| [**Remoteprogram**](imsrdpclient5-remoteprogram.md)<br/>                      | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**itsremoteprogram**](itsremoteprogram.md) -Schnittstelle unterstützt.<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**ITSRemoteProgram2**](itsremoteprogram2.md) -Schnittstelle unterstützt.<br/>                                                                                                                                             |
| [**Securedsettings**](imstscax-securedsettings.md)<br/>                       | Schreibgeschützt<br/>  | Ruft einen [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstellen Zeiger ab.<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle ab. Diese Schnittstelle kann verwendet werden, um gesicherte Einstellungen für das Client Steuerelement festzulegen.<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) -Schnittstelle unterstützt.<br/>                                                                                                                       |
| [**Securedsettingsenabled**](imstscax-securedsettingsenabled.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob die [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle verfügbar ist. Das heißt, ob sich die Webseite, die das Steuerelement enthält, derzeit in einer der zulässigen Internet Explorer-URL-Sicherheitszonen befindet.<br/> |
| [**Servers**](imstscax-server.md)<br/>                                         | Lesen/Schreiben<br/> | Gibt den Namen des Servers an, mit dem das aktuelle Steuerelement verbunden ist.<br/>                                                                                                                                                                 |
| [**Startconnected**](imstscax-startconnected.md)<br/>                         | Lesen/Schreiben<br/> | Gibt an, ob das Steuerelement beim Start sofort die RD-Sitzungshost Server-Verbindung herstellen soll.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Schreibgeschützt<br/>  | Ruft ab, was durch ein Skript an die [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md) -Schnittstelle übermittelt wurde.<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) -Schnittstelle ab.<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) -Schnittstelle unterstützt.<br/>                                                                                                                   |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) -Schnittstelle unterstützt.<br/>                                                                                                                   |
| [**User**](imstscax-username.md)<br/>                                     | Lesen/Schreiben<br/> | Gibt die Anmelde Informationen für den Benutzernamen an.<br/>                                                                                                                                                                                                   |
| [**Version**](imstscax-version.md)<br/>                                       | Schreibgeschützt<br/>  | Gibt die Versionsnummer des aktuellen Steuer Elements an.<br/>                                                                                                                                                                                        |
| [**Verticalscrollbarvisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine vertikale Bild Lauf Leiste anzeigt.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Die **IMsRdpClient9** -Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                                                                                                                               |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient9 ist als 28904001-04b6-436C-a55b-0af1a0883dc9 definiert.<br/>                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

