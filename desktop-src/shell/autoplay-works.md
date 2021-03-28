---
description: Das Erstellen einer Autorun-fähigen Anwendung ist ein einfaches Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, um diese Technologie zu implementieren), aber heute gibt es viele verschiedene Medientypen, von denen es verwendet werden kann.
title: Erstellen einer AutoRun-Enabled Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128468"
---
# <a name="creating-an-autorun-enabled-application"></a>Erstellen einer AutoRun-Enabled Anwendung

Das Erstellen einer Autorun-fähigen Anwendung ist ein einfaches Verfahren. In diesem Thema wird CD-ROM als Beispiel verwendet (es war das erste Medium, um diese Technologie zu implementieren), aber heute gibt es viele verschiedene Medientypen, von denen es verwendet werden kann.

Um Autorun in Ihrer Anwendung zu aktivieren, schließen Sie einfach zwei wesentliche Dateien ein:

-   Eine Autorun. inf-Datei
-   Eine Start Anwendung

Wenn ein Benutzer eine CD in ein CD-ROM-Laufwerk auf einem automatisch nicht kompatiblen Computer einfügt, prüft das System sofort, ob die Festplatte über ein persönliches Computerdatei System verfügt. Wenn dies der Fall ist, sucht das System nach einer Datei namens " [Autorun. inf](#creating-an-autoruninf-file)". Diese Datei gibt eine Setup Anwendung an, die ausgeführt wird, sowie eine Reihe optionaler Einstellungen. Die Start Anwendung installiert, deinstalliert, konfiguriert und führt die Anwendung möglicherweise aus.

-   [Erstellen einer Autorun. inf-Datei](#creating-an-autoruninf-file)
-   [Der \[ Abschnitt "de viceingestall" \]](#the-deviceinstall-section)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Erstellen einer Autorun. inf-Datei

Autorun. inf ist eine Textdatei im Stammverzeichnis der CD-ROM, die Ihre Anwendung enthält. Die primäre Funktion besteht darin, dem System den Namen und den Speicherort des Start Programms der Anwendung zur Verfügung zu stellen, das beim Einfügen der Festplatte ausgeführt wird.

> [!Note]  
> Autorun. inf-Dateien werden unter Windows XP nicht für Laufwerke unterstützt, die das Laufwerk \_ von [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea)zurücksetzen.

 

Die Datei Autorun. inf kann auch optionale Informationen enthalten, einschließlich:

-   Der Name einer Datei, die ein Symbol enthält, das das CD-ROM-Laufwerk der Anwendung darstellt. Dieses Symbol wird von Windows-Explorer anstelle des Standard Laufwerks Symbols angezeigt.
-   Zusätzliche Befehle für das Kontextmenü, das angezeigt wird, wenn der Benutzer mit der rechten Maustaste auf das CD-ROM-Symbol klickt. Sie können auch den Standardbefehl angeben, der ausgeführt wird, wenn der Benutzer auf das Symbol doppelklickt.

Autorun. inf-Dateien ähneln den INI-Dateien. Sie bestehen aus mindestens einem Abschnitt, wobei jeder mit einem Namen in eckigen Klammern steht. Jeder Abschnitt enthält eine Reihe von Befehlen, die von der Shell ausgeführt werden, wenn die Festplatte eingefügt wird. Es gibt zwei Abschnitte, die derzeit für Autorun. inf-Dateien definiert sind.

-   Der **\[ Auto ausführen \]** -Abschnitt enthält die Standard Befehle Auto ausführen. Alle Auto ausführen. inf-Dateien müssen über einen **\[ Auto ausführen- \]** Abschnitt verfügen.
-   Ein optionaler Abschnitt " **\[ Autorun. alpha \]** " kann für Systeme eingeschlossen werden, die auf RISC-basierten Computern ausgeführt werden. Wenn ein CD-ROM-Laufwerk auf einem RISC-basierten System in ein CD-ROM-Laufwerk eingefügt wird, führt die Shell die Befehle in diesem Abschnitt anstelle der im Abschnitt **\[ Auto ausführen \]** .

> [!Note]  
> Die Shell prüft zuerst nach einem architekturspezifischen Abschnitt. Wenn eine solche nicht gefunden wird, werden die Informationen im Abschnitt **\[ Auto ausführen \]** verwendet. Nachdem die Shell einen Abschnitt gefunden hat, ignoriert Sie alle anderen, sodass jeder Abschnitt in sich selbst enthalten sein muss.

 

Jeder Abschnitt enthält eine Reihe von Befehlen, die bestimmen, wie der Autorun-Vorgang stattfindet. Es stehen fünf Befehle zur Verfügung.



| Befehl                         | BESCHREIBUNG                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [DefaultIcon](autorun-cmds.md) | Gibt das Standard Symbol für die Anwendung an.                                        |
| [angezeigt](autorun-cmds.md)        | Gibt den Pfad und den Dateinamen eines anwendungsspezifischen Symbols für das CD-ROM-Laufwerk an. |
| [open](autorun-cmds.md)        | Gibt den Pfad und den Dateinamen der Start Anwendung an.                           |
| [useautorun](autorun-cmds.md)  | Gibt an, dass AutoPlay v2-Features verwendet werden sollen, wenn unterstützt.                       |
| [schel](autorun-cmds.md)       | Definiert den Standardbefehl im Kontextmenü der CD-ROM.                             |
| [\_shellverb](autorun-cmds.md) | Fügt Befehle zum Kontextmenü der CD-ROM hinzu.                                           |



 

Im folgenden finden Sie ein Beispiel für eine einfache INF-Datei. Gibt Filename.exe als Start Anwendung an. Das zweite Symbol in Filename.exe stellt das CD-ROM-Laufwerk anstelle des Standard-Laufwerk Symbols dar.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



In diesem Autorun. inf-Beispiel werden je nach Computertyp verschiedene Start Anwendungen ausgeführt.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>Der \[ Abschnitt "de viceingestall" \]

Sie können den Abschnitt " **\[ de vicabstall \]** " auf allen Wechselmedien verwenden. Sie wird nur unter Windows XP unterstützt. Mit **DriverPath** geben Sie einen Verzeichnispfad an, in dem Windows XP nach Treiberdateien sucht, was eine lange Suche durch den gesamten Inhalt verhindert.

Verwenden Sie den Abschnitt **\[ deviceinstall \]** mit einer Treiberinstallation, um Verzeichnisse anzugeben, in denen Windows XP die Medien nach Treiberdateien durchsuchen soll. Unter Windows XP werden die gesamten Medien nicht mehr standardmäßig durchsucht, daher muss **\[ devicinstall \]** zum Angeben von Such Standorten erforderlich sein. Folgendes ist das einzige Wechselmedium, das in Windows XP vollständig ohne einen **\[ deviceinstall \]** -Abschnitt in der Datei "Autorun. inf" durchsucht wird.

-   Disketten in den Laufwerken A oder B.
-   CD/DVD-Medien weniger als 1 Gigabyte (GB).

Alle anderen Medien müssen einen **\[ deviceinstall \]** -Abschnitt für Windows XP enthalten, um Treiber zu ermitteln, die auf diesem Medium gespeichert sind.

> [!Note]  
> Wie beim **\[ Autorun \]** -Abschnitt kann der Abschnitt " **\[ de viceinstall \]** " architekturspezifisch sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von Autorun-Start Anwendungen](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Schreiben einer Geräte Installationsanwendung](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
