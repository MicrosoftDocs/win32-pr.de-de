---
title: MsRdpClient3a-Klasse
description: 'Microsoft RDP-Clientsteuerung (verteilbar): Version 4a.'
ms.assetid: F2E3D49F-B3F9-40EF-9B93-C87F55DB0352
ms.tgt_platform: multiple
keywords:
- MsRdpClient3a-Klasse Remotedesktopdienste
- MsRdpClient3a-Klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient3a
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46699f5cd070c8a302305479f9eade7ba1191ae07e272af7409623f3d01960ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058638"
---
# <a name="msrdpclient3a-class"></a>MsRdpClient3a-Klasse

Microsoft RDP-Clientsteuerung (verteilbar): Version 4a

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)

**MsRdpClient3a verfügt** über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient3a-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](imstscax-connect.md)                                                         | Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das -Steuerelement festgelegt sind.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Erstellt ein clientseitiges virtuelles Kanalobjekt für jeden angegebenen Namen des virtuellen Kanals.<br/>                                                                                                                                                                                              |
| [**Trennen**](imstscax-disconnect.md)                                                   | Trennt die aktive Verbindung.<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Ruft die für einen virtuellen Kanal festgelegten Optionen ab.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Benachrichtigt das Geräteumleitungsmodul des Remotedesktop ActiveX, dass eine Geräteänderung auf dem System aufgetreten ist. Diese Methode übergibt [**WM \_ DEVICECHANGE-Benachrichtigungen**](/windows/desktop/DevIO/wm-devicechange) an das Steuerelement.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Wird aufgerufen, ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Zertifikatfehlerdialogfeld).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Wird aufgerufen, bevor ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Zertifikatfehlerdialogfeld).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Wird aufgerufen, wenn das Clientsteuer steuerelement automatisch erneut eine Verbindung mit einer Remotesitzung hergestellt hat.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Wird aufgerufen, wenn ein Client eine Sitzung automatisch erneut mit einem RD-Sitzungshost verbindet.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Wird aufgerufen, wenn ein Client eine Sitzung automatisch erneut mit einem RD-Sitzungshost verbindet.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Wird aufgerufen, wenn der Client Daten in einem skriptierbaren virtuellen Kanal empfängt.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Wird aufgerufen, wenn der Client die [**IMsRdpClient::RequestClose-Methode**](imsrdpclient-requestclose.md) aufruft.<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Wird aufgerufen, wenn das Clientsteuersystem eine Verbindung mit einem serverseitigen RD-Sitzungshost wird.<br/>                                                                                                                                                                       |
| [**Beim Herstellen einer Verbindung**](imstscaxevents-onconnecting.md)                                         | Wird aufgerufen, wenn das Clientsteuerelemente als Reaktion auf einen Aufruf von [**IMsTscAx::Verbinden.**](imstscax-connect.md)<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Wird aufgerufen, wenn der Benutzer auf der Verbindungsleiste nach unten gezogen wurde.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Wird aufgerufen, wenn die Geräteschaltfläche in der Verbindungsleiste gedrückt wurde.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Wird aufgerufen, wenn die Verbindung zwischen dem Clientsteuer steuerelement und dem RD-Sitzungshost wurde.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Wird aufgerufen, wenn der Client in den Vollbildmodus eintritt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer [](terminal-services-shortcut-keys.md) die Tastenkombination für den Vollbildmodus drückt (STRG+ALT+BREAK).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Wird aufgerufen, wenn das Clientsteuer steuerelement einen schwerwiegenden Fehler trifft.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Wird aufgerufen, wenn die Tastenkombination für den Releasefokus gedrückt wird. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die Tastenkombination STRG+ALT+NACH-LINKS oder STRG+ALT+NACH-RECHTS-TASTE drückt.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Wird aufgerufen, wenn der Benutzer während des von der [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout-Methode**](imsrdpclientadvancedsettings-minutestoidletimeout.md) festgelegten Zeitraums keine Maus- oder Tastatureingaben erhalten hat.<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer [](terminal-services-shortcut-keys.md) die Tastenkombination für den Vollbildmodus drückt (STRG+ALT+BREAK).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Wird aufgerufen, wenn sich das Clientsteuerfeld erfolgreich bei einem RD-Sitzungshost-Server angemeldet hat. Dies wird nach der Anzeige des Dialogfelds Windows Anmeldung angezeigt.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Anmeldeereignis auftritt.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Wird aufgerufen, wenn sich der Mauseingabemodus geändert hat.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Wird während der Verbindungssequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn **die NotifyTSPublicKey-Eigenschaft** **VARIANT TRUE \_ ist.**<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Wird aufgerufen, um anzugeben, dass sich die Größe des Clientsteuer steuerelements auf dem Remotedesktop als Reaktion auf einen Clientsteuerungsvorgang geändert hat.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Clientsteuerprogramm zurückgibt.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Wird aufgerufen, wenn der Benutzer die Schaltfläche **Minimieren** auf der Verbindungsleiste im Vollbildmodus drückt. Das Ausschlagen dieses Ereignisses ist eine Anforderung, die die Containeranwendung selbst minimiert.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Wird aufgerufen, wenn der Client den Wechsel in den Vollbildmodus an fordert, und die [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen-Methode**](imstscadvancedsettings-containerhandledfullscreen.md) aufgerufen wird, um die **ContainerHandledFullScreen-Eigenschaft** auf einen Wert ungleich 0 (null) zu setzen.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Wird aufgerufen, wenn der Client den Vollbildmodus verlassen möchte und die [**Eigenschaft IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) auf einen Wert ungleich 0 (null) festgelegt wurde.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Wird aufgerufen, wenn der Client eine Systemmeldung empfängt.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Wird aufgerufen, wenn der Benutzername vom -Steuerelement übernommen wurde.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Wird aufgerufen, wenn das Clientsteuer steuerelement einen Fehlerzustand trifft, der nicht schwerwiegender ist.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Fordert ein ordnungsgemäßes Herunterfahren des Clientsteuer steuerelements an.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Setzt alle Kennwortzustände im Steuerelement zurück.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Sendet eine Reihe von Tastatureingaben an das Steuerelement. Die Tastatureingaben sind in Scancodeform, d.&a0;b. den Tastaturdaten der tatsächlichen physischen Tasten.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Sendet Daten an den RD-Sitzungshost-Server über einen virtuellen Kanal, der zuvor mithilfe der [**IMsTscAx::CreateVirtualChannels-Methode erstellt**](imstscax-createvirtualchannels.md) wurde.<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Legt die Optionen für den virtuellen Kanal für das Clientsteuer steuerelement fest.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Die **MsRdpClient3a-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | Beschreibung                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Schreibgeschützt<br/>  | Ein [**IMsTscAdvancedSettings-Schnittstellenzeiger.**](imstscadvancedsettings-interface.md)<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings-Schnittstelle,**](imsrdpclientadvancedsettings-interface.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerfeld verwendet wird.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings2-Schnittstelle,**](imsrdpclientadvancedsettings2.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerfeld verwendet wird.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings3-Schnittstelle,**](imsrdpclientadvancedsettings3.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerfeld verwendet wird.<br/>         |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>              | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                      | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Schreibgeschützt<br/>  | Die maximale Verschlüsselungsstärke des aktuellen Steuerelements.<br/>                                                                                                        |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | Lesegeschützt<br/> | Das Remotedesktop ActiveX-Steuerelementkennwort im Klartextformat.<br/>                                                                                              |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Farbtiefe des aktuellen Steuerelements.<br/>                                                                                                                            |
| [**Verbunden**](imstscax-connected.md)<br/>                                   | Schreibgeschützt<br/>  | Der Verbindungsstatus des aktuellen Steuerelements.<br/>                                                                                                                   |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lesen/Schreiben<br/> | Text, der im Clientbereich des Steuerelements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Lesen/Schreiben<br/> | Der Text, der zentriert im -Steuerelement angezeigt wird, während das Steuerelement eine Verbindung verbindet.<br/>                                                                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lesen/Schreiben<br/> | Die Höhe des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel.<br/>                                                                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lesen/Schreiben<br/> | Die Breite des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel.<br/>                                                                                         |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lesen/Schreiben<br/> | Der Text, der im -Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/>                                                                               |
| [**Domain**](imstscax-domain.md)<br/>                                         | Lesen/Schreiben<br/> | Die Domäne, bei der sich der aktuelle Benutzer anmeldet.<br/>                                                                                                                  |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Erweiterte Informationen zum Grund für die Trennung der Verbindung des Clientsteuer steuerelements.<br/>                                                                                      |
| [**Fullscreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                          |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Lesegeschützt<br/> | Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                            |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine horizontale Bildlaufleiste angezeigt hat.<br/>                                                                                           |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>          | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                  | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Schreibgeschützt<br/>  | Ein [**IMsTscSecuredSettings-Schnittstellenzeiger.**](imstscsecuredsettings-interface.md)<br/>                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientSecuredSettings-Schnittstelle,**](imsrdpclientsecuredsettings-interface.md) die zum Festlegen geschützter Einstellungen für das Clientsteuerfeld verwendet wird.<br/>    |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob [**die IMsTscSecuredSettings-Schnittstelle**](imstscsecuredsettings-interface.md) verfügbar ist.<br/>                                                 |
| [**Server**](imstscax-server.md)<br/>                                         | Lesen/Schreiben<br/> | Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br/>                                                                                              |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lesen/Schreiben<br/> | Gibt an, ob das Steuerelement die Serververbindung RD-Sitzungshost beim Start eingibt.<br/>                                                   |
| [**Nutzername**](imstscax-username.md)<br/>                                     | Lesen/Schreiben<br/> | Die Anmeldeinformationen für den Benutzernamen.<br/>                                                                                                                                |
| [**Version**](imstscax-version.md)<br/>                                       | Schreibgeschützt<br/>  | Die Versionsnummer des aktuellen Steuerelements.<br/>                                                                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine vertikale Bildlaufleiste anzeigt.<br/>                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient3a ist als 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4 definiert.<br/>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotedesktop ActiveX Steuerelementklassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

