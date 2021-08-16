---
description: Erläutert Methoden zum Öffnen eines Systemsteuerung-Elements für Windows Vista- und höher-Systeme sowie zur Behandlung von Legacy-Systemsteuerung Befehlen.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ausführen Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e2bc84ce5225176585f2da221fab6110ce79f9ff68dfc83b3c66125d623d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224276"
---
# <a name="executing-control-panel-items"></a>Ausführen Systemsteuerung Elementen

> [!Note]  
> Wenn Sie nach der Liste der kanonischen und Modulnamen für Systemsteuerung suchen, finden Sie weitere Informationen unter [Kanonische Namen von](controlpanel-canonical-names.md)Systemsteuerung Elementen.

 

Es gibt zwei Möglichkeiten zum Öffnen eines Systemsteuerung Elements:

-   Der Benutzer kann Systemsteuerung und dann ein Element öffnen, indem er auf das Symbol des Elements klickt oder doppelklickt.
-   Der Benutzer oder eine Anwendung kann ein Systemsteuerung starten, indem es direkt über die Eingabeaufforderung ausgeführt wird.

Eine Anwendung kann die Systemsteuerung programmgesteuert mithilfe der [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) öffnen.


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



Das folgende Beispiel zeigt, wie eine Anwendung das Systemsteuerung element **namensMyCpl.cpl** mithilfe der [**WinExec-Funktion starten**](/windows/win32/api/winbase/nf-winbase-winexec) kann.


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Wenn ein Systemsteuerung über eine Befehlszeile geöffnet wird, können Sie es anweisen, eine bestimmte Registerkarte im Element zu öffnen. Aufgrund des Hinzu- und Entfernens bestimmter Registerkarten in einigen Windows Vista Systemsteuerung-Elementen hat sich die Nummerierung der Registerkarten möglicherweise von der Nummerierung in Windows XP geändert. Im folgenden Beispiel wird beispielsweise die vierte Registerkarte im Element System auf Windows XP und die dritte Registerkarte auf Windows Vista gestartet.


```
control.exe sysdm.cpl,,3
```



In diesem Thema wird Folgendes erörtert:

