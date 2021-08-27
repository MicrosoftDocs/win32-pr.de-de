---
title: MsRdpClient5-Klasse
description: 'Microsoft RDP-Clientsteuerung (verteilbar): Version 6.'
ms.assetid: 30DC49A8-A9B1-4F74-B578-5761FA0C1315
ms.tgt_platform: multiple
keywords:
- MsRdpClient5-Remotedesktopdienste
- MsRdpClient5-Klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca53765f137e524f1605cdc0bbcabadbc12e89da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473376"
---
# <a name="msrdpclient5-class"></a>MsRdpClient5-Klasse

Microsoft RDP-Clientsteuerung (verteilbar): Version 6

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)

**MsRdpClient5** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient5-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](imstscax-connect.md)                                                         | Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das -Steuerelement festgelegt sind.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Erstellt ein clientseitiges virtuelles Kanalobjekt für jeden angegebenen Namen des virtuellen Kanals.<br/>                                                                                                                                                                                              |
| [**Trennen**](imstscax-disconnect.md)                                                   | Trennt die aktive Verbindung.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Ruft die Fehlercodes und Fehlermeldungen ab.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Ruft die für einen virtuellen Kanal festgelegten Optionen ab.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Benachrichtigt das Geräteumleitungsmodul des Remotedesktop ActiveX, dass eine Geräteänderung auf dem System aufgetreten ist. Diese Methode übergibt [**WM \_ DEVICECHANGE-Benachrichtigungen**](/windows/desktop/DevIO/wm-devicechange) an das Steuerelement.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Wird aufgerufen, ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Zertifikatfehlerdialogfeld).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Wird aufgerufen, ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Zertifikatfehlerdialogfeld).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Wird aufgerufen, wenn das Clientsteuer steuerelement automatisch erneut eine Verbindung mit einer Remotesitzung hergestellt hat.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Wird aufgerufen, wenn ein Client eine Sitzung automatisch erneut mit einem RD-Sitzungshost verbindet.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Wird aufgerufen, wenn ein Client eine Sitzung automatisch erneut mit einem RD-Sitzungshost verbindet.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Wird aufgerufen, wenn der Client Daten in einem skriptierbaren virtuellen Kanal empfängt.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Wird aufgerufen, wenn der Client die [**IMsRdpClient::RequestClose-Methode**](imsrdpclient-requestclose.md) aufruft.<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Wird aufgerufen, wenn das Clientsteuer steuerelement eine Verbindung mit einem serverseitigen RD-Sitzungshost wird.<br/>                                                                                                                                                                       |
| [**Beim Herstellen einer Verbindung**](imstscaxevents-onconnecting.md)                                         | Wird aufgerufen, wenn das Clientsteuerelemente als Reaktion auf einen Aufruf von [**IMsTscAx::Verbinden.**](imstscax-connect.md)<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Wird aufgerufen, wenn der Benutzer auf der Verbindungsleiste nach unten gezogen wurde.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Wird aufgerufen, wenn die Geräteschaltfläche in der Verbindungsleiste gedrückt wurde.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Wird aufgerufen, wenn die Verbindung zwischen dem Clientsteuer steuerelement und dem serverseitigen RD-Sitzungshost wurde.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Wird aufgerufen, wenn der Client in den Vollbildmodus eintritt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer [](terminal-services-shortcut-keys.md) die Tastenkombination für den Vollbildmodus drückt (STRG+ALT+BREAK).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Wird aufgerufen, wenn das Clientsteuer steuerelement einen schwerwiegenden Fehler trifft.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Wird aufgerufen, wenn die Tastenkombination für den Releasefokus gedrückt wird. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die Tastenkombination STRG+ALT+NACH-LINKS oder STRG+ALT+NACH-RECHTS-TASTE drückt.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Wird aufgerufen, wenn der Benutzer während des von der [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout-Methode**](imsrdpclientadvancedsettings-minutestoidletimeout.md) festgelegten Zeitraums keine Maus- oder Tastatureingaben erhalten hat.<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer [](terminal-services-shortcut-keys.md) die Tastenkombination für den Vollbildmodus drückt (STRG+ALT+BREAK).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Wird aufgerufen, wenn sich das Clientsteuerfeld erfolgreich bei einem RD-Sitzungshost-Server angemeldet hat. Folgen Sie dazu der Anzeige Windows Anmeldedialogfelds.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Anmeldeereignis auftritt.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Wird aufgerufen, wenn sich der Mauseingabemodus geändert hat.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Wird während der Verbindungssequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn **die NotifyTSPublicKey-Eigenschaft** **VARIANT TRUE \_ ist.**<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Wird aufgerufen, um anzugeben, dass sich die Größe des Clientsteuer steuerelements auf dem Remotedesktop als Reaktion auf einen Clientsteuerungsvorgang geändert hat.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Clientsteuerprogramm zurückgibt.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Wird aufgerufen, wenn der Benutzer die Schaltfläche **Minimieren** auf der Verbindungsleiste im Vollbildmodus drückt. Das Ausschlagen dieses Ereignisses ist eine Anforderung, die die Containeranwendung selbst minimiert.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Wird aufgerufen, wenn der Client den Wechsel in den Vollbildmodus an fordert, und die [**Methode IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) aufgerufen wird, um die **ContainerHandledFullScreen-Eigenschaft** auf einen Wert ungleich 0 (null) zu setzen.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Wird aufgerufen, wenn der Client anfordert, den Vollbildmodus zu verlassen, und die [**Eigenschaft IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) auf einen Wert ungleich 0 (null) festgelegt wurde.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Wird aufgerufen, wenn der Client eine Systemmeldung empfängt.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Wird aufgerufen, wenn der Benutzername vom Steuerelement abgerufen wurde.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Wird aufgerufen, wenn das Clientsteuerelement eine Fehlerbedingung erkennt, die nicht schwerwiegend ist.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Fordert ein ordnungsgemäßes Herunterfahren des Clientsteuerelements an.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Setzt alle Kennwortzustände im Steuerelement zurück.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Sendet eine Reihe von Tastatureingaben an das Steuerelement. Die Tastatureingaben befinden sich in Scancodeform, d. h. den Tastaturdaten der tatsächlichen physischen Tasten.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Sendet Daten über einen virtuellen Kanal, der zuvor mit der [**IMsTscAx::CreateVirtualChannels-Methode**](imstscax-createvirtualchannels.md) erstellt wurde, an den RD-Sitzungshost Server.<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Legt die Optionen für den virtuellen Kanal für das Clientsteuerelement fest.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Die **MsRdpClient5-Klasse** verfügt über diese Eigenschaften.




