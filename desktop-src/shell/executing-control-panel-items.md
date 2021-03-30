---
description: Erläutert die Methoden zum Öffnen eines System Steuerungs Elements für Windows Vista und spätere Systeme sowie zum abdecken von Legacy-System Steuerungs Befehlen.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ausführen von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994934"
---
# <a name="executing-control-panel-items"></a>Ausführen von System Steuerungselementen

> [!Note]  
> Wenn Sie die Liste der kanonischen und Modulnamen für System Steuerungselemente suchen, finden Sie weitere Informationen unter [kanonische Namen von System Steuerungselementen](controlpanel-canonical-names.md).

 

Es gibt zwei Möglichkeiten zum Öffnen eines System Steuerungs Elements:

-   Der Benutzer kann die Systemsteuerung öffnen und dann ein Element öffnen, indem Sie auf das Element Symbol klicken oder doppelklicken.
-   Der Benutzer oder eine Anwendung kann ein System Steuerungselement starten, indem es direkt über die Eingabeaufforderung ausgeführt wird.

Eine Anwendung kann die Systemsteuerung Programm gesteuert mithilfe der [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec) -Funktion öffnen.


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



Im folgenden Beispiel wird gezeigt, wie eine Anwendung das System Steuerungselement mit dem Namen **MyCpl.cpl** mit der [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec) -Funktion starten kann.


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Wenn ein System Steuerungselement über eine Befehlszeile geöffnet wird, können Sie es anweisen, eine bestimmte Registerkarte im Element zu öffnen. Aufgrund des Hinzufügens und Entfernens bestimmter Registerkarten in einigen Windows Vista-System Steuerungselementen hat sich die Nummerierung der Registerkarten in Windows XP möglicherweise geändert. Im folgenden Beispiel wird z. b. die vierte Registerkarte im System Element unter Windows XP und die dritte Registerkarte unter Windows Vista gestartet.


```
control.exe sysdm.cpl,,3
```



In diesem Thema wird Folgendes erörtert:

