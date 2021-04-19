---
title: Befehlszeilenparameter
description: Befehlszeilenparameter
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Windows-Media Player, Parameter
- Windows Media Player, Befehlszeilenparameter
- Windows Media Player, wmplayer
- Windows Media Player, WMPConfig
- Windows Media Player, wmpnscfg
- Befehlszeilenparameter
- Wmplayer
- WMPConfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa65b686f8a746111a62bd6afcc3df280191c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342294"
---
# <a name="command-line-parameters"></a>Befehlszeilenparameter

## <a name="command-line-parameters-for-wmplayer"></a>Befehlszeilenparameter für wmplayer

Windows Media Player unterstützt eine Reihe von Befehlszeilen Parametern, die angeben, wie sich der Player beim Start verhält. In der folgenden Tabelle werden die Parameter und deren Verhalten ausführlich erläutert.



| Syntax                                                                                                              | Verhalten                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*Pfad \\ Dateiname*" (Beispiel: `wmplayer "c:\filename.wma"` )<br/>                                            | Starten Sie den Player, und wiedergeben Sie die Datei.                                                                                                                                                                                                                                                                                                        |
| "*Pfad \\ Dateiname*"/fullscreen (Beispiel: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Geben Sie die angegebene Datei im Vollbildmodus wieder. Sie müssen den Pfad und den Dateinamen des wieder zugebende Inhalts angeben.<br/>                                                                                                                                                                                                                     |
| /Device: {DVD \| AudioCD} (Beispiel: `wmplayer /device:audio CD` )<br/>                                         | Abspielen einer DVD oder AudioCD.                                                                                                                                                                                                                                                                                                                    |
| "*Pfad \\ Dateiname*? WMPSkin =*Skin Name*"z. b.: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Öffnen Sie den Player, und wenden Sie die angegebene Skin an.                                                                                                                                                                                                                                                                                              |
| /Service:*keyName*                                                                                                  | Öffnen Sie den Player, der den durch *keyName* angegebenen Online Shop anzeigt. Erfordert Windows Media Player 10 oder höher.<br/>                                                                                                                                                                                                                      |
| > Task nowspielen                                                                                                    | Öffnen Sie den Player im Feature " **jetzt Wiedergabe** ".                                                                                                                                                                                                                                                                                            |
| > Task mediaguide                                                                                                    | Öffnen Sie den Player in der **Medien Leit Faden** Funktion (aktueller aktiver Online Store in Windows Media Player 10 oder höher).                                                                                                                                                                                                                          |
| > Task CDAudio                                                                                                       | Öffnen Sie den Player im Feature " **aus CD kopieren** " (**RIP** -Feature in Windows Media Player 10 oder Windows Media Player 11). Dieser Parameter wird in Windows Media Player 12 nicht unterstützt.                                                                                                                                                       |
| > Task cdwrite                                                                                                       | Öffnen Sie den Player im **Burn** -Feature. Erfordert Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| > Task medialibrary                                                                                                  | Öffnen Sie den Player in der **Bibliotheks** Funktion.                                                                                                                                                                                                                                                                                                |
| > Task Radiotuner                                                                                                    | Öffnen Sie den Player im Optionsfeld " **Radio Tuner** " (aktueller aktiver Online Store in Windows Media Player 10 oder höher).                                                                                                                                                                                                                          |
| > Task portabledevice                                                                                                | Öffnen Sie den Player im Feature "in **CD kopieren oder Gerät** " (**Synchronisierungs** Feature in Windows Media Player 10 oder höher).                                                                                                                                                                                                                            |
| > Task Services/Service Dienst *Name*                                                                               | Öffnen Sie den Player in der **Premium Services** -Funktion, und zeigen Sie den Dienst an, der durch den Dienst *Name* -Parameter angegeben wird. Dieser Wert ist der eindeutige Name für den Dienst. Wenn der angegebene Dienst nicht zuvor angezeigt wurde, wird der Service *Name* -Parameter ignoriert. (Öffnet den angegebenen Online Store in Windows Media Player 10 oder höher.) |
| > Task Servicetask *X*                                                                                                | Öffnen Sie den Player im Aufgabenbereich des Online Store-Dienstanbieter, der durch *X* angegeben wird Beispielsweise öffnet > Task ServiceTask1 den Player im Aufgabenbereich des ersten Online Store-Dienstanbieter.                                                                                                                                                                      |
| > Task skinviewer                                                                                                    | Öffnen Sie den Player in der **Skin Chooser** -Funktion.                                                                                                                                                                                                                                                                                           |
| /Playlist *Playlistname*                                                                                            | Öffnen Sie den Player, und wiedergeben Sie die angegebene Wiedergabeliste.                                                                                                                                                                                                                                                                                           |
| /Schema: {Music \| Pictures \| Video \| TV \| other} zum Beispiel: `wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Öffnen Sie den Player, der die angegebene Medienkategorie anzeigt. Erfordert Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Befehlszeilenparameter für WMPConfig

Wmpconfig.exe wird zum Ausführen bestimmter Befehle in Windows Media Player verwendet, die Administrator Berechtigungen erfordern. Beispiele hierfür sind das Starten und Beenden von Diensten zum Durchsuchen und Freigeben von Diensten sowie das Aktivieren von Ausnahmen in der Windows-Firewall. In der folgenden Tabelle werden die möglichen Werte für die Befehlszeilenparameter beschrieben.



| Syntax                                                                                    | Verhalten                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Disablehmedevice *Mac*                                                                    | Deaktiviert das Gerät, das durch einen Media Access Control (Mac)-Bezeichner angegeben wird.  |
| Hmeoff-Beispiel:<br/> WMPConfig hmeoff<br/>                                    | Deaktiviert den Windows Media Player-Netzwerkfreigabe Dienst.                 |
| Hmeon-Beispiel:<br/> WMPConfig-hmeon<br/>                                      | Ermöglicht die Freigabe, das Durchsuchen und die Firewallausnahme.                     |
| Removehmedevice- *Mac*                                                                     | Entfernt das durch einen Mac-Bezeichner angegebene Gerät.                          |
| Restorehmedevice *Mac*                                                                    | Stellt das durch einen Mac-Bezeichner angegebene Gerät wieder her.                         |
| Setdvdparameental- *Level*-Beispiel:<br/> WMPConfig setdvdparameentallevel 3<br/> | Legt die Steuerelement Ebene der DVD-Jugendfest. Die Ebene wird als ganze Zahl angegeben. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Befehlszeilenparameter für wmpnscfg

Microsoft Windows verwendet wmpnscfg.exe, um Benutzer zu benachrichtigen, wenn Medien renderinggeräte im Netzwerk gefunden werden. Wmpnscfg startet den Windows Media Player Network Sharing Service (NSS) und wartet dann auf Benachrichtigungen vom Dienst. Wenn wmpnscfg benachrichtigt wird, dass ein neues Medien Gerät im Netzwerk verfügbar ist, wird in der Taskleiste ein Popup Fenster angezeigt, in dem der Benutzer über die Verfügbarkeit des neuen Geräts informiert wird. Wenn der Benutzer auf das Popup klickt, wird in wmpnscfg Windows Media Player gestartet. Daraufhin wird ein Dialogfeld angezeigt, in dem der Benutzer aufgefordert wird, die Freigabe für das neue Gerät zuzulassen oder zu verweigern.

In der Regel ruft Windows wmpnscfg ohne Befehlszeilenparameter auf. Es ist jedoch ein Parameter verfügbar, der in der folgenden Tabelle beschrieben wird.



| Parameter | Verhalten                         |
|-----------|----------------------------------|
| /Close    | Schließen Sie alle Instanzen von wmpnscfg. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





