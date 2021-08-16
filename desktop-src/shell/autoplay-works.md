---
description: Das Erstellen einer AutoRun-fähigen Anwendung ist ein unkompliziertes Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, das diese Technologie implementiert hat), aber heute gibt es viele verschiedene Medientypen, die es verwenden können.
title: Erstellen einer AutoRun-Enabled-Anwendung
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
# <a name="creating-an-autorun-enabled-application"></a>Erstellen einer AutoRun-Enabled-Anwendung

Das Erstellen einer AutoRun-fähigen Anwendung ist ein unkompliziertes Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, das diese Technologie implementiert hat), aber heute gibt es viele verschiedene Medientypen, die es verwenden können.

Um AutoRun in Ihrer Anwendung zu aktivieren, fügen Sie einfach zwei wichtige Dateien ein:

-   Eine Autorun.inf-Datei
-   Eine Startanwendung

Wenn ein Benutzer einen Datenträger in ein CD-ROM-Laufwerk auf einem AutoRun-kompatiblen Computer einfügt, überprüft das System sofort, ob der Datenträger über ein Dateisystem für personalcomputer verfügt. In diesem Falle sucht das System nach einer Datei mit dem Namen [Autorun.inf](#creating-an-autoruninf-file). Diese Datei gibt eine Setupanwendung an, die zusammen mit einer Vielzahl optionaler Einstellungen ausgeführt wird. Die Startanwendung installiert, deinstalliert, konfiguriert und führt die Anwendung möglicherweise aus.

-   [Erstellen einer Autorun.inf-Datei](#creating-an-autoruninf-file)
-   [\[ \] Abschnitt "DeviceInstall"](#the-deviceinstall-section)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Erstellen einer Autorun.inf-Datei

Autorun.inf ist eine Textdatei im Stammverzeichnis der CD-ROM, die Ihre Anwendung enthält. Die primäre Funktion besteht darin, dem System den Namen und speicherort des Startprogramms der Anwendung bereitzustellen, das beim Einfügen des Datenträgers ausgeführt wird.

> [!Note]  
> Autorun.inf-Dateien werden unter Windows XP für Laufwerke, die DRIVE \_ REMOVABLE von [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea)zurückgeben, nicht unterstützt.

 

Die Datei Autorun.inf kann auch optionale Informationen enthalten, z.B.:

-   Der Name einer Datei, die ein Symbol enthält, das das CD-ROM-Laufwerk Ihrer Anwendung darstellt. Dieses Symbol wird von Windows Explorer anstelle des Standardlaufwerksymbols angezeigt.
-   Zusätzliche Befehle für das Kontextmenü, das angezeigt wird, wenn der Benutzer mit der rechten Maustaste auf das CD-ROM-Symbol klickt. Sie können auch den Standardbefehl angeben, der ausgeführt wird, wenn der Benutzer auf das Symbol doppelklickt.

Autorun.inf-Dateien ähneln .ini Dateien. Sie bestehen aus einem oder mehreren Abschnitten, die jeweils durch einen Namen in eckigen Klammern geführt werden. Jeder Abschnitt enthält eine Reihe von Befehlen, die von der Shell ausgeführt werden, wenn der Datenträger eingefügt wird. Es gibt zwei Abschnitte, die derzeit für Autorun.inf-Dateien definiert sind.

-   Der **\[ Abschnitt \] autorun** enthält die Standardbefehle für autoRun. Alle Autorun.inf-Dateien müssen über einen **\[ autorun-Abschnitt verfügen. \]**
-   Ein **\[ optionaler abschnitt \] autorun.alpha** kann für Systeme enthalten sein, die auf RISC-basierten Computern ausgeführt werden. Wenn ein Datenträger in ein CD-ROM-Laufwerk auf einem RISC-basierten System eingefügt wird, führt die Shell die Befehle in diesem Abschnitt anstelle der Befehle im **\[ Abschnitt autorun \]** aus.

> [!Note]  
> Die Shell prüft zunächst auf einen architekturspezifischen Abschnitt. Wenn keine gefunden wird, werden die Informationen im Abschnitt **\[ autorun \]** verwendet. Nachdem die Shell einen Abschnitt gefunden hat, ignoriert sie alle anderen, sodass jeder Abschnitt eigenständig sein muss.

 

Jeder Abschnitt enthält eine Reihe von Befehlen, die bestimmen, wie der Autorun-Vorgang erfolgt. Es sind fünf Befehle verfügbar.



| Befehl                         | Beschreibung                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [defaulticon](autorun-cmds.md) | Gibt das Standardsymbol für die Anwendung an.                                        |
| [Symbol](autorun-cmds.md)        | Gibt den Pfad und den Dateinamen eines anwendungsspezifischen Symbols für das CD-ROM-Laufwerk an. |
| [open](autorun-cmds.md)        | Gibt den Pfad und dateinamen der Startanwendung an.                           |
| [useautorun](autorun-cmds.md)  | Gibt an, dass V2-Features für die automatische Wiedergabe verwendet werden sollen, wenn sie unterstützt werden.                       |
| [Muschel](autorun-cmds.md)       | Definiert den Standardbefehl im Kontextmenü der CD-ROM.                             |
| [\_Shellverb](autorun-cmds.md) | Fügt befehle zum Kontextmenü der CD-ROM hinzu.                                           |



 

Im Folgenden wird ein Beispiel für eine einfache Datei Autorun.inf beschrieben. Sie gibt Filename.exe als Startanwendung an. Das zweite Symbol in Filename.exe stellt das CD-ROM-Laufwerk anstelle des Standardlaufwerksymbols dar.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Dieses Autorun.inf-Beispiel führt je nach Computertyp verschiedene Startanwendungen aus.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>\[ \] Abschnitt "DeviceInstall"

Sie können den Abschnitt **\[ DeviceInstall \]** auf beliebigen Wechselmedien verwenden. Sie wird nur unter Windows XP unterstützt. Sie verwenden **DriverPath,** um einen Verzeichnispfad anzugeben, in dem Windows XP nach Treiberdateien sucht, wodurch eine lange Suche durch den gesamten Inhalt verhindert wird.

Sie verwenden den Abschnitt **\[ DeviceInstall \]** mit einer Treiberinstallation, um Verzeichnisse anzugeben, in denen Windows XP die Medien nach Treiberdateien durchsuchen soll. Unter Windows XP werden ganze Medien standardmäßig nicht mehr durchsucht, sodass **\[ DeviceInstall \]** Suchstandorte angeben muss. Im Folgenden finden Sie die einzigen Wechselmedien, die Windows XP vollständig ohne **\[ \] deviceInstall-Abschnitt** in einer Autorun.inf-Datei durchsucht.

-   Disketten, die auf Laufwerken A oder B gefunden werden.
-   CD-/DVD-Medien mit einer Größe von weniger als 1 GIGABYTE (GB).

Alle anderen Medien müssen einen **\[ DeviceInstall-Abschnitt \]** für Windows XP enthalten, um auf diesem Medium gespeicherte Treiber zu erkennen.

> [!Note]  
> Wie beim Abschnitt **\[ AutoRun \]** kann der Abschnitt **\[ DeviceInstall \]** architekturspezifisch sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von Autoun-Startanwendungen](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Schreiben einer Geräteinstallationsanwendung](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