| Eigenschaft | Zugriffstyp | BESCHREIBUNG | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br /> | Schreibgeschützt<br /> | Ein <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings-Schnittstellenzeiger.</strong></a><br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br /> | Schreibgeschützt<br /> | Ein <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4-Schnittstellenzeiger.</strong></a><br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br /> | Schreibgeschützt<br /> | Die Schnittstelle zu <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5.</strong></a><br /> | 
| <a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br /> | Lesen/Schreiben<br /> | Diese Eigenschaft wird nicht unterstützt.<br /> | 
| <a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br /> | Lesen/Schreiben<br /> | Diese Eigenschaft wird nicht unterstützt.<br /> | 
| <a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br /> | Schreibgeschützt<br /> | Die maximale Verschlüsselungsstärke des aktuellen Steuerelements.<br /> | 
| <a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br /> | Lesegeschützt<br /> | Das Remotedesktop ActiveX Steuerelementkennwort im Klartextformat.<br /> | 
| <a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a><br /> | Lesen/Schreiben<br /> | Farbtiefe des aktuellen Steuerelements.<br /> | 
| <a href="imstscax-connected.md"><strong>Verbunden</strong></a><br /> | Schreibgeschützt<br /> | Der Verbindungsstatus des aktuellen Steuerelements.<br /> | 
| <a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br /> | Lesen/Schreiben<br /> | Text, der im Clientbereich des Steuerelements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br /> | 
| <a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br /> | Lesen/Schreiben<br /> | Der Text, der im Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.<br /> | 
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | Lesen/Schreiben<br /> | Die Textzeichenfolge, die für die Verbindungsleiste angezeigt werden soll.<br /> | 
| <a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br /> | Lesen/Schreiben<br /> | Die Höhe des aktuellen Steuerelements auf dem ersten Remotedesktop in Pixel.<br /> | 
| <a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br /> | Lesen/Schreiben<br /> | Die Breite des aktuellen Steuerelements auf dem ersten Remotedesktop in Pixel.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | Schreibgeschützt<br /> | Die Sammlung von PnP-Geräten, die für die Umleitung verfügbar sind.<br /> | 
| <a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br /> | Lesen/Schreiben<br /> | Der Text, der im Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br /> | 
| <a href="imstscax-domain.md"><strong>Domain</strong></a><br /> | Lesen/Schreiben<br /> | Die Domäne, bei der sich der aktuelle Benutzer anmeldet.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | Schreibgeschützt<br /> | Die Auflistung der Laufwerke, die für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob CredSSP für diese Verbindung aktiviert ist.<br /> | 
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | Schreibgeschützt<br /> | Erweiterte Informationen zum Grund der Trennung des Clientsteuerelements.<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>Fullscreen</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | Lesegeschützt<br /> | Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | Schreibgeschützt<br /> | Gibt an, ob das Steuerelement eine horizontale Bildlaufleiste angezeigt hat.<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | Schreibgeschützt<br /> | Die Clienteinstellungen für das Webportalstarter.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die NegotiateSecurityLayer-Einstellung für diese Verbindung unterstützt wird.<br /><blockquote>[!Note]<br />Wenn <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> auf dem Client aktiviert und vorhanden ist oder Secure Sockets Layer (SSL) mit Benutzerauthentifizierung aktiviert ist, wird NegotiateSecurityLayer ignoriert.</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | Lesen/Schreiben<br /> | Diese Eigenschaft wird nicht unterstützt.<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | Lesen/Schreiben<br /> | Diese Eigenschaft wird nicht unterstützt.<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die Aufforderung zum Eingeben von Anmeldeinformationen angezeigt werden soll.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob dynamisch angefügte PnP-Geräte, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob dynamisch angefügte PnP-Laufwerke, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | Schreibgeschützt<br /> | Die RemoteApp-Clienteinstellung.<br /> | 
| <a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br /> | Schreibgeschützt<br /> | Ein <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings-Schnittstellenzeiger.</strong></a><br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings-Schnittstelle,</strong></a> die zum Festlegen geschützter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | Schreibgeschützt<br /> | Gibt an, ob die <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings-Schnittstelle</strong></a> verfügbar ist.<br /> | 
| <a href="imstscax-server.md"><strong>Server</strong></a><br /> | Lesen/Schreiben<br /> | Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Umleitungssicherheitswarnung" vor dem Starten einer Sitzung angezeigt werden soll.<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Steuerelement die RD-Sitzungshost Serververbindung sofort beim Start herstellt.<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | Schreibgeschützt<br /> | Die Rd-Gatewayeinstellung des Clients.<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | Lesen/Schreiben<br /> | Das Fensterhandle, das das übergeordnete Fenster für das Steuerelement sein soll. Dadurch können alle vom Steuerelement angezeigten Fenster in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br /> | 
| <a href="imstscax-username.md"><strong>Nutzername</strong></a><br /> | Lesen/Schreiben<br /> | Die Anmeldeinformationen für den Benutzernamen.<br /> | 
| <a href="imstscax-version.md"><strong>Version</strong></a><br /> | Schreibgeschützt<br /> | Die Versionsnummer des aktuellen Steuerelements.<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | Schreibgeschützt<br /> | Gibt an, ob das Steuerelement eine vertikale Bildlaufleiste anzeigt.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Sicherheitswarnungsdialogfeld eine Warnung zur Umleitung der Zwischenablage enthalten soll, bevor eine Sitzung gestartet wird.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die Sicherheitswarnung eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.<br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotedesktop ActiveX Steuerelementklassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

