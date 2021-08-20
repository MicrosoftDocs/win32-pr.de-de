---
description: Erläutert Methoden zum Öffnen eines Systemsteuerung Elements für Windows Vista- und höhere Systeme sowie das Abdecken von Legacybefehlen Systemsteuerung.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ausführen von Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb941bb7542b0d786d682e6626e8d78faea8bd7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478416"
---
# <a name="executing-control-panel-items"></a>Ausführen von Systemsteuerung Elementen

> [!Note]  
> Wenn Sie nach der Liste der kanonischen und Modulnamen für Systemsteuerung Elemente suchen, finden Sie weitere Informationen unter [Kanonische Namen von Systemsteuerung Items](controlpanel-canonical-names.md).

 

Es gibt zwei Möglichkeiten, ein Systemsteuerung Element zu öffnen:

-   Der Benutzer kann Systemsteuerung öffnen und dann ein Element öffnen, indem er auf das Symbol des Elements klickt oder doppelklickt.
-   Der Benutzer oder eine Anwendung kann ein Systemsteuerung Element starten, indem er es direkt über die Eingabeaufforderung ausführt.

Eine Anwendung kann die Systemsteuerung programmgesteuert mithilfe der [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) öffnen.


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



Das folgende Beispiel zeigt, wie eine Anwendung das Systemsteuerung Element namens **MyCpl.cpl** mithilfe der [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) starten kann.


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Wenn ein Systemsteuerung Element über eine Befehlszeile geöffnet wird, können Sie es anweisen, eine bestimmte Registerkarte im Element zu öffnen. Aufgrund des Hinzufügens und Entfernens bestimmter Registerkarten in einigen Windows Vista-Systemsteuerung-Elementen hat sich die Nummerierung der Registerkarten möglicherweise von der Nummerierung in Windows XP geändert. Im folgenden Beispiel wird beispielsweise die vierte Registerkarte im Element System auf Windows XP und die dritte Registerkarte auf Windows Vista gestartet.


```
control.exe sysdm.cpl,,3
```



In diesem Thema wird Folgendes erörtert:

