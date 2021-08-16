---
title: MsRdpClient10NotSafeForScripting-Klasse
description: 'Microsoft RDP-Clientsteuerung: Version 11.'
ms.assetid: AAC3DA65-222D-498F-B9C3-A8CBCB722D9D
ms.tgt_platform: multiple
keywords:
- MsRdpClient10NotSafeForScripting-Klasse Remotedesktopdienste
- MsRdpClient10NotSafeForScripting-Klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient10NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04b7d11d0177c2ee91e4b1c2c536ba2f029489c0f1aee3b0a3475cccb66291c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350307"
---
# <a name="msrdpclient10notsafeforscripting-class"></a>MsRdpClient10NotSafeForScripting-Klasse

Microsoft RDP-Clientsteuerung – Version 11

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IMsRdpClient10**](imsrdpclient10.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
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
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
-   [**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
-   [**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)

**MsRdpClient10NotSafeForScripting** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient10NotSafeForScripting-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attachevent**](imsrdpclient9-attachevent.md)                                            | Angefügt ein Ereignis. <br/>                                                                                                                                                                                                                                                                |
| [**Verbinden**](imstscax-connect.md)                                                         | Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das -Steuerelement festgelegt sind.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Erstellt ein clientseitiges virtuelles Kanalobjekt für jeden angegebenen Namen des virtuellen Kanals.<br/>                                                                                                                                                                                              |
| [**Detachevent**](imsrdpclient9-detachevent.md)                                            | Trennt ein Ereignis. <br/>                                                                                                                                                                                                                                                                |
| [**Trennen**](imstscax-disconnect.md)                                                   | Trennt die aktive Verbindung.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Ruft die Fehlercodes und Fehlermeldungen ab.<br/>                                                                                                                                                                                                                                      |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                                        | Ruft den Statustext für den angegebenen Statuscode ab.<br/>                                                                                                                                                                                                                           |
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
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Wird aufgerufen, wenn der Benutzername vom -Steuerelement übernommen wurde.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Wird aufgerufen, wenn das Clientsteuer steuerelement einen Fehlerzustand trifft, der nicht schwerwiegender ist.<br/>                                                                                                                                                                                                    |
| [**Verbindung wiederherstellen**](imsrdpclient8-reconnect.md)                                                | Verbindet sich mit der neuen Desktopbreite und -höhe erneut mit der Remotesitzung.<br/>                                                                                                                                                                                                            |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Fordert ein ordnungsgemäßes Herunterfahren des Clientsteuer steuerelements an.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Setzt alle Kennwortzustände im Steuerelement zurück.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Sendet eine Reihe von Tastatureingaben an das Steuerelement. Die Tastatureingaben sind in Scancodeform, d.&a0;b. den Tastaturdaten der tatsächlichen physischen Tasten.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Sendet Daten an den RD-Sitzungshost-Server über einen virtuellen Kanal, der zuvor mithilfe der [**IMsTscAx::CreateVirtualChannels-Methode erstellt**](imstscax-createvirtualchannels.md) wurde.<br/>                                                                                         |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                                  | Bewirkt, dass eine Aktion in der Remotesitzung ausgeführt wird.<br/>                                                                                                                                                                                                                            |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Legt die Optionen für den virtuellen Kanal für das Clientsteuer steuerelement fest.<br/>                                                                                                                                                                                                                           |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)              | Synchronisiert Einstellungen für die Sitzungsanzeige. <br/>                                                                                                                                                                                                                                            |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85))          | Aktualisiert einstellungen für die Sitzungsanzeige. <br/>                                                                                                                                                                                                                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **MsRdpClient10NotSafeForScripting-Klasse** verfügt über diese Eigenschaften.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Eigenschaft</th>
<th style="text-align: left;">Zugriffstyp</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings-Schnittstellenzeiger.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Zeiger auf die <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerfeld verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Zeiger auf die <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerfeld verwendet wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Zeiger auf die <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3-Schnittstelle,</strong></a> die zum Festlegen erweiterter Einstellungen für das Clientsteuerfeld verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4-Schnittstellenzeiger.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Schnittstelle zu <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Schnittstelle zu <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7-Schnittstelle</strong></a> unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Eine <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8-Schnittstelle,</strong></a> die das Einstellungsobjekt darstellt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob im Dialogfeld "Anmeldeinformationen" ein Kontrollkästchen zum Speichern von Anmeldeinformationen angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>AllowPromptingForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmeldeinformationen auffordern kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die maximale Verschlüsselungsstärke des aktuellen Steuerelements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Das Remotedesktop ActiveX-Steuerelementkennwort im Klartextformat.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Farbtiefe des aktuellen Steuerelements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Verbunden</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Der Verbindungsstatus des aktuellen Steuerelements.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Text, der im Clientbereich des Steuerelements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Der Text, der zentriert im -Steuerelement angezeigt wird, während das Steuerelement eine Verbindung verbindet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Textzeichenfolge, die für die Verbindungsleiste angezeigt werden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Höhe des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Breite des aktuellen Steuerelements auf dem ursprünglichen Remotedesktop in Pixel.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Sammlung von PnP-Geräten, die für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>DisableConnectionBar</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX die Verbindungsleiste deaktivieren soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>DisableRemoteAppCapsCheck</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Der Text, der im -Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Domain</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Domäne, bei der sich der aktuelle Benutzer anmeldet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Auflistung der Datenträgerlaufwerke, die für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob CredSSP für diese Verbindung aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Erweiterte Informationen zum Grund für die Trennung der Verbindung des Clientsteuer steuerelements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>Fullscreen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>GetRemoteMonitorsBoundingBox</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt das umgebundene Rechteck des Remotemonitors an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Steuerelement eine horizontale Bildlaufleiste angezeigt hat.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der Benutzer das Clientsteuer steuerelement mithilfe der RD-Webzugriff gestartet hat.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob RDP-Einstellungen als sicher markiert sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Clienteinstellungen für das Webportal-Startfeld.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die NegotiateSecurityLayer-Einstellung für diese Verbindung unterstützt wird.<br/>
<blockquote>
[!Note]<br />
Wenn <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport aktiviert</strong></a> und auf dem Client vorhanden ist, oder wenn Secure Sockets Layer (SSL) mit Benutzerauthentifizierung aktiviert ist, wird NegotiateSecurityLayer ignoriert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Dialogfeld "Eingabeaufforderung für Anmeldeinformationen" angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Clientsteuerfeld ein Dialogfeld anzeigt, das zur Eingabe von Anmeldeinformationen aufgefordert wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>Eigenschaft</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Enthält eine benannte Eigenschaft.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt die Herausgeberzertifikatkette an. Die Kette wird in einer Variante des Typs VT_BYREF gespeichert, die einen Zeiger auf eine <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> enthält.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob dynamisch angeschlossene PnP-Geräte, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob dynamisch angefügte PnP-Laufwerke, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Steuert das Vorhandensein und die Darstellung des Umleitungsdialogfelds.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>RemoteMonitorCount</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt die Anzahl der Remotemonitore an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>RemoteMonitorLayoutMatchesLocal</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Layout des Remotemonitors mit dem Layout des lokalen Monitors identisch ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die RemoteApp-Clienteinstellung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2-Schnittstelle</strong></a> unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient10-remoteprogram3.md"><strong>RemoteProgram3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="itsremoteprogram3.md"><strong>ITSRemoteProgram3-Schnittstelle</strong></a> unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings-Schnittstellenzeiger.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Zeiger auf die <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings-Schnittstelle,</strong></a> die zum Festlegen geschützter Einstellungen für das Clientsteuerelement verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2-Schnittstelle</strong></a> unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob die <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings-Schnittstelle</strong></a> verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Server</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Dialogfeld "Umleitungssicherheitswarnung" vor dem Starten einer Sitzung angezeigt werden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Steuerelement die RD-Sitzungshost Serververbindung sofort beim Start herstellt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Rd-Gatewayeinstellung des Clients.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Schnittstelle zu <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3-Schnittstelle</strong></a> unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient9-transportsettings4.md"><strong>TransportSettings4</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclienttransportsettings4.md"><strong>IMsRdpClientTransportSettings4-Schnittstelle</strong></a> unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Website, von der aus der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Websites des Clientcomputers enthalten ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Das Fensterhandle, das das übergeordnete Fenster für das Steuerelement sein soll. Dadurch können alle vom Steuerelement angezeigten Fenster in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>UseMultimon</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX-Steuerelement mehrere Monitore verwenden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>UseRedirectionServerName</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der Umleitungsservername verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>Nutzername</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Anmeldeinformationen für den Benutzernamen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Version</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Versionsnummer des aktuellen Steuerelements.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Steuerelement eine vertikale Bildlaufleiste anzeigt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Sicherheitswarnungsdialogfeld eine Warnung zur Umleitung der Zwischenablage enthalten soll, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>WarnAboutDirectXRedirection</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht verwendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob im Dialogfeld "Umleitung" eine Meldung zur Druckerumleitung angezeigt wird, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Sicherheitswarnung eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                        |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                |
| CLSID<br/>                    | CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotedesktop ActiveX Steuerelementklassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

