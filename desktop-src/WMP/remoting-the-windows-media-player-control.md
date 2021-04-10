---
title: Remoting des Windows Media Player-Steuerelements
description: Remoting des Windows Media Player-Steuerelements
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Remoting-ActiveX-Steuerelement
- Windows Media Player-Objektmodell, Remote-ActiveX-Steuerelement
- Objektmodell, Remote-ActiveX-Steuerelement
- Windows Media Player Mobile, Remoting-ActiveX-Steuerelement
- Windows Media Player ActiveX-Steuerelement, Remoting
- Windows Media Player Mobile ActiveX-Steuerelement, Remoting
- ActiveX-Steuerelement, Remoting
- Remoting von Windows Media Player ActiveX-Steuerelement
- einbetten, Remote-ActiveX-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615d3d31535abea098939af65ea67c13acbf8f6c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038681"
---
# <a name="remoting-the-windows-media-player-control"></a>Remoting des Windows Media Player-Steuerelements

Wenn Sie das Windows Media Player-Steuerelement in ein C++-Programm einbinden, können Sie es als Remote Erweiterung des vollständigen Modus des Players verwenden. Dies wird als "Remoting" der Windows Media Player-Steuerelement bezeichnet und ermöglicht es Ihnen, alle Features des vollmodusplayers bereitzustellen, ohne Sie selbst zu implementieren.

Wenn Sie das Steuerelement Remote ausführen, wird dieselbe Wiedergabe-Engine wie der vollständige Modus des Players freigegeben, und die Benutzer können zwischen dem eingebetteten Modus (dem "angedockten" Zustand) und dem vollständigen Modus (der Status "nicht angedockt") hin-und herwechseln, während die digitale Medienwiedergabe ununterbrochen fortgesetzt wird.

## <a name="enabling-remote-embedding"></a>Aktivieren der Remote Einbettung

Um die Remote Einbettung des Windows Media Player-Steuer Elements zu aktivieren, muss das Programm die **IServiceProvider** -und [iwmpremotemediaservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) -Schnittstellen implementieren. **IServiceProvider** ist eine Standard Component Object Model (com)-Schnittstelle mit einer einzelnen Methode namens **QueryService**. Windows Media Player ruft diese Methode auf, um einen Zeiger auf eine **iwmpremotemediaservices** -Schnittstelle abzurufen.

**Iwmpremotemediaservices** verfügt über mehrere Methoden, aber nur zwei davon sind für Remoting direkt relevant. In [getapplicationname](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname)geben Sie den Namen des Programms zurück, das von Windows Media Player der Liste **zu anderem Programm wechseln** im Menü **Ansicht** hinzugefügt wird. In [getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)geben Sie den Einbettungs Modus des Steuer Elements an, indem Sie den Wert "Remote" oder "local" zurückgeben. Wenn eine Remote Verbindung erfolgreich hergestellt wurde, gibt die [get \_ IsRemote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote) -Methode der [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4) -Schnittstelle true zurück.

## <a name="specifying-an-exclusive-online-store"></a>Angeben eines exklusiven Online Stores

Bei Windows Media Player 11 kann eine Anwendung, die das Player-Steuerelement Remote einbettet, einen exklusiven Online Store angeben. In diesem Fall ist die Dienst Auswahl in Windows Media Player deaktiviert, und nur der angegebene Onlinespeicher ist für den Benutzer verfügbar. Ausführliche Informationen zum Angeben eines exklusiven Online Speichers finden Sie unter [exklusive Online Stores](exclusive-online-stores.md).

## <a name="docking-and-undocking"></a>Andocken und Andocken

Die **IWMPPlayer4** -Schnittstelle bietet auch über die [get \_ playerapplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication) -Methode Zugriff auf die [iwmpplayerapplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication) -Schnittstelle. Verwenden Sie **iwmpplayerapplication** , um zwischen den angedockten und nicht angedockten Zuständen zu wechseln und den aktuellen angedockten Zustand und den Speicherort der Video-oder Visualisierungs Anzeige zu bestimmen.

Die [iwmpplayerapplication:: switchtoplayerapplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication) -Methode entdockt das Steuerelement, indem es den vollständigen Modus von Windows Media Player öffnet und die Video-oder Visualisierungs Anzeige an den Fensterbereich für die wieder **Gabe** überträgt. Die [iwmpplayerapplication:: switchtocontrol](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol) -Methode Dockt das Steuerelement an, indem Sie die Video-oder Visualisierungs Anzeige an das Programm übertragen und den vollständigen Modus des Players schließt, wenn er geöffnet ist. Das Steuerelement kann auch angedockt werden, indem Sie ein Programm aus der Liste **zu anderem Programm wechseln** oder den vollständigen Modus des Players schließen. In beiden Fällen wird jedes digitale Medium, das abgespielt wird, ununterbrochen fortgesetzt.

## <a name="transferring-the-video-or-visualization-display"></a>Übertragen der Video-oder Visualisierungs Anzeige

Wenn mehrere Programme mit eingebetteten, remoten Windows Media Player-Steuerelementen gleichzeitig ausgeführt werden, verwenden alle-Steuerelemente dieselbe Wiedergabe-Engine. Außerdem verwenden Sie die gleiche Instanz des vollständigen Modus des Players im nicht angedockten Zustand. Im angedockten Zustand kann jedoch nur ein Steuerelement das Video oder die Visualisierung anzeigen. Im nicht angedockten Zustand zeigt nur der vollständige Modus des Players das Video oder die Visualisierung an. Die **switchdecontrol** -Methode funktioniert sowohl in angedockten als auch in nicht angedockten Zuständen und überträgt die Video-oder Visualisierungs Anzeige an das Programm, das Sie aufruft.