-   [Windows Kanonische Vista-Namen](#windows-vista-canonical-names)
-   [Neue Befehle für Windows Vista](#new-commands-for-windows-vista)
-   [Legacybefehle für Systemsteuerung](#legacy-control-panel-commands)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Kanonische Vista-Namen

In Windows Vista und höher besteht die bevorzugte Methode zum Starten eines Systemsteuerung Elements über eine Befehlszeile darin, den kanonischen Namen des Systemsteuerung Elements zu verwenden. Ein kanonischer Name ist eine nicht lokalisierte Zeichenfolge, die vom Systemsteuerung Element in der Registrierung deklariert wird. Der Wert der Verwendung eines kanonischen Namens ist, dass der Modulname des Systemsteuerung Elements abstrahiert wird. Ein Element kann in einem .dll implementiert und später als .exe erneut implementiert oder sein Modulname geändert werden. Solange der kanonische Name gleich bleibt, muss jedes Programm, das ihn mit diesem kanonischen Namen öffnet, nicht aktualisiert werden.

Gemäß der Konvention wird der kanonische Name als "CorporationName.ControlPanelItemName" gebildet.

Das folgende Beispiel zeigt, wie eine Anwendung das Systemsteuerung Element **Windows Update** mit [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)starten kann.


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Verwenden Sie "%systemroot% \\ system32control.exe \\ /name *canonicalName",* um ein Systemsteuerung Element mit seinem kanonischen Namen zu starten.

Verwenden Sie "%systemroot% \\ system32control.exe \\ /name **canonicalName** /page **pageName",** um eine bestimmte Unterseite in einem Element zu öffnen oder sie mit zusätzlichen Parametern zu öffnen.

Eine Anwendung kann auch die [**IOpenControlPanel::Open-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) implementieren, um Systemsteuerung Elemente zu starten, einschließlich der Möglichkeit, eine bestimmte Unterseite zu öffnen.

Eine vollständige Liste der kanonischen Namen Systemsteuerung Elements finden Sie unter [Kanonische Namen von Systemsteuerung Items](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Neue Befehle für Windows Vista

Auf Windows Vista werden einige Optionen, auf die von einem .cpl-Modul auf Windows XP zugegriffen wurde, jetzt als .exe-Dateien implementiert. Dies bietet zusätzliche Sicherheit, da Standardbenutzer beim Versuch, die Dateien zu starten, aufgefordert werden, Administratoranmeldeinformationen anzugeben. Auf Optionen, die keine zusätzliche Sicherheit erfordern, wird über die gleichen Befehlszeilen zugegriffen, die in Windows XP verwendet wurden. Es folgt eine Liste der Befehle, die in Windows Vista verwendet werden, um auf bestimmte Registerkarten von Systemsteuerung Elementen zuzugreifen:

### <a name="personalization"></a>Personalisierung

-   Schriftgrad und DPI: %windir% \\ system32 \\DpiScaling.exe
-   Bildschirmauflösung: %windir% \\ system32 \\control.exe desk.cpl,Einstellungen,@Settings
-   Anzeigeeinstellungen: %windir% \\ system32 \\control.exe desk.cpl,Einstellungen,@Settings
-   Designs: %windir% \\ system32 \\control.exe desk.cpl,Themes,@Themes
-   Bildschirmschoner: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver
-   Multimonitor: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor
-   Farbschema: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization
-   Desktophintergrund: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper

> [!Note]  
> Starter- und Basic-Editionen unterstützen control.exe Befehl /name Microsoft.Personalization nicht.

 

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

-   Ordnersuche: %windir% \\ system32 \\rundll32.exe shell32.dll,Optionen \_ RunDLL 2
-   Dateizuordnungen: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pagefileAssoc
-   Ansicht: %windir% \\ system32 \\rundll32.exe shell32.dll,Optionen \_ RunDLL 7
-   Allgemein: %windir% \\ system32 \\rundll32.exe shell32.dll,Optionen \_ RunDLL 0

### <a name="power-options"></a>Energieoptionen

-   Aktuelle Planeinstellungen bearbeiten: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pagePlanSettings
-   Systemeinstellungen: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings
-   Erstellen eines Energiesparplans: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageCreateNewPlan
-   Es gibt keinen kanonischen Befehl für die Seite Advanced Einstellungen, auf die in der älteren Weise zugegriffen wird: %windir% \\ system32 \\control.exe powercfg.cpl,,3

## <a name="legacy-control-panel-commands"></a>Legacybefehle für Systemsteuerung

Wenn Sie die [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) verwenden, kann das System spezielle Systemsteuerung Befehle erkennen. Diese Befehle stellen Windows Vista voraus.




| | | control.exe Desktop-| Startet das <strong>fenster Anzeigeeigenschaften.</strong><blockquote>[!Note]<br />Starter- und Basic-Editionen unterstützen diesen Befehl nicht.</blockquote><br /> | | control.exe Farb-| Startet das <strong>fenster Anzeigeeigenschaften,</strong> in dem die Registerkarte <strong>Darstellung</strong> vorab ausgewählt ist. | | control.exe Datums-/Uhrzeit-| Öffnet das Fenster <strong>Datums- und Uhrzeiteigenschaften.</strong> | | control.exe internationale | Öffnet das Fenster <strong>Regions- und Sprachoptionen.</strong> | | control.exe Maus-| Öffnet das Fenster <strong>Mauseigenschaften.</strong> | | control.exe Tastatur-| Öffnet das Fenster <strong>Tastatureigenschaften.</strong> | | control.exe Drucker | Zeigt den Ordner <strong>Drucker und Faxe an.</strong> | | control.exe schriftarten | Zeigt den Ordner <strong>Schriftarten an.</strong> | 




 

Für Windows Systeme ab 2000:



| Befehl                    | BESCHREIBUNG                                              |
|----------------------------|----------------------------------------------------------|
| control.exe Ordner        | Öffnet das Fenster **Ordneroptionen.**                  |
| control.exe Netware        | Startet das **NetWare-Fenster (sofern** installiert).   |
| control.exe Telefonie      | Öffnet das Fenster **Telefon und Modemoptionen.**         |
| control.exe admintools     | Zeigt den Ordner **Verwaltung an.**            |
| control.exe schedtasks     | Zeigt den Ordner **Geplante Aufgaben** an.                 |
| control.exe netconnections | Zeigt den Ordner **Netzwerkverbindungen an.**             |
| control.execontrol.exe       | Startet das Fenster **Überwachungsmonitor** (sofern installiert). |
| control.exe userpasswords  | Öffnet das Fenster **Benutzerkonten.**                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Items](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[Registrieren Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Systemsteuerung Nachrichtenverarbeitung](message-processing.md)
</dt> <dt>

[Erweitern von Systemsteuerung Elementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
