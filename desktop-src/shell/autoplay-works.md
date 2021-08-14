---
description: Das Erstellen einer AutoRun-fähigen Anwendung ist ein einfaches Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, das diese Technologie implementiert hat), aber heute gibt es viele verschiedene Medientypen, die sie verwenden können.
title: Erstellen einer AutoRun-Enabled Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f3a3c265f71b0bdf66d7825e65eb69ab975bfc6bffa5c9a8674ed5a0fb8feb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224932"
---
# <a name="creating-an-autorun-enabled-application"></a>Erstellen einer AutoRun-Enabled Anwendung

Das Erstellen einer AutoRun-fähigen Anwendung ist ein einfaches Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, das diese Technologie implementiert hat), aber heute gibt es viele verschiedene Medientypen, die sie verwenden können.

Um AutoRun in Ihrer Anwendung zu aktivieren, fügen Sie einfach zwei wichtige Dateien ein:

-   Eine Autorun.inf-Datei
-   Eine Startanwendung

Wenn ein Benutzer einen Datenträger in ein CD-ROM-Laufwerk auf einem Computer mit AutoRun-Kompatibilität einfügung, überprüft das System sofort, ob der Datenträger über ein Dateisystem für den pc-Computer verfügt. In diesem Beispiel sucht das System nach einer Datei mit dem Namen [Autorun.inf.](#creating-an-autoruninf-file) Diese Datei gibt eine Setupanwendung an, die zusammen mit einer Vielzahl optionaler Einstellungen ausgeführt wird. Die Startanwendung installiert, deinstalliert, konfiguriert und führt die Anwendung möglicherweise aus.

-   [Erstellen einer Autorun.inf-Datei](#creating-an-autoruninf-file)
-   [Abschnitt \[ \] "DeviceInstall"](#the-deviceinstall-section)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Erstellen einer Autorun.inf-Datei

Autorun.inf ist eine Textdatei, die sich im Stammverzeichnis der CD-ROM befindet, die Ihre Anwendung enthält. Die primäre Funktion besteht in der Bereitstellung des Namens und speicherorts des Startprogramms der Anwendung, das beim Einfügen des Datenträgers ausgeführt wird.

> [!Note]  
> Autorun.inf-Dateien werden unter Windows XP für Laufwerke, die DRIVE \_ REMOVABLE von [**GetDriveType zurückgeben, nicht unterstützt.**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea)

 

Die Datei Autorun.inf kann auch optionale Informationen enthalten, einschließlich:

-   Der Name einer Datei, die ein Symbol enthält, das das CD-ROM-Laufwerk Ihrer Anwendung darstellen soll. Dieses Symbol wird von Windows Explorer statt des Standardlaufwerksymbols angezeigt.
-   Zusätzliche Befehle für das Kontextmenü, das angezeigt wird, wenn der Benutzer mit der rechten Maustaste auf das CD-ROM-Symbol klickt. Sie können auch den Standardbefehl angeben, der ausgeführt wird, wenn der Benutzer auf das Symbol doppelklickt.

Autorun.inf-Dateien ähneln .ini Dateien. Sie bestehen aus einem oder mehreren Abschnitten, die jeweils von einem In eckigen Klammern umschlossenen Namen geleitet werden. Jeder Abschnitt enthält eine Reihe von Befehlen, die von der Shell ausgeführt werden, wenn der Datenträger eingefügt wird. Es gibt zwei Abschnitte, die derzeit für Autorun.inf-Dateien definiert sind.

-   Der **\[ Abschnitt \] autorun** enthält die Standardmäßigen AutoRun-Befehle. Alle Autorun.inf-Dateien müssen über einen **\[ Autorun-Abschnitt \]** verfügen.
-   Ein **\[ optionaler Abschnitt \] autorun.alpha** kann für Systeme enthalten sein, die auf RISC-basierten Computern ausgeführt werden. Wenn ein Datenträger auf einem RISC-basierten System in ein CD-ROM-Laufwerk eingefügt wird, werden die Befehle in diesem Abschnitt von der Shell anstelle der Befehle im Abschnitt **\[ autorun \]** ausgeführt.

> [!Note]  
> Die Shell überprüft zuerst einen architekturspezifischen Abschnitt. Wenn sie keine findet, werden die Informationen im Abschnitt **\[ autorun \]** verwendet. Nachdem die Shell einen Abschnitt gefunden hat, ignoriert sie alle anderen, sodass jeder Abschnitt in sich geschlossen sein muss.

 

Jeder Abschnitt enthält eine Reihe von Befehlen, die bestimmen, wie der Autorun-Vorgang ausgeführt wird. Es sind fünf Befehle verfügbar.



| Befehl                         | BESCHREIBUNG                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [defaulticon](autorun-cmds.md) | Gibt das Standardsymbol für die Anwendung an.                                        |
| [Symbol](autorun-cmds.md)        | Gibt den Pfad und dateinamen eines anwendungsspezifischen Symbols für das CD-ROM-Laufwerk an. |
| [open](autorun-cmds.md)        | Gibt den Pfad und dateinamen der Startanwendung an.                           |
| [useautorun](autorun-cmds.md)  | Gibt an, dass V2-Features für die automatische Wiedergabe verwendet werden sollen, wenn dies unterstützt wird.                       |
| [Muschel](autorun-cmds.md)       | Definiert den Standardbefehl im Kontextmenü der CD-ROM.                             |
| [\_Shellverb](autorun-cmds.md) | Fügt dem Kontextmenü der CD-ROM Befehle hinzu.                                           |



 

Im Folgenden finden Sie ein Beispiel für eine einfache Datei Autorun.inf. Sie gibt Filename.exe als Startanwendung an. Das zweite Symbol in Filename.exe das CD-ROM-Laufwerk anstelle des Standardlaufwerksymbols.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



In diesem Autorun.inf-Beispiel werden je nach Computertyp verschiedene Startanwendungen ausgeführt.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>Abschnitt \[ \] "DeviceInstall"

Sie können den Abschnitt **\[ DeviceInstall \]** auf allen Wechselmedien verwenden. Dies wird nur unter xp Windows unterstützt. Sie verwenden **DriverPath,** um einen Verzeichnispfad anzugeben, in dem Windows XP nach Treiberdateien sucht, wodurch eine langwierige Suche durch den gesamten Inhalt verhindert wird.

Sie verwenden den **\[ Abschnitt DeviceInstall \]** mit einer Treiberinstallation, um Verzeichnisse anzugeben, in denen Windows XP die Medien nach Treiberdateien durchsuchen soll. Unter Windows XP werden standardmäßig nicht mehr alle Medien durchsucht, daher muss **\[ DeviceInstall \]** Suchspeicherorte angeben. Im Folgenden finden Sie die einzigen Wechselmedien, die Windows XP vollständig ohne **\[ \] deviceInstall-Abschnitt** in einer Autorun.inf-Datei durchsucht.

-   Diskettendatenträger auf Laufwerken A oder B.
-   CD/DVD-Medien mit einer Größe von weniger als 1 Gigabyte (GB).

Alle anderen Medien müssen einen **\[ \] DeviceInstall-Abschnitt** für Windows XP enthalten, um auf diesem Medium gespeicherte Treiber zu erkennen.

> [!Note]  
> Wie im **\[ Abschnitt \] AutoRun kann** der **\[ Abschnitt DeviceInstall \]** architekturspezifisch sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren automatischer Startanwendungen](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Schreiben einer Geräteinstallationsanwendung](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