Der einzige Unterschied zwischen angedockten und nicht angedockten Zuständen ist das vorhanden sein des vollständigen Modus von Windows Media Player und dessen Besitz der Video-oder Visualisierungs Anzeige. Im nicht angedockten Zustand sind alle eingebetteten, Remote Steuerelemente, die derzeit ausgeführt werden, weiterhin sichtbar, und Ihre Benutzeroberflächen sind weiterhin voll funktionsfähig. Wenn ein Video-oder Visualisierungs Fenster vorhanden ist, ist es jedoch leer. Im angedockten Zustand gehört nur eines der eingebetteten, Remote Steuerelemente der Anzeige, aber alle Benutzeroberflächen funktionieren weiterhin.

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>Ausblenden oder Ändern des Steuer Elements im nicht angedockten Zustand

Sie müssen ihre eigene Implementierung bereitstellen, wenn Sie die Benutzeroberfläche eines eingebetteten Steuer Elements im nicht angedockten Zustand ausblenden oder ändern möchten oder wenn das Programm die Anzeige nicht besitzt. Sie können diese Änderungen vornehmen, wenn Sie das Steuerelement andocken und abdocken, oder Sie können Sie als Reaktion auf Windows Media Player-Ereignisse festlegen. Da der Player über die Menüoption **zum Wechseln zum anderen Programm** angedockt werden kann, ist es in der Regel besser, diese Funktionalität als Reaktion auf Ereignisse bereitzustellen.

Sie können Ereignishandler für die Ereignisse [switchedtoplayerapplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) und [switchedtocontrol](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) implementieren, oder Sie können einen einzelnen Ereignishandler für das [playerdockedstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) -Ereignis implementieren. Im letzteren Fall können Sie den angedockten Zustand ermitteln, indem Sie [iwmpplayerapplication:: get \_ playerdocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked)aufrufen. Verwenden Sie in beiden Fällen [iwmpplayerapplication:: get \_ hasdisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) , um zu bestimmen, ob das Programm das Video oder die Visualisierungs Anzeige besitzt.

## <a name="re-establishing-a-remote-connection"></a>Erneutes Einrichten einer Remote Verbindung

Unter bestimmten Umständen können bei der Verbindung zwischen einem Remote-, eingebetteten und dem eigenständigen Player Fehler auftreten, wodurch die Zeiger auf die Windows-Media Player Schnittstellen ungültig werden. Windows Media Player versucht automatisch, erneut eine Verbindung herzustellen, und gibt das [playerreconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) -Ereignis aus, um diesen Versuch zu signalisieren. Obwohl die erneute Verbindung automatisch erfolgt, müssen Sie einen Ereignishandler für dieses Ereignis bereitstellen, wenn Sie die ungültigen Zeiger freigeben und neue abrufen möchten, damit Sie über die neue Verbindung auf den eigenständigen Player zugreifen können.

## <a name="controlling-the-undocked-player"></a>Steuern des nicht angedockten Players

Alle remoten Instanzen des Windows Media Player-Steuer Elements können den vollständigen Modus des Players unabhängig vom angedockten Zustand bearbeiten. Funktionen, die nicht für den vollständigen Modus des Players relevant sind, werden jedoch ignoriert, bis das Windows-Media Player Steuerelement angedockt ist. Dies schließt die Eigenschaften der [iwmpplayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) und der abgeleiteten Schnittstellen ein, z. b. **aktiviert**, **enablecontextmenu**, **uiMode** und **windowlessvideo**.

## <a name="error-dialog-boxes"></a>Fehler Dialogfelder

In einer remoten Windows Media Player-Steuerelement Instanz die *Einstellungen*. die **enableerrordialogs** -Eigenschaft verhält sich auf eine bestimmte Weise. Es gelten die folgenden Regeln:

-   Wenn Windows Media Player nicht angedockt ist (die Windows Media Player-Benutzeroberfläche ist sichtbar), wird die **enableerrordialogs** -Eigenschaft ignoriert, und Fehler Dialogfelder werden vom Player behandelt.
-   Wenn Windows Media Player angedockt ist, gilt der von jeder Remote Instanz des Steuer Elements für **enableerrordialogs** angegebene Wert nur für die einzelne Steuerelement Instanz. Das heißt, wenn eine bestimmte Steuerelement Instanz den Wert "true" für **enableerrordialogs** angibt, zeigt nur diese Instanz ein Dialogfeld an, wenn ein Fehler auftritt, wenn alle anderen Instanzen des Steuer Elements den Wert "false" angegeben haben.

## <a name="remoting-in-the-background"></a>Remoting im Hintergrund

Sie sollten vermeiden, dass eine Remote Instanz des Players im Hintergrund ausgeführt wird, wenn das Steuerelement nicht verwendet wird. Da die Remote Player-Steuerelement Instanz die Wiedergabe-Engine mit dem vollmodusplayer freigibt, kann das Beibehalten einer ausgeführten Instanz im Hintergrund zu unerwartetem Verhalten führen. Beispielsweise kann der Benutzer den vollmodusplayer schließen, während eine Datei wiedergegeben wird. Der Benutzer erwartet, dass die Dateiwiedergabe vollständig angehalten wird, wenn der Spieler geschlossen wird, aber die Audiowiedergabe kann weiterhin abgespielt werden, da die Wiedergabe-Engine noch aktiv ist.

## <a name="samples"></a>Beispiele

Das Windows Media Player SDK-Setup Paket installiert Beispiele, die das Remoting veranschaulichen. Weitere Informationen finden Sie in den Beispielen für remoteskin und wmpml.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




