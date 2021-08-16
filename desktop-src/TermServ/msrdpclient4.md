---
title: MsRdpClient4-Klasse
description: 'Microsoft RDP-Clientsteuerung (verteilbar): Version 5.'
ms.assetid: 3F238C63-E860-4F27-B3D6-29F03B22E49E
ms.tgt_platform: multiple
keywords:
- MsRdpClient4-Klasse Remotedesktopdienste
- MsRdpClient4-Klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6b4300bcad7544793f3c958809f78a0c1b1203618ccf21688f9fc0ac483faa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350242"
---
# <a name="msrdpclient4-class"></a>MsRdpClient4-Klasse

Microsoft RDP-Clientsteuerung (verteilbar): Version 5

Diese Klasse implementiert die folgenden Schnittstellen.

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

**MsRdpClient4 verfügt** über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient4-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
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
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Wird aufgerufen, wenn sich das Clientsteuerfeld erfolgreich bei einem RD-Sitzungshost server angemeldet hat. Folgen Sie der Anzeige des Dialogfelds Windows Anmeldung.<br/>                                                                                                                                      |
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
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Wird aufgerufen, wenn der Client den Vollbildmodus verlassen möchte und die [**Eigenschaft IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) auf einen Wert ungleich 0 festgelegt wurde.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Wird aufgerufen, wenn der Client eine Systemmeldung empfängt.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Wird aufgerufen, wenn der Benutzername vom Steuerelement abgerufen wurde.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Wird aufgerufen, wenn das Clientsteuerelement eine Fehlerbedingung erkennt, die nicht schwerwiegend ist.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Fordert ein ordnungsgemäßes Herunterfahren des Clientsteuerelements an.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Setzt alle Kennwortzustände im Steuerelement zurück.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Sendet eine Reihe von Tastatureingaben an das Steuerelement. Die Tastatureingaben befinden sich in Scancodeform, d.h. den Tastaturdaten der tatsächlichen physischen Tasten.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Sendet Daten über einen virtuellen Kanal, der zuvor mithilfe der [**IMsTscAx::CreateVirtualChannels-Methode**](imstscax-createvirtualchannels.md) erstellt wurde, an den RD-Sitzungshost Server.<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Legt die Optionen für den virtuellen Kanal für das Clientsteuerelement fest.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Die **MsRdpClient4-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                           | Schreibgeschützt<br/>  | Ein [**IMsTscAdvancedSettings-Schnittstellenzeiger.**](imstscadvancedsettings-interface.md)<br/>                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>                     | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings-Schnittstelle,**](imsrdpclientadvancedsettings-interface.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br/>                                    |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>                    | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings2-Schnittstelle,**](imsrdpclientadvancedsettings2.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br/>                                            |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>                    | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings3-Schnittstelle,**](imsrdpclientadvancedsettings3.md) die zum Festlegen erweiterter Einstellungen für das Clientsteuerelement verwendet wird.<br/>                                            |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>                    | Schreibgeschützt<br/>  | Ein [**IMsRdpClientAdvancedSettings4-Schnittstellenzeiger.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                                      |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>                    | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                            | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                                                   |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                               | Schreibgeschützt<br/>  | Die maximale Verschlüsselungsstärke des aktuellen Steuerelements.<br/>                                                                                                                                           |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>              | Lesegeschützt<br/> | Der Remotedesktop ActiveX Steuerelementkennwort im Klartextformat.<br/>                                                                                                                                 |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                                   | Lesen/Schreiben<br/> | Farbtiefe des aktuellen Steuerelements.<br/>                                                                                                                                                               |
| [**Verbunden**](imstscax-connected.md)<br/>                                         | Schreibgeschützt<br/>  | Der Verbindungsstatus des aktuellen Steuerelements.<br/>                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>                | Lesen/Schreiben<br/> | Text, der im Clientbereich des Steuerelements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                                                             |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                               | Lesen/Schreiben<br/> | Der Text, der im Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.<br/>                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                                 | Lesen/Schreiben<br/> | Die Höhe des aktuellen Steuerelements auf dem ersten Remotedesktop in Pixel.<br/>                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                                   | Lesen/Schreiben<br/> | Die Breite des aktuellen Steuerelements auf dem ersten Remotedesktop in Pixel.<br/>                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                           | Lesen/Schreiben<br/> | Der Text, der im Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/>                                                                                                                  |
| [**Domain**](imstscax-domain.md)<br/>                                               | Lesen/Schreiben<br/> | Die Domäne, bei der sich der aktuelle Benutzer anmeldet.<br/>                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/>       | Schreibgeschützt<br/>  | Erweiterte Informationen zum Grund der Trennung des Clientsteuerelements.<br/>                                                                                                                         |
| [**Fullscreen**](imsrdpclient-fullscreen.md)<br/>                                   | Lesen/Schreiben<br/> | Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                                                             |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                             | Lesegeschützt<br/> | Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/>       | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine horizontale Bildlaufleiste angezeigt hat.<br/>                                                                                                                              |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>                | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                        | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                                                   |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                             | Schreibgeschützt<br/>  | Ein [**IMsTscSecuredSettings-Schnittstellenzeiger.**](imstscsecuredsettings-interface.md)<br/>                                                                                                             |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                       | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientSecuredSettings-Schnittstelle,**](imsrdpclientsecuredsettings-interface.md) die zum Festlegen geschützter Einstellungen für das Clientsteuerelement verwendet wird.<br/>                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>               | Schreibgeschützt<br/>  | Gibt an, ob die [**IMsTscSecuredSettings-Schnittstelle**](imstscsecuredsettings-interface.md) verfügbar ist.<br/>                                                                                    |
| [**Server**](imstscax-server.md)<br/>                                               | Lesen/Schreiben<br/> | Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br/>                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                               | Lesen/Schreiben<br/> | Gibt an, ob das Steuerelement die RD-Sitzungshost Serververbindung sofort beim Start herstellt.<br/>                                                                                      |
| [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)<br/> | Lesen/Schreiben<br/> | Das Fensterhandle, das das übergeordnete Fenster für das Steuerelement sein soll. Dadurch können alle vom Steuerelement angezeigten Fenster in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br/> |
| [**Nutzername**](imstscax-username.md)<br/>                                           | Lesen/Schreiben<br/> | Die Anmeldeinformationen für den Benutzernamen.<br/>                                                                                                                                                                   |
| [**Version**](imstscax-version.md)<br/>                                             | Schreibgeschützt<br/>  | Die Versionsnummer des aktuellen Steuerelements.<br/>                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>           | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine vertikale Bildlaufleiste anzeigt.<br/>                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient4 ist als 4EDCB26C-D24C-4E72-AF07-B576699AC0DE definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotedesktop ActiveX-Steuerelementklassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