-   [Kanonische Windows Vista-Namen](#windows-vista-canonical-names)
-   [Neue Befehle für Windows Vista](#new-commands-for-windows-vista)
-   [Ältere System Steuerungsbefehle](#legacy-control-panel-commands)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-vista-canonical-names"></a>Kanonische Windows Vista-Namen

In Windows Vista und höher ist die bevorzugte Methode zum Starten eines System Steuerungs Elements über eine Befehlszeile die Verwendung des kanonischen Namens des System Steuerungs Elements. Ein kanonischer Name ist eine nicht lokalisierte Zeichenfolge, die das System Steuerungselement in der Registrierung deklariert. Der Wert der Verwendung eines kanonischen Namens besteht darin, dass der Modulname des System Steuerungs Elements abstrahiert wird. Ein Element kann in einer DLL-Version implementiert und später als exe-Version neu implementiert werden oder dessen Modulname ändern. Solange der kanonische Name unverändert bleibt, muss jedes Programm, das es mithilfe dieses kanonischen Namens öffnet, nicht aktualisiert werden.

Gemäß der Konvention wird der kanonische Name als "corporationname. controlpanelitemname" formatiert.

Im folgenden Beispiel wird gezeigt, wie eine Anwendung das System Steuerungselement **Windows Update** mit [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec)starten kann.


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Wenn Sie ein System Steuerungselement mit dem kanonischen Namen starten möchten, verwenden Sie Folgendes: "% SystemRoot% \\ system32 \\control.exe/Name *CanonicalName*"

Verwenden Sie Folgendes, um eine bestimmte Unterseite in einem Element zu öffnen oder mit zusätzlichen Parametern zu öffnen: "% SystemRoot% \\ system32 \\control.exe/Name **CanonicalName** /Seite **pagename**"

Eine Anwendung kann auch die [**iopencontrolpanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) -Methode implementieren, um System Steuerungselemente zu starten, einschließlich der Fähigkeit, eine bestimmte Unterseite zu öffnen.

Eine komplette Liste der kanonischen Namen von System Steuerungselementen finden Sie unter [kanonische Namen von System Steuerungselementen](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Neue Befehle für Windows Vista

Unter Windows Vista sind einige Optionen, auf die von einem cpl-Modul unter Windows XP zugegriffen wurde, jetzt als exe-Dateien implementiert. Dies bietet zusätzliche Sicherheit, da Standardbenutzer aufgefordert werden, Administrator Anmelde Informationen anzugeben, wenn versucht wird, die Dateien zu starten. Optionen, die keine zusätzliche Sicherheit erfordern, werden über dieselben Befehlszeilen wie in Windows XP aufgerufen. Im folgenden finden Sie eine Liste der Befehle, die in Windows Vista verwendet werden, um auf bestimmte Registerkarten von System Steuerungselementen zuzugreifen:

### <a name="personalization"></a>Personalization

-   Schriftgröße und dpi:% windir% \\ system32 \\DpiScaling.exe
-   Bildschirmauflösung:% windir% \\ system32 \\control.exe desk.cpl, Einstellungen,@Settings
-   Anzeigeeinstellungen:% windir% \\ system32 \\control.exe desk.cpl, Einstellungen,@Settings
-   Themen:% windir% \\ system32 \\control.exe desk.cpl, Designs,@Themes
-   Bildschirmschoner:% windir% \\ system32 \\control.exe desk.cpl, Bildschirmschoner,@screensaver
-   Multimonitor:% windir% \\ system32 \\control.exe desk.cpl, Monitor,@Monitor
-   Farbschema:% windir% \\ system32 \\control.exe/Name Microsoft. Personalization/Seite pagefarbige zation
-   Desktop Hintergrund:% windir% \\ system32 \\control.exe/Name Microsoft. Personalization/Seite pgewallpaper

> [!Note]  
> Starter-und Basic-Editionen unterstützen nicht control.exe/Name Microsoft. Personalization-Befehl.

 

### <a name="system"></a>System

-   Leistung:% windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Remote Zugriff:% windir% \\ system32 \\SystemPropertiesRemote.exe
-   Computer Name:% windir% \\ system32 \\SystemPropertiesComputerName.exe
-   System Schutz:% windir% \\ system32 \\SystemPropertiesProtection.exe
-   Erweiterte Systemeigenschaften:% windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programme und Funktionen

-   Software hinzufügen oder entfernen:% windir% \\ system32 \\control.exe/Name Microsoft. Program Sand Features
-   Windows-Features:% windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Regions- und Sprachoptionen

-   Tastatur:% systemroot% \\ system32 \\control.exe/Name Microsoft. regionandlanguageoptions/Seite/p: "Keyboard"
-   Speicherort:% systemroot% \\ system32 \\control.exe/Name Microsoft. regionandlanguageoptions/Seite/p: "Location"
-   Verwaltung:% systemroot% \\ system32 \\control.exe/Name Microsoft. regionandlanguageoptions/Seite/p: "administrative"

### <a name="folder-options"></a>Ordneroptionen

-   Ordner Suche:% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundung 2
-   Dateizuordnungen:% windir% \\ system32 \\control.exe/Name Microsoft. defaultprograms/Seite pagefileassoc
-   Ansicht:% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundung 7
-   Allgemein:% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundung 0

### <a name="power-options"></a>Energieoptionen

-   Aktuelle Plan Einstellungen bearbeiten:% windir% \\ system32 \\control.exe/Name Microsoft. poweroptions/Seite pagePlanSettings
-   System Einstellungen:% windir% \\ system32 \\control.exe/Name Microsoft. poweroptions/Seite pageglobalsettings
-   Erstellen Sie einen Energie Sparplan:% windir% \\ system32 \\control.exe/Name Microsoft. poweroptions/Seite pagekreatenewplan
-   Es ist kein kanonischer Befehl für die Seite Erweiterte Einstellungen vorhanden. der Zugriff erfolgt auf ältere Weise:% windir% \\ system32 \\control.exe powercfg.cpl,, 3

## <a name="legacy-control-panel-commands"></a>Ältere System Steuerungsbefehle

Wenn Sie die [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec) -Funktion verwenden, kann das System spezielle System Steuerungsbefehle erkennen. Mit diesen Befehlen wird Windows Vista vorab angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe Desktop</td>
<td>Öffnet das Fenster <strong>Eigenschaften anzeigen</strong> .
<blockquote>
[!Note]<br />
Dieser Befehl wird von den Starter-und Basic-Editionen nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>control.exe Farbe</td>
<td>Öffnet das Fenster <strong>Anzeigeeigenschaften</strong> <strong>mit der vorab</strong> ausgewählten Registerkarte Darstellung.</td>
</tr>
<tr class="odd">
<td>control.exe Datum/-Uhrzeit</td>
<td>Öffnet das Fenster mit den <strong>Eigenschaften für Datum und Uhrzeit</strong> .</td>
</tr>
<tr class="even">
<td>control.exe International</td>
<td>Öffnet das Fenster Regions <strong>-und Sprachoptionen</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe Maus</td>
<td>Öffnet das Fenster mit den <strong>Maus Eigenschaften</strong> .</td>
</tr>
<tr class="even">
<td>control.exe Tastatur</td>
<td>Öffnet das Fenster <strong>Tastatur Eigenschaften</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe Drucker</td>
<td>Zeigt den Ordner <strong>Drucker und Faxe</strong> an.</td>
</tr>
<tr class="even">
<td>control.exe Schriftarten</td>
<td>Zeigt den Ordner " <strong>Fonts</strong> " an.</td>
</tr>
</tbody>
</table>



 

Für Windows 2000-Systeme und spätere Systeme:



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| control.exe Ordner        | Öffnet das Fenster **Ordneroptionen** .                  |
| control.exe NetWare        | Hiermit wird das **Novell NetWare** -Fenster (sofern installiert) gestartet.   |
| control.exe Telefonie      | Öffnet das Fenster " **Telefon-und Modem Optionen** ".         |
| control.exe admintools     | Zeigt den Ordner **Verwaltung** an.            |
| control.exe schedtasks     | Zeigt den Ordner " **geplante Aufgaben** " an.                 |
| control.exe netconnections | Zeigt den Ordner **Netzwerkverbindungen** an.             |
| control.exe Infrarot       | Hiermit wird das Fenster des **Infrarot Monitors** (sofern installiert) gestartet. |
| control.exe Benutzer Kennwörter  | Öffnet das Fenster **Benutzerkonten** .                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPlApplet](using-cplapplet.md)
</dt> <dt>

[Nachrichtenverarbeitung in der Systemsteuerung](message-processing.md)
</dt> <dt>

[Erweitern von System Steuerungselementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
