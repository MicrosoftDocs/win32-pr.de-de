---
title: MsRdpClient6NotSafeForScripting-Klasse
description: 'Microsoft RDP-Clientsteuerung: Version 7.'
ms.assetid: D34BDA07-986C-4BA7-B454-3E9DC1A7BA1E
ms.tgt_platform: multiple
keywords:
- MsRdpClient6NotSafeForScripting-Klasse Remotedesktopdienste
- MsRdpClient6NotSafeForScripting-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient6NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a18900084f063610c4b761a8643ef30bda9c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467066"
---
# <a name="msrdpclient6notsafeforscripting-class"></a>MsRdpClient6NotSafeForScripting-Klasse

Microsoft RDP-Clientsteuerung – Version 7

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IMsRdpClient6**](imsrdpclient6.md)
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
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)

**MsRdpClient6NotSafeForScripting** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient6NotSafeForScripting-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](imstscax-connect.md)                                                         | Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das Steuerelement festgelegt sind.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Erstellt ein clientseitiges virtuelles Kanalobjekt für jeden angegebenen Namen des virtuellen Kanals.<br/>                                                                                                                                                                                              |
| [**Trennen**](imstscax-disconnect.md)                                                   | Trennt die aktive Verbindung.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Ruft die Fehlercodes und Fehlermeldungen ab.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Ruft die für einen virtuellen Kanal festgelegten Optionen ab.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Benachrichtigt das Modul für die Geräteumleitung über die Remotedesktop ActiveX, dass eine Geräteänderung auf dem System aufgetreten ist. Diese Methode übergibt [**WM \_ DEVICECHANGE-Benachrichtigungen**](/windows/desktop/DevIO/wm-devicechange) an das Steuerelement.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Dialogfeld zertifikatfehler).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Dialogfeld "Zertifikatfehler").<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Wird aufgerufen, wenn das Clientsteuerelement automatisch wieder eine Verbindung mit einer Remotesitzung hergestellt hat.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Wird aufgerufen, wenn ein Client gerade eine Sitzung automatisch mit einem RD-Sitzungshost Server verbindet.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Wird aufgerufen, wenn ein Client gerade eine Sitzung automatisch mit einem RD-Sitzungshost Server verbindet.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Wird aufgerufen, wenn der Client Daten in einem skriptfähigen virtuellen Kanal empfängt.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Wird aufgerufen, wenn der Client die [**IMsRdpClient::RequestClose-Methode**](imsrdpclient-requestclose.md) aufruft.<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Wird aufgerufen, wenn das Clientsteuerelement gerade eine Verbindung mit einem RD-Sitzungshost Server herstellen soll.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Wird aufgerufen, wenn das Clientsteuerelement als Reaktion auf einen Aufruf von [**IMsTscAx::Verbinden**](imstscax-connect.md)eine Verbindung mit einem Server herstellt.<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Wird aufgerufen, wenn der Benutzer auf der Verbindungsleiste nach unten gezogen wurde.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Wird aufgerufen, wenn die Geräteschaltfläche in der Verbindungsleiste gedrückt wurde.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Wird aufgerufen, wenn das Clientsteuerelement vom RD-Sitzungshost Server getrennt wurde.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die [Tastenkombination](terminal-services-shortcut-keys.md) im Vollbildmodus drückt (STRG+ALT+BREAK).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Wird aufgerufen, wenn beim Clientsteuerelement ein schwerwiegender Fehler auftritt.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Wird aufgerufen, wenn die Tastenkombination des Releasefokus gedrückt wird. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer strg+ALT+NACH-LINKS-TASTE oder die Tastenkombination STRG+ALT+NACH-RECHTS drückt.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Wird aufgerufen, wenn während des zeitraums, der von der [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout-Methode**](imsrdpclientadvancedsettings-minutestoidletimeout.md) festgelegt wurde, keine Maus- oder Tastatureingabe vom Benutzer erfolgt ist.<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die [Tastenkombination](terminal-services-shortcut-keys.md) im Vollbildmodus drückt (STRG+ALT+BREAK).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Wird aufgerufen, wenn sich das Clientsteuerelement erfolgreich bei einem RD-Sitzungshost-Server angemeldet hat. Folgen Sie dazu der Anzeige des Dialogfelds Windows Anmeldung.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Anmeldeereignis auftritt.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Wird aufgerufen, wenn sich der Mauseingabemodus geändert hat.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Wird während der Verbindungssequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn die **NotifyTSPublicKey-Eigenschaft** **VARIANT \_ TRUE** ist.<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Wird aufgerufen, um anzugeben, dass sich die Größe des Clientsteuerelements auf dem Remotedesktop als Reaktion auf einen Clientsteuerelementvorgang geändert hat.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Clientsteuerelement zurückgibt.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Wird aufgerufen, wenn der Benutzer die Schaltfläche **Minimieren** auf der Verbindungsleiste im Vollbildmodus drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, die die Containeranwendung selbst minimiert.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Wird aufgerufen, wenn der Client den Wechsel in den Vollbildmodus anfordert und die [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen-Methode**](imstscadvancedsettings-containerhandledfullscreen.md) aufgerufen wird, um die **ContainerHandledFullScreen-Eigenschaft** auf einen Wert ungleich 0 (null) festzulegen.<br/> |
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

