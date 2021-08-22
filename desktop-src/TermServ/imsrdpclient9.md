---
title: IMsRdpClient9-Schnittstelle
description: Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der IMsRdpClient8-Schnittstelle ableiten.
ms.assetid: 353f0328-d8a3-4466-bf23-c6d6b8a47e5d
ms.tgt_platform: multiple
keywords:
- IMsRdpClient9-Remotedesktopdienste
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: 5a84530c401398f373d9ae7e2f02619f9b3abeaa9f1d51a9f550afe55a7347e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609281"
---
# <a name="imsrdpclient9-interface"></a>IMsRdpClient9-Schnittstelle

Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der [**IMsRdpClient8-Schnittstelle**](imsrdpclient8.md) ableiten.

## <a name="members"></a>Member

Die **IMsRdpClient9-Schnittstelle** erbt von [**IMsRdpClient8**](imsrdpclient8.md). **IMsRdpClient9** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClient9-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attachevent**](imsrdpclient9-attachevent.md)                                   | Angefügt ein Ereignis.<br/>                                                                                                                                                               |
| [**Verbinden**](imstscax-connect.md)                                                | Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das -Steuerelement festgelegt sind.<br/>                                                                                                        |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                    | Erstellt ein clientseitiges virtuelles Kanalobjekt für jeden angegebenen Namen des virtuellen Kanals.<br/>                                                                                            |
| [**Detachevent**](imsrdpclient9-detachevent.md)                                   | Trennt ein Ereignis.<br/>                                                                                                                                                               |
| [**Trennen**](imstscax-disconnect.md)                                          | Trennt die aktive Verbindung.<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Ruft die Fehlerbeschreibung für die Sitzungstrennungsereignisse ab.<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Ruft den Statustext für den angegebenen Statuscode ab.<br/>                                                                                                                         |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Ruft die für einen virtuellen Kanal festgelegten Optionen ab.<br/>                                                                                                                                 |
| [**Verbindung wiederherstellen**](imsrdpclient8-reconnect.md)                                       | Verbindet sich mit der neuen Desktopbreite und -höhe erneut mit der Remotesitzung.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX an.<br/>                                                                                                              |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                      | Sendet Daten an den RD-Sitzungshost über einen virtuellen Kanal, der zuvor mithilfe der [**CreateVirtualChannels-Methode erstellt**](imstscax-createvirtualchannels.md) wurde.<br/> |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Bewirkt, dass eine Aktion in der Remotesitzung ausgeführt wird.<br/>                                                                                                                          |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Legt die Optionen für den virtuellen Kanal für das Remotedesktop ActiveX fest.<br/>                                                                                                         |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Synchronisiert Einstellungen für die Sitzungsanzeige.<br/>                                                                                                                                           |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Aktualisiert einstellungen für die Sitzungsanzeige.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient9-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | Beschreibung                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Schreibgeschützt<br/>  | Ruft einen [**IMsTscAdvancedSettings-Schnittstellenzeiger**](imstscadvancedsettings-interface.md) ab.<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings-Schnittstelle**](imsrdpclientadvancedsettings-interface.md) ab. Die -Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Clientsteuersystem zu festlegen.<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings2-Schnittstelle**](imsrdpclientadvancedsettings2.md) ab. Die -Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Clientsteuersystem zu festlegen.<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings3-Schnittstelle**](imsrdpclientadvancedsettings3.md) ab.<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf eine [**IMsRdpClientAdvancedSettings4-Schnittstelle**](imsrdpclientadvancedsettings4.md) ab.<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings5-Schnittstelle**](imsrdpclientadvancedsettings5.md) ab.<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings6-Schnittstelle**](imsrdpclientadvancedsettings5.md) ab.<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientAdvancedSettings7-Schnittstelle**](imsrdpclientadvancedsettings7.md) unterstützt.<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Schreibgeschützt<br/>  | Enthält ein -Objekt, das die [**IMsRdpClientAdvancedSettings8-Schnittstelle**](imsrdpclientadvancedsettings8.md) unterstützt.<br/>                                                                                                                      |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Schreibgeschützt<br/>  | Ruft die maximale Verschlüsselungsstärke des aktuellen Steuerelements ab.<br/>                                                                                                                                                                           |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Die Farbtiefe (in Bits pro Pixel) für die Verbindung des Steuerelements.<br/>                                                                                                                                                                           |
| [**Verbunden**](imstscax-connected.md)<br/>                                   | Schreibgeschützt<br/>  | Ruft den Verbindungsstatus des aktuellen Steuerelements ab.<br/>                                                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lesen/Schreiben<br/> | Enthält den Text, der im Clientbereich des Steuerelements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                                                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Lesen/Schreiben<br/> | Gibt den Text an, der zentriert im -Steuerelement angezeigt wird, während das Steuerelement eine Verbindung verbindet.<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lesen/Schreiben<br/> | Gibt die Höhe des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel an.<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lesen/Schreiben<br/> | Gibt die Breite des aktuellen Steuerelements auf dem ersten Remotedesktop in Pixel an.<br/>                                                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lesen/Schreiben<br/> | Gibt den Text an, der im Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/>                                                                                                                                                  |
| [**Domain**](imstscax-domain.md)<br/>                                         | Lesen/Schreiben<br/> | Gibt die Domäne an, bei der sich der aktuelle Benutzer anmeldet.<br/>                                                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Enthält erweiterte Informationen zum Grund der Trennung des Steuerelements.<br/>                                                                                                                                                                 |
| [**Fullscreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Bestimmt, ob sich das Clientsteuerelement im Vollbildmodus befindet.<br/>                                                                                                                                                                               |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Lesegeschützt<br/> | Gibt den Fenstertitel an, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine horizontale Bildlaufleiste angezeigt hat.<br/>                                                                                                                                                                        |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Schreibgeschützt<br/>  | Ruft die Skripterstellungsclienteinstellungsschnittstelle [**IMsRdpClientShell**](imsrdpclientshell.md)ab.<br/>                                                                                                                                           |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**ITSRemoteProgram-Schnittstelle**](itsremoteprogram.md) unterstützt.<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**ITSRemoteProgram2-Schnittstelle**](itsremoteprogram2.md) unterstützt.<br/>                                                                                                                                             |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Schreibgeschützt<br/>  | Ruft einen [**IMsTscSecuredSettings-Schnittstellenzeiger**](imstscsecuredsettings-interface.md) ab.<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientSecuredSettings-Schnittstelle**](imsrdpclientsecuredsettings-interface.md) ab. Diese Schnittstelle kann verwendet werden, um sichere Einstellungen für das Clientsteuerelement festzulegen.<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientSecuredSettings2-Schnittstelle**](imsrdpclientsecuredsettings2.md) unterstützt.<br/>                                                                                                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob die [**IMsTscSecuredSettings-Schnittstelle**](imstscsecuredsettings-interface.md) verfügbar ist. Das heißt, ob sich die Webseite, die das Steuerelement enthält, derzeit in einer der zulässigen Internet Explorer URL-Sicherheitszonen befindet.<br/> |
| [**Server**](imstscax-server.md)<br/>                                         | Lesen/Schreiben<br/> | Gibt den Namen des Servers an, mit dem das aktuelle Steuerelement verbunden ist.<br/>                                                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lesen/Schreiben<br/> | Gibt an, ob das Steuerelement die RD-Sitzungshost Serververbindung sofort beim Start herstellt.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Schreibgeschützt<br/>  | Ruft ab, was über ein Skript an die [**IMsRdpClientTransportSettings-Schnittstelle**](imsrdpclienttransportsettings.md) übergeben wurde.<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientTransportSettings2-Schnittstelle**](imsrdpclienttransportsettings2.md) ab.<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3-Schnittstelle**](imsrdpclienttransportsettings3.md) unterstützt.<br/>                                                                                                                   |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings4-Schnittstelle**](imsrdpclienttransportsettings4.md) unterstützt.<br/>                                                                                                                   |
| [**Nutzername**](imstscax-username.md)<br/>                                     | Lesen/Schreiben<br/> | Gibt die Anmeldeinformationen für den Benutzernamen an.<br/>                                                                                                                                                                                                   |
| [**Version**](imstscax-version.md)<br/>                                       | Schreibgeschützt<br/>  | Gibt die Versionsnummer des aktuellen Steuerelements an.<br/>                                                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine vertikale Bildlaufleiste anzeigt.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Die **IMsRdpClient9-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                                                                                                                               |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient9 ist als 28904001-04B6-436C-A55B-0AF1A0883DC9 definiert.<br/>                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Weitere Informationen

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

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