-   [Windows Kanonische Vista-Namen](#windows-vista-canonical-names)
-   [Neue Befehle für Windows Vista](#new-commands-for-windows-vista)
-   [Legacy-Systemsteuerung Befehle](#legacy-control-panel-commands)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Kanonische Vista-Namen

In Windows Vista und höher ist die bevorzugte Methode zum Starten eines Systemsteuerung-Elements über eine Befehlszeile die Verwendung des kanonischen Namens des Systemsteuerung Elements. Ein kanonischer Name ist eine nicht lokalisierte Zeichenfolge, die vom Systemsteuerung in der Registrierung deklariert wird. Der Wert der Verwendung eines kanonischen Namens ist, dass er den Modulnamen des Systemsteuerung abstrahiert. Ein Element kann in einer -.dll und später erneut als ein Element implementiert .exe oder seinen Modulnamen ändern. Solange der kanonische Name unverändert bleibt, muss jedes Programm, das ihn mit diesem kanonischen Namen öffnet, nicht aktualisiert werden.

Standardmäßig wird der kanonische Name als "CorporationName.ControlPanelItemName" gebildet.

Das folgende Beispiel zeigt, wie eine Anwendung das Systemsteuerung-Element Windows **Update** mit [**WinExec starten kann.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Um ein Systemsteuerung-Element mit seinem kanonischen Namen zu starten, verwenden Sie: "%systemroot% \\ system32 \\control.exe /name *canonicalName*"

Verwenden Sie zum Öffnen einer bestimmten Unterseite in einem Element oder zum Öffnen mit zusätzlichen Parametern: "%systemroot% \\ system32 \\control.exe /name **canonicalName** /page **pageName**"

Eine Anwendung kann auch die [**IOpenControlPanel::Open-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) implementieren, um Systemsteuerung zu starten, einschließlich der Möglichkeit, eine bestimmte Unterseite zu öffnen.

Eine vollständige Liste der kanonischen Systemsteuerung-Elementnamen finden Sie unter [Kanonische Namen von](controlpanel-canonical-names.md)Systemsteuerung Elementen.

## <a name="new-commands-for-windows-vista"></a>Neue Befehle für Windows Vista

Unter Windows Vista werden einige Optionen, auf die von einem .cpl-Modul auf Windows XP zugegriffen wurde, jetzt als .exe implementiert. Dies bietet zusätzliche Sicherheit, da Standardbenutzer beim Versuch, die Dateien zu starten, zur Eingabe von Administratoranmeldeinformationen aufgefordert werden können. Auf Optionen, die keine zusätzliche Sicherheit erfordern, wird über dieselben Befehlszeilen zugegriffen, die in xp Windows wurden. Im Folgenden finden Sie eine Liste von Befehlen, die in Windows Vista verwendet werden, um auf bestimmte Registerkarten von Systemsteuerung zugreifen:

### <a name="personalization"></a>Personalization

-   Schriftgrad und DPI: %windir% \\ system32 \\DpiScaling.exe
-   Bildschirmauflösung: %windir% \\ system32 \\control.exe desk.cpl,Einstellungen,@Settings
-   Anzeigeeinstellungen: %windir% \\ system32 \\control.exe desk.cpl,Einstellungen,@Settings
-   Designs: %windir% \\ system32 \\control.exe desk.cpl,Themes,@Themes
-   Bildschirmschoner: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver
-   Mehrere Monitore: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor
-   Farbschema: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization
-   Desktophintergrund: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper

> [!Note]  
> Starter- und Basic-Editionen unterstützen den Befehl control.exe /name Microsoft.Personalization nicht.

 

### <a name="system"></a>System

-   Leistung: %windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Remotezugriff: %windir% \\ system32 \\SystemPropertiesRemote.exe
-   Computername: %windir% \\ system32 \\SystemPropertiesComputerName.exe
-   Systemschutz: %windir% \\ system32 \\SystemPropertiesProtection.exe
-   Erweiterte Systemeigenschaften: %windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programme und Features

-   Hinzufügen oder Entfernen von Programmen: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures
-   Windows Features: %windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Regions- und Sprachoptionen

-   Tastatur: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"
-   Speicherort: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"
-   Administrator: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"

### <a name="folder-options"></a>Ordneroptionen

-   Ordnersuche: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 2
-   Dateizuordnungen: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc
-   Ansicht: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 7
-   Allgemein: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 0

### <a name="power-options"></a>Energieoptionen

-   Aktuelle Planeinstellungen bearbeiten: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings
-   Systemeinstellungen: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings
-   Erstellen eines Energieplans: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan
-   Es gibt keinen kanonischen Befehl für die Seite "Advanced Einstellungen". Der Zugriff erfolgt auf ältere Weise: %windir% \\ system32 \\control.exe powercfg.cpl,,3

## <a name="legacy-control-panel-commands"></a>Legacy-Systemsteuerung Befehle

Wenn Sie die [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) verwenden, kann das System spezielle Systemsteuerung erkennen. Diese Befehle sind vor Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe Desktop</td>
<td>Startet das <strong>Anzeigeeigenschaften</strong> Fenster.
<blockquote>
[!Note]<br />
Die Editionen Starter und Basic unterstützen diesen Befehl nicht.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>control.exe Farbe</td>
<td>Startet das fenster <strong>Anzeigeeigenschaften,</strong> in dem die <strong>Registerkarte Darstellung</strong> vorab ausgewählt ist.</td>
</tr>
<tr class="odd">
<td>control.exe Datum/Uhrzeit</td>
<td>Öffnet das Fenster <strong>Datums- und Uhrzeiteigenschaften.</strong></td>
</tr>
<tr class="even">
<td>control.exe international</td>
<td>Öffnet das Fenster <strong>"Regionale Optionen" und "Sprachoptionen".</strong></td>
</tr>
<tr class="odd">
<td>control.exe Maus</td>
<td>Öffnet das Fenster <strong>Mauseigenschaften.</strong></td>
</tr>
<tr class="even">
<td>control.exe Tastatur</td>
<td>Öffnet das Fenster <strong>Tastatureigenschaften.</strong></td>
</tr>
<tr class="odd">
<td>control.exe Drucker</td>
<td>Zeigt den Ordner <strong>Drucker und Faxe</strong> an.</td>
</tr>
<tr class="even">
<td>control.exe Schriftarten</td>
<td>Zeigt den Ordner <strong>Schriftarten</strong> an.</td>
</tr>
</tbody>
</table>



 

Für Windows 2000- und höher-Systeme:



| Befehl                    | Beschreibung                                              |
|----------------------------|----------------------------------------------------------|
| control.exe Ordner        | Öffnet das Fenster **Ordneroptionen.**                  |
| control.exe netware        | Startet (sofern installiert) das **Fenster "Schließen von NetWare".**   |
| control.exe Telefonie      | Öffnet das Fenster **Telefon und Modemoptionen.**         |
| control.exe admintools     | Zeigt den **Ordner Verwaltung an.**            |
| control.exe schedtasks     | Zeigt den Ordner **Geplante Aufgaben** an.                 |
| control.exe netconnections | Zeigt den Ordner **Netzwerkverbindungen an.**             |
| control.exe       | Startet das Fenster **Überwachungsmonitor** (sofern installiert). |
| control.exe userpasswords  | Öffnet das Fenster **Benutzerkonten.**                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Items](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[Registrieren von Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Systemsteuerung der Nachrichtenverarbeitung](message-processing.md)
</dt> <dt>

[Erweitern von System Systemsteuerung Elementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für ein Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
