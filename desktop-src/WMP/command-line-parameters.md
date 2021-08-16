---
title: Befehlszeilenparameter
description: Befehlszeilenparameter
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Windows Media Player, Parameter
- Windows Media Player, Befehlszeilenparameter
- Windows Media Player,Wmplayer
- Windows Media Player,Wmpconfig
- Windows Media Player,Wmpnscfg
- Befehlszeilenparameter
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240040453bc60a7a03ca56f205643f97202eb840a501fd13aa417b86aef060d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341950"
---
# <a name="command-line-parameters"></a>Befehlszeilenparameter

## <a name="command-line-parameters-for-wmplayer"></a>Befehlszeilenparameter für Wmplayer

Windows Media Player unterstützt eine Reihe von Befehlszeilenparametern, die angeben, wie sich der Player beim Start verhält. In der folgenden Tabelle werden die Parameter und deren Verhalten ausführlich beschrieben.



| Syntax                                                                                                              | Verhalten                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*\\ Pfaddateiname*"(Beispiel: `wmplayer "c:\filename.wma"` )<br/>                                            | Starten Sie den Player, und wiedergeben Sie die Datei.                                                                                                                                                                                                                                                                                                        |
| "*\\ pfaddateiname*" /fullscreen(Beispiel: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Wiedergeben der angegebenen Datei im Vollbildmodus. Sie müssen den Pfad und den Dateinamen des inhalts angeben, der wiedergegeben werden soll.<br/>                                                                                                                                                                                                                     |
| /Device:{DVD \| AudioCD}(Beispiel: `wmplayer /device:audio CD` )<br/>                                         | Wiedergeben einer DVD oder Audio-CD                                                                                                                                                                                                                                                                                                                    |
| "*\\ Pfaddateiname*? WMPSkin=*Skinname*"Beispiel: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Öffnen Sie den Player, und wenden Sie die angegebene Skin an.                                                                                                                                                                                                                                                                                              |
| /Service:*keyname*                                                                                                  | Öffnen Sie den Player, in dem der durch *den Schlüsselnamen* angegebene Onlineshop angezeigt wird. Erfordert Windows Media Player 10 oder höher.<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | Öffnen Sie den Player im Feature **Jetzt wiedergeben.**                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | Öffnen Sie den Player im **Media Guide-Feature** (aktuell aktiver Onlineshop in Windows Media Player 10 oder höher).                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | Öffnen Sie den Player im Feature **"Aus CD kopieren"** (10 oder Windows Media Player Windows Media Player 11). Dieser Parameter wird in Windows Media Player 12 nicht unterstützt.                                                                                                                                                       |
| /Task CDWrite                                                                                                       | Öffnen Sie den Player im **Feature "Burn".** Erfordert Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | Öffnen Sie den  Player in der Bibliotheksfunktion.                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | Öffnen Sie den Player im **Radio Tuner-Feature** (aktuell aktiver Onlineshop in Windows Media Player 10 oder höher).                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | Öffnen Sie den Player im Feature **Auf CD oder Gerät kopieren** (**Synchronisierungsfeature** in Windows Media Player 10 oder höher).                                                                                                                                                                                                                            |
| /Task Services /Service *servicename*                                                                               | Öffnen Sie den Player im **Feature Premium Services,** und zeigen Sie den *dienstnamensspezifischen* Dienst an. Dieser Wert ist der eindeutige Name für den Dienst. Wenn der angegebene Dienst zuvor nicht angezeigt wurde, wird der *servicename-Parameter* ignoriert. (Öffnet den angegebenen Onlineshop in Windows Media Player 10 oder höher.) |
| /Task ServiceTask *X*                                                                                                | Öffnen Sie den Player im Aufgabenbereich des Onlineshopdiensts, der durch *X* angegeben wird. Beispielsweise öffnet /Task ServiceTask1 den Player im ersten Aufgabenbereich des Onlineshopdiensts.                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | Öffnen Sie den Player in der **Funktion "Skin Chooser".**                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | Öffnen Sie den Player, und wiedergeben Sie die angegebene Wiedergabeliste.                                                                                                                                                                                                                                                                                           |
| /Schema:{Musik \| Pictures \| Video TV \| \| Other}Beispiel:`wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Öffnen Sie den Player mit der angegebenen Medienkategorie. Erfordert Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Befehlszeilenparameter für Wmpconfig

Wmpconfig.exe wird verwendet, um bestimmte Befehle in Windows Media Player auszuführen, die Administratorberechtigungen erfordern. Beispiele hierfür sind das Starten und Beenden von Browser- und Freigabediensten sowie das Aktivieren von Ausnahmen in der Windows Firewall. In der folgenden Tabelle werden die möglichen Werte für die Befehlszeilenparameter beschrieben.



| Syntax                                                                                    | Verhalten                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *MAC*                                                                    | Deaktiviert das gerät, das durch einen MAC-Bezeichner (Media Access Control) angegeben wird.  |
| HMEOff-Beispiel:<br/> wmpconfig HMEOff<br/>                                    | Deaktiviert den Windows Media Player-Netzwerkfreigabedienst.                 |
| HMEOn-Beispiel:<br/> wmpconfig HMEOn<br/>                                      | Ermöglicht die Freigabe, das Durchsuchen und die Firewallausnahme.                     |
| RemoveHMEDevice *MAC*                                                                     | Entfernt das durch einen MAC-Bezeichner angegebene Gerät.                          |
| RestoreHMEDevice *MAC*                                                                    | Stellt das durch einen MAC-Bezeichner angegebene Gerät wieder her.                         |
| SetDVDParentalLevel-Ebene Beispiel: <br/> wmpconfig SetDVDParentalLevel 3<br/> | Legt die Dvd-Jugendschutzebene fest. Die Ebene wird als ganze Zahl angegeben. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Befehlszeilenparameter für Wmpnscfg

Microsoft Windows verwendet wmpnscfg.exe, um Benutzer zu warnen, wenn Medienrenderinggeräte im Netzwerk gefunden werden. Wmpnscfg startet den Windows Media Player Network Sharing Service (NSS) und wartet dann auf Benachrichtigungen vom Dienst. Wenn wmpnscfg benachrichtigt wird, dass ein neues Mediengerät im Netzwerk verfügbar ist, wird in der Taskleiste ein Popup angezeigt, das den Benutzer über die Verfügbarkeit des neuen Geräts informiert. Wenn der Benutzer auf das Popup klickt, startet wmpnscfg Windows Media Player, in dem ein Dialogfeld angezeigt wird, in dem der Benutzer aufgefordert wird, die Freigabe für das neue Gerät zuzulassen oder zu verweigern.

In der Regel ruft Windows wmpnscfg ohne Befehlszeilenparameter auf. Es ist jedoch ein Parameter verfügbar, der in der folgenden Tabelle beschrieben wird.



| Parameter | Verhalten                         |
|-----------|----------------------------------|
| /Close    | Schließen Sie alle Instanzen von wmpnscfg. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





