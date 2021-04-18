---
title: MsRdpClient3NotSafeForScripting-Klasse
description: Microsoft RDP-Client Steuerung-Version 4.
ms.assetid: F8123627-3561-45F6-81AD-41D1147E449D
ms.tgt_platform: multiple
keywords:
- MsRdpClient3NotSafeForScripting-Klasse Remotedesktopdienste
- MsRdpClient3NotSafeForScripting-Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- MsRdpClient3NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce431ad60fae8edc82a33dbf65038f7aa38c3b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340012"
---
# <a name="msrdpclient3notsafeforscripting-class"></a>MsRdpClient3NotSafeForScripting-Klasse

Microsoft RDP-Client Steuerung-Version 4

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**Imsrdpclient**](imsrdpclientshell2.md)
-   [**Imstscax**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**Imstscaxevents**](imstscaxevents-interface.md)
-   [**Imstscnonscriptable**](imstscnonscriptable-interface.md)
-   [**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)

**MsRdpClient3NotSafeForScripting** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MsRdpClient3NotSafeForScripting** -Klasse verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](imstscax-connect.md)                                                         | Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.<br/>                                                                                                                                                                                                          |
| [**"Kreatevirtualchannels"**](imstscax-createvirtualchannels.md)                             | Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.<br/>                                                                                                                                                                                              |
| [**Trennen**](imstscax-disconnect.md)                                                   | Trennt die aktive Verbindung.<br/>                                                                                                                                                                                                                                                 |
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
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Fordert ein ordnungsgemäßes Herunterfahren des Client Steuer Elements an.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Setzt alle Kenn Wort Zustände im-Steuerelement zurück.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Sendet eine Reihe von Tastatureingaben an das-Steuerelement. Die Tastatureingaben befinden sich in einem Scan-codeformular, bei dem es sich um die Tastatur Daten aus den eigentlichen physischen Schlüsseln handelt.<br/>                                                                                                                                       |
| [**Sendonvirtualchannel**](imstscax-sendonvirtualchannel.md)                               | Sendet Daten an den RD-Sitzungshost-Server über einen virtuellen Kanal, der zuvor mit der [**imstscax:: foratevirtualchannels**](imstscax-createvirtualchannels.md) -Methode erstellt wurde.<br/>                                                                                         |
| [**Setvirtualchanneloptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Legt die Optionen des virtuellen Kanals für das Client Steuerelement fest.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Die **MsRdpClient3NotSafeForScripting** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Advancedsettings**](imstscax-advancedsettings.md)<br/>                     | Schreibgeschützt<br/>  | Ein [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger.<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Ein Zeiger auf die [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Schreibgeschützt<br/>  | Zeiger auf die [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle, die verwendet wird, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/>         |
| [**Binarypassword**](imstscnonscriptable-binarypassword.md)<br/>              | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**Binarysalt**](imstscnonscriptable-binarysalt.md)<br/>                      | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**Chiffrierung**](imstscax-cipherstrength.md)<br/>                         | Schreibgeschützt<br/>  | Die maximale Verschlüsselungsstärke des aktuellen Steuer Elements.<br/>                                                                                                        |
| [**Cleartextpassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | Lesegeschützt<br/> | Das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format.<br/>                                                                                              |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Farbtiefe des aktuellen Steuer Elements.<br/>                                                                                                                            |
| [**Verbunden**](imstscax-connected.md)<br/>                                   | Schreibgeschützt<br/>  | Der Verbindungsstatus des aktuellen Steuer Elements.<br/>                                                                                                                   |
| [**Connectedstatustext**](imsrdpclient2-connectedstatustext.md)<br/>          | Lesen/Schreiben<br/> | Text, der im Client Bereich des Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                          |
| [**Connectingtext**](imstscax-connectingtext.md)<br/>                         | Lesen/Schreiben<br/> | Der Text, der im Steuerelement zentriert angezeigt wird, während das-Steuerelement eine Verbindung herstellt.<br/>                                                                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lesen/Schreiben<br/> | Die Höhe des aktuellen Steuer Elements in Pixel auf dem anfänglichen Remote Desktop.<br/>                                                                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lesen/Schreiben<br/> | Die Breite des aktuellen Steuer Elements in Pixel auf dem anfänglichen Remote Desktop.<br/>                                                                                         |
| [**Disconnectedtext**](imstscax-disconnectedtext.md)<br/>                     | Lesen/Schreiben<br/> | Der Text, der im-Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.<br/>                                                                               |
| [**Domain**](imstscax-domain.md)<br/>                                         | Lesen/Schreiben<br/> | Die Domäne, an der der aktuelle Benutzer sich anmeldet.<br/>                                                                                                                  |
| [**Extendeddisconnecverrat**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Erweiterte Informationen über den Grund für das Trennen der Verbindung des Client Steuer Elements.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Gibt an, ob sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                                          |
| [**Fullscrebereberechtigen**](imstscax-fullscreentitle.md)<br/>                       | Lesegeschützt<br/> | Der Fenstertitel, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.<br/>                                                                                            |
| [**Horizontalscrollbarvisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine horizontale Schiebe Leiste angezeigt hat.<br/>                                                                                           |
| [**Portablepassword**](imstscnonscriptable-portablepassword.md)<br/>          | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**Portablesalt**](imstscnonscriptable-portablesalt.md)<br/>                  | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht unterstützt.<br/>                                                                                                                                |
| [**Securedsettings**](imstscax-securedsettings.md)<br/>                       | Schreibgeschützt<br/>  | Ein [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstellen Zeiger.<br/>                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Ein Zeiger auf die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle, die verwendet wird, um gesicherte Einstellungen für das Client Steuerelement festzulegen.<br/>    |
| [**Securedsettingsenabled**](imstscax-securedsettingsenabled.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob die [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle verfügbar ist.<br/>                                                 |
| [**Servers**](imstscax-server.md)<br/>                                         | Lesen/Schreiben<br/> | Der Name des Servers, mit dem das aktuelle Steuerelement verbunden ist.<br/>                                                                                              |
| [**Startconnected**](imstscax-startconnected.md)<br/>                         | Lesen/Schreiben<br/> | Gibt an, ob das Steuerelement beim Start sofort die RD-Sitzungshost Server-Verbindung herstellen soll.<br/>                                                   |
| [**User**](imstscax-username.md)<br/>                                     | Lesen/Schreiben<br/> | Die Anmelde Informationen für den Benutzernamen.<br/>                                                                                                                                |
| [**Version**](imstscax-version.md)<br/>                                       | Schreibgeschützt<br/>  | Die Versionsnummer des aktuellen Steuer Elements.<br/>                                                                                                                     |
| [**Verticalscrollbarvisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Schreibgeschützt<br/>  | Gibt an, ob das Steuerelement eine vertikale Bild Lauf Leiste anzeigt.<br/>                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | CLSID \_ MsRdpClient3NotSafeForScripting ist als ACE575FD-1F-4074-9401-EBAB990FA9DE definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop ActiveX-Steuerelement Klassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