Die **MsRdpClient6NotSafeForScripting-Klasse** verfügt über diese Eigenschaften.




| Eigenschaft | Zugriffstyp | BESCHREIBUNG | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br /> | Schreibgeschützt<br /> | Ein <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings-Schnittstellenzeiger.</strong></a><br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br /> | Schreibgeschützt<br /> | Ein <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4-Schnittstellenzeiger.</strong></a><br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br /> | Schreibgeschützt<br /> | Die Schnittstelle zu <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5.</strong></a><br /> | 
| <a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br /> | Schreibgeschützt<br /> | Die Schnittstelle zu <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6.</strong></a><br /> | 
| <a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob im Dialogfeld "Anmeldeinformationen" ein Kontrollkästchen zum Speichern von Anmeldeinformationen angezeigt wird.<br /> | 
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
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | Schreibgeschützt<br /> | Erweiterte Informationen zum Grund für die Trennung der Verbindung des Clientsteuer steuerelements.<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>Fullscreen</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | Lesegeschützt<br /> | Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | Schreibgeschützt<br /> | Gibt an, ob das Steuerelement eine horizontale Scrollleiste angezeigt hat.<br /> | 
| <a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob der Benutzer das Clientsteuersystem mithilfe der RD-Webzugriff gestartet hat.<br /> | 
| <a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob RDP-Einstellungen als sicher markiert sind.<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | Schreibgeschützt<br /> | Die Clienteinstellungen für das Webportal-Startfeld.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die NegotiateSecurityLayer-Einstellung für diese Verbindung unterstützt wird.<br /><blockquote>[!Note]<br />Wenn <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> aktiviert und auf dem Client vorhanden ist, oder wenn Secure Sockets Layer (SSL) mit Benutzerauthentifizierung aktiviert ist, wird NegotiateSecurityLayer ignoriert.</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | Lesen/Schreiben<br /> | Diese Eigenschaft wird nicht unterstützt.<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | Lesen/Schreiben<br /> | Diese Eigenschaft wird nicht unterstützt.<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Eingabeaufforderung für Anmeldeinformationen" angezeigt werden soll.<br /> | 
| <a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Clientsteuerfeld ein Dialogfeld anzeigt, das zur Eingabe von Anmeldeinformationen aufgefordert wird.<br /> | 
| <a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br /> | Lesen/Schreiben<br /> | Gibt die Herausgeberzertifikatkette an. Die Kette wird in einer Variante des Typs VT_BYREF gespeichert, die einen Zeiger auf eine <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> enthält.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob dynamisch angeschlossene PnP-Geräte, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob dynamisch angefügte PnP-Laufwerke, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br /> | Lesen/Schreiben<br /> | Steuert das Vorhandensein und die Darstellung des Umleitungsdialogfelds.<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | Schreibgeschützt<br /> | Die RemoteApp-Clienteinstellung.<br /> | 
| <a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br /> | Schreibgeschützt<br /> | Ein <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings-Schnittstellenzeiger.</strong></a><br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | Schreibgeschützt<br /> | Zeiger auf die <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings-Schnittstelle,</strong></a> die zum Festlegen geschützter Einstellungen für das Clientsteuerfeld verwendet wird.<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | Schreibgeschützt<br /> | Gibt an, ob <a href="imstscsecuredsettings-interface.md"><strong>die IMsTscSecuredSettings-Schnittstelle</strong></a> verfügbar ist.<br /> | 
| <a href="imstscax-server.md"><strong>Server</strong></a><br /> | Lesen/Schreiben<br /> | Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Sicherheitswarnung für Umleitung" angezeigt werden soll, bevor eine Sitzung gestartet wird.<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Steuerelement die Serververbindung RD-Sitzungshost beim Start eingibt.<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | Schreibgeschützt<br /> | Die Client-RD-Gatewayeinstellung.<br /> | 
| <a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br /> | Schreibgeschützt<br /> | Die Schnittstelle zu <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2.</strong></a><br /> | 
| <a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites des Clientcomputers enthalten ist.<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | Lesen/Schreiben<br /> | Das Fensterhand handle, das als übergeordnetes Fenster für das Steuerelement verwendet werden soll. Dadurch können alle fenster, die vom -Steuerelement angezeigt werden, in Bezug auf alle fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br /> | 
| <a href="imstscax-username.md"><strong>Nutzername</strong></a><br /> | Lesen/Schreiben<br /> | Die Anmeldeinformationen für den Benutzernamen.<br /> | 
| <a href="imstscax-version.md"><strong>Version</strong></a><br /> | Schreibgeschützt<br /> | Die Versionsnummer des aktuellen Steuerelements.<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | Schreibgeschützt<br /> | Gibt an, ob das Steuerelement eine vertikale Bildlaufleiste anzeigt.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Sicherheitswarnung" eine Warnung zur Umleitung der Zwischenablage enthalten soll, bevor eine Sitzung gestartet wird.<br /> | 
| <a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob im Dialogfeld "Umleitung" eine Meldung zur Druckerumleitung angezeigt wird, bevor eine Sitzung gestartet wird.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die Sicherheitswarnung eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.<br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotedesktop ActiveX Steuerelementklassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

