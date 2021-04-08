---
title: MsRdpClient8-Klasse
description: 'Microsoft RDP Client Control (verteilbare Version): Version 9.'
ms.assetid: 877D475B-E2B4-46FB-B7A1-D376F6AE6B8D
ms.tgt_platform: multiple
keywords:
- MsRdpClient8-Klasse Remotedesktopdienste
- MsRdpClient8-Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc1410df2be1b738d217372a563cfdef13cbc3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949616"
---
# <a name="msrdpclient8-class"></a>MsRdpClient8-Klasse

Microsoft RDP-Client Steuerung (Redistributable)-Version 9

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**Imsrdpclient**](imsrdpclientshell2.md)
-   [**Imstscax**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**Imstscaxevents**](imstscaxevents-interface.md)
-   [**Imstscnonscriptable**](imstscnonscriptable-interface.md)
-   [**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
-   [**Imsrdppreferredredirectioninfo**](imsrdppreferredredirectioninfo.md)

**MsRdpClient8** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient8** -Klasse verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](imstscax-connect.md)                                                         | Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.<br/>                                                                                                                                                                                                          |
| [**"Kreatevirtualchannels"**](imstscax-createvirtualchannels.md)                             | Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.<br/>                                                                                                                                                                                              |
| [**Trennen**](imstscax-disconnect.md)                                                   | Trennt die aktive Verbindung.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Ruft die Fehlercodes und Fehlermeldungen ab.<br/>                                                                                                                                                                                                                                      |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                                        | Ruft den Status Text für den angegebenen Statuscode ab.<br/>                                                                                                                                                                                                                           |
| [**Getvirtualchanneloptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.<br/>                                                                                                                                                                                                                                   |
| [**Notifyredirectdevicechange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Benachrichtigt das Geräte Umleitungs Modul des Remotedesktop ActiveX-Steuer Elements, dass eine Geräte Änderung auf dem System aufgetreten ist. Diese Methode übergibt [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Benachrichtigungen an das-Steuerelement.<br/>                                                        |
| [**Onauthenticationwarningverworfen**](imstscaxevents-onauthenticationwarningdismissed.md) | Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.<br/>                                                                                                                                                             |
| [**Onauthenticationwarningangezeigte**](imstscaxevents-onauthenticationwarningdisplayed.md) | Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.<br/>                                                                                                                                                            |
| [**Onautoreconnected**](imstscaxevents-onautoreconnected.md)                               | Wird aufgerufen, wenn das Client Steuerelement automatisch eine Verbindung mit einer Remote Sitzung hergestellt hat.<br/>                                                                                                                                                                                                  |
| [**Onautoreconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem RD-Sitzungshost Server automatisch erneut verbindet.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem RD-Sitzungshost Server automatisch erneut verbindet.<br/>                                                                                                                                                                      |
| [**Onchannelreceiveddata**](imstscaxevents-onchannelreceiveddata.md)                       | Wird aufgerufen, wenn der Client Daten eines Skript fähigen virtuellen Kanals empfängt.<br/>                                                                                                                                                                                                              |
| [**Onconfirmclose**](imstscaxevents-onconfirmclose.md)                                     | Wird aufgerufen, wenn der Client die [**imsrdpclient:: RequestClose**](imsrdpclient-requestclose.md) -Methode aufruft.<br/>                                                                                                                                                                           |
| [**Onconnected**](imstscaxevents-onconnected.md)                                           | Wird aufgerufen, wenn das Client Steuerelement gerade eine Verbindung mit einem RD-Sitzungshost Server herstellt.<br/>                                                                                                                                                                       |
| [**Verbindung wird hergestellt**](imstscaxevents-onconnecting.md)                                         | Wird aufgerufen, wenn das Client Steuerelement mit dem Herstellen einer Verbindung mit einem Server als Reaktion auf einen Aufruf von [**imstscax:: Connect**](imstscax-connect.md)beginnt.<br/>                                                                                                                                               |
| [**Onconnectionbarpulldown**](imstscaxevents-onconnectionbarpulldown.md)                   | Wird aufgerufen, wenn der Benutzer auf die Verbindungs Leiste gezogen hat.<br/>                                                                                                                                                                                                                       |
| [**Onde vicesbuttonpressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Wird aufgerufen, wenn die Schaltfläche Geräte in der Verbindungs Leiste gedrückt wurde.<br/>                                                                                                                                                                                                             |
| [**Nicht getrennt**](imstscaxevents-ondisconnected.md)                                     | Wird aufgerufen, wenn das Client Steuerelement vom RD-Sitzungshost Server getrennt wurde.<br/>                                                                                                                                                                                              |
| [**Onenterfullscreenmode**](imstscaxevents-onenterfullscreenmode.md)                       | Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).<br/>                                                                     |
| [**Onfatalerror**](imstscaxevents-onfatalerror.md)                                         | Wird aufgerufen, wenn das Client Steuerelement einen schwerwiegenden Fehler feststellt.<br/>                                                                                                                                                                                                                           |
| [**Onfocus Released**](imstscaxevents-onfocusreleased.md)                                   | Wird aufgerufen, wenn die Tastenkombination für den releasefokus gedrückt wird. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste drückt.<br/>                                                                                             |
| [**"Onidletimeoutnotification"**](imstscaxevents-onidletimeoutnotification.md)               | Wird aufgerufen, wenn der Benutzer während der von der [**imsrdpclientadvancedsettings::p UT \_ minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) -Methode festgelegten Zeitspanne keine Maus-oder Tastatureingaben hat.<br/>                                                |
| [**Onleavefullscreenmode**](imstscaxevents-onleavefullscreenmode.md)                       | Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).<br/>                                                                     |
| [**Onlogincomplete**](imstscaxevents-onlogincomplete.md)                                   | Wird aufgerufen, wenn sich das Client Steuerelement erfolgreich bei einem RD-Sitzungshost Server angemeldet hat, und zwar nach der Anzeige des Windows-Anmelde Dialogfelds.<br/>                                                                                                                                      |
| [**Onlogonerror**](imstscaxevents-onlogonerror.md)                                         | Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Logon-Ereignis auftritt.<br/>                                                                                                                                                                                                                             |
| [**Onmouseinputmodechanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Wird aufgerufen, wenn sich der Mauseingabe Modus geändert hat.<br/>                                                                                                                                                                                                                                      |
| [**Onnetworkstatuschge**](imstscaxevents-onnetworkstatuschanged.md)                     | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.<br/>                                                                                                                                                                                                                                        |
| [**Onreceivedtspublickey**](imstscaxevents-onreceivedtspublickey.md)                       | Wird während der Verbindungs Sequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn die **notifytspublickey** -Eigenschaft **Variant \_ true** ist.<br/>                                                                                              |
| [**Onremotedesktopsizechange**](imstscaxevents-onremotedesktopsizechange.md)               | Wird aufgerufen, um anzugeben, dass sich die Größe des Client Steuer Elements auf dem Remote Desktop als Reaktion auf einen Client Steuerungs Vorgang geändert hat.<br/>                                                                                                                                                |
| [**"Onremoteprogram" angezeigt**](imstscaxevents-onremoteprogramdisplayed.md)                 | Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.<br/>                                                                                                                                                                                                                                      |
| [**Onremoteprogramresult**](imstscaxevents-onremoteprogramresult.md)                       | Wird aufgerufen, wenn ein RemoteApp-Programm ein Ergebnis an das Client Steuerelement zurückgibt.<br/>                                                                                                                                                                                                            |
| [**"Onremotewindow" angezeigt**](imstscaxevents-onremotewindowdisplayed.md)                   | Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.<br/>                                                                                                                                                                                                                                       |
| [**Onrequestcontainermini mieren**](imstscaxevents-onrequestcontainerminimize.md)             | Wird aufgerufen, wenn der Benutzer auf der Verbindungs Leiste im Vollbildmodus auf die Schaltfläche **minimieren** drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, dass die Containeranwendung sich selbst minimiert.<br/>                                                                                              |
| [**Onrequestgofullscreen**](imstscaxevents-onrequestgofullscreen.md)                       | Wird aufgerufen, wenn der Client anfordert, in den Vollbildmodus zu wechseln, und die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Methode aufgerufen wird, um die **containerhandledfullscreen** -Eigenschaft auf einen Wert ungleich 0 (null) festzulegen.<br/> |
| [**Onrequestleavefullscreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Wird aufgerufen, wenn der Client den Vollbildmodus verlässt und die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Eigenschaft auf einen Wert ungleich 0 (null) festgelegt wurde.<br/>                                                   |
| [**Onservicemess agereceived**](imstscaxevents-onservicemessagereceived.md)                 | Wird aufgerufen, wenn der Client eine Systemmeldung empfängt.<br/>                                                                                                                                                                                                                                  |
| [**Onusernamebezogen**](imstscaxevents-onusernameacquired.md)                             | Wird aufgerufen, wenn der Benutzername vom-Steuerelement abgerufen wurde.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Wird aufgerufen, wenn das Client Steuerelement einen Fehlerzustand erkennt, der nicht schwerwiegend ist.<br/>                                                                                                                                                                                                    |
| [**Verbindung wiederherstellen**](imsrdpclient8-reconnect.md)                                                | Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her.<br/>                                                                                                                                                                                                            |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Fordert ein ordnungsgemäßes Herunterfahren des Client Steuer Elements an.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Setzt alle Kenn Wort Zustände im-Steuerelement zurück.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Sendet eine Reihe von Tastatureingaben an das-Steuerelement. Die Tastatureingaben befinden sich in einem Scan-codeformular, bei dem es sich um die Tastatur Daten aus den eigentlichen physischen Schlüsseln handelt.<br/>                                                                                                                                       |
| [**Sendonvirtualchannel**](imstscax-sendonvirtualchannel.md)                               | Sendet Daten an den RD-Sitzungshost-Server über einen virtuellen Kanal, der zuvor mit der [**imstscax:: foratevirtualchannels**](imstscax-createvirtualchannels.md) -Methode erstellt wurde.<br/>                                                                                         |
| [**Sendremoteaction**](imsrdpclient8-sendremoteaction.md)                                  | Bewirkt, dass eine Aktion in der Remote Sitzung ausgeführt wird.<br/>                                                                                                                                                                                                                            |
| [**Setvirtualchanneloptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Legt die Optionen des virtuellen Kanals für das Client Steuerelement fest.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Die **MsRdpClient8** -Klasse verfügt über diese Eigenschaften.



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
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>Advancedsettings</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein <a href="imstscadvancedsettings-interface.md"><strong>imstscadvancedsettings</strong></a> -Schnittstellen Zeiger.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Zeiger auf die <a href="imsrdpclientadvancedsettings-interface.md"><strong>imsrdpclientadvancedsettings</strong></a> -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Zeiger auf die <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a> -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Zeiger auf die <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a> -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a> -Schnittstellen Zeiger.<br/></td>
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
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7</strong></a> -Schnittstelle unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Eine <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> -Schnittstelle, die das Einstellungs Objekt darstellt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>Allowkredentialsave</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, um das Speichern von Anmelde Informationen zu aktivieren.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>Allowpromptingforanmeldeinformationen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmelde Informationen auffordert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>Binarypassword</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>Binarysalt</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>Chiffrierung</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die maximale Verschlüsselungsstärke des aktuellen Steuer Elements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>Cleartextpassword</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Farbtiefe des aktuellen Steuer Elements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Verbunden</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Der Verbindungsstatus des aktuellen Steuer Elements.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>Connectedstatustext</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Text, der im Client Bereich des Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>Connectingtext</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Der Text, der im Steuerelement zentriert angezeigt wird, während das-Steuerelement eine Verbindung herstellt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>Connectionbartext</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Text Zeichenfolge, die für die Verbindungs Leiste angezeigt werden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Höhe des aktuellen Steuer Elements in Pixel auf dem anfänglichen Remote Desktop.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Breite des aktuellen Steuer Elements in Pixel auf dem anfänglichen Remote Desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Sammlung von PNP-Geräten, die für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>Disableconnectionbar</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungs Leiste deaktivieren soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>Disableremoteappcapscheck</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>Disconnectedtext</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Der Text, der im-Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Domain</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Domäne, an der der aktuelle Benutzer sich anmeldet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>Drivecollection</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Sammlung von Festplatten Laufwerken, die für die Umleitung verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>Enablekredsspsupport</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob "kredssp" für diese Verbindung aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>Extendeddisconnecverrat</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Erweiterte Informationen über den Grund für das Trennen der Verbindung des Client Steuer Elements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>Fullscrebereberechtigen</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>Getremotemonitorsboundingbox</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt das Begrenzungs Rechteck des Remote Monitors an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>Horizontalscrollbarvisible</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Steuerelement eine horizontale Schiebe Leiste angezeigt hat.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>Launchedviaclientshellinterface</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der Benutzer das Client Steuerelement über die RD-Webzugriff Schnittstelle gestartet hat.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>Markrdpsettingssecure</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob RDP-Einstellungen als sicher gekennzeichnet sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>Msrdpclientshell</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Client Einstellungen für das Webportal-Start Programm.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>Aushandatesecuritylayer</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die aushandatesecuritylayer-Einstellung für diese Verbindung unterstützt wird.<br/>
<blockquote>
[!Note]<br />
Wenn " <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>kredsspsupport</strong></a> " aktiviert ist und auf dem Client vorhanden ist, oder wenn Secure Sockets Layer (SSL) mit Benutzerauthentifizierung aktiviert ist, wird "aushandatesecuritylayer" ignoriert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>Portablepassword</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>Portablesalt</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>Promptfor-Anmelde Informationen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Dialogfeld Eingabeaufforderung für Anmelde Informationen angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>Promptforkredsonclient</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Client Steuerelement ein Dialogfeld anzeigt, in dem Anmelde Informationen angefordert werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>Publishercertificatechain</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt die Herausgeber Zertifikat Kette an. Die Kette wird in einer Variante vom Typ VT_BYREF gespeichert, die einen Zeiger auf eine <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> Struktur enthält.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>Redirectdynamicdevices</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob dynamisch angefügte PNP-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>Redirectdynamicdrives</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob dynamisch angefügte PNP-Laufwerke, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>Redirectionwarningtype</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Steuert das vorhanden sein und das Erscheinungsbild des Dialog Felds Umleitung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>Remotemonitorcount</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt die Anzahl der Remote Monitore an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>Remotemonitorlayoutmatcheslocal</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Remote Monitor Layout mit dem Layout des lokalen Monitors identisch ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>Remoteprogram</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die RemoteApp-Client Einstellung.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2</strong></a> -Schnittstelle unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>Securedsettings</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein <a href="imstscsecuredsettings-interface.md"><strong>imstscsecuredsettings</strong></a> -Schnittstellen Zeiger.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Zeiger auf die <a href="imsrdpclientsecuredsettings-interface.md"><strong>imsrdpclientsecuredsettings</strong></a> -Schnittstelle, die verwendet wird, um gesicherte Einstellungen für das Client Steuerelement festzulegen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2</strong></a> -Schnittstelle unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>Securedsettingsenabled</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob die <a href="imstscsecuredsettings-interface.md"><strong>imstscsecuredsettings</strong></a> -Schnittstelle verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Servers</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>Showredirectionwarningdialog</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Dialogfeld für die Umleitung der Sicherheitswarnung angezeigt werden soll, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>Startconnected</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Steuerelement beim Start sofort die RD-Sitzungshost Server-Verbindung herstellen soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Client RD-Gateway Einstellung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Schnittstelle zu <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ein Objekt, das die <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3</strong></a> -Schnittstelle unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>Treuhand Website</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites des Client Computers enthalten ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>Uianentwindowhandle</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Das Fenster Handle, das das übergeordnete Fenster für das-Steuerelement sein soll. Dadurch können alle Fenster, die vom Steuerelement angezeigt werden, in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>Usemultimon</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Remotedesktop ActiveX-Steuerelement mehrere Monitore verwenden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>Useredirectionservername</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der Umleitungs Servername verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>User</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Die Anmelde Informationen für den Benutzernamen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Version</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Die Versionsnummer des aktuellen Steuer Elements.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>Verticalscrollbarvisible</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Gibt an, ob das Steuerelement eine vertikale Bild Lauf Leiste anzeigt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>Warnaboutclipboardredirection</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Dialogfeld Sicherheitswarnung eine Warnung bezüglich der Zwischenablage Umleitung enthalten soll, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>Warnaboutdirectxredirect</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Diese Eigenschaft wird nicht verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>Warnaboutprinterredirect</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob das Dialogfeld Umleitung eine Meldung zur Drucker Umleitung anzeigt, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>Warnaboutsendinganmelde Informationen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop ActiveX-Steuerelement Klassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

