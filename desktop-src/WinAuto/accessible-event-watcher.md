---
title: Barrierefreiheitstools – AccEvent (Accessible Event Watcher)
description: Mit AccEvent (Accessible Event Watcher) können Entwickler und Tester überprüfen, ob die Benutzeroberflächenelemente einer Anwendung bei Änderungen der Benutzeroberfläche die richtigen Microsoft Benutzeroberflächenautomatisierung auslösen und Ereignisse Microsoft Active Accessibility.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2192bf6973444bf2bfc307ff4613d9d1c593d5a22f9800ecb61bc310b3a210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327802"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Barrierefreiheitstools – AccEvent (Accessible Event Watcher)

**Mit AccEvent (Accessible Event Watcher)** können Entwickler und Tester überprüfen, ob die Benutzeroberflächenelemente einer Anwendung ordnungsgemäße Microsoft Benutzeroberflächenautomatisierung auslösen und Ereignisse Microsoft Active Accessibility, wenn Benutzeroberflächenänderungen auftreten. Änderungen an der Benutzeroberfläche können auftreten, wenn sich der Fokus ändert oder wenn ein Benutzeroberflächenelement aufgerufen, ausgewählt oder ein Zustand oder eine Eigenschaft geändert wird.

**AccEvent** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner bin \\ < *version* > \\ < *platform*> des SDK-Installationspfads (Accevent.exe).

> [!NOTE]
> **AccEvent** ist ein Legacytool. Es wird empfohlen, stattdessen [Barrierefreiheit Insights](https://accessibilityinsights.io/) zu verwenden.

## <a name="requirements"></a>Anforderungen

**AccEvent** kann verwendet werden, um Barrierefreiheitsdaten auf Systemen ohne Benutzeroberflächenautomatisierung zu untersuchen, die ursprünglich für Microsoft Active Accessibility geschrieben wurden. Um Benutzeroberflächenautomatisierung zu untersuchen, müssen Benutzeroberflächenautomatisierung auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md).

**AccEvent** wird als Teil der gesamten Tools im Windows SDK installiert und nicht als separater Exe-Download verteilt. Das Windows SDK enthält alle tools im Zusammenhang mit der Barrierefreiheit, die in diesem Abschnitt dokumentiert sind. [Abrufen des Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Downloadarchiv, das von dieser Seite verknüpft ist, wenn Sie eine frühere Version benötigen.)

Suchen Sie zum Ausführen von **AccEvent** AccEvent.exe auf der \\ Bin-Versionsplattform> Ordner , und führen Sie ihn aus (in der \\ <  > \\ <  Regel müssen Sie nicht als Administrator ausführen).

## <a name="the-accessible-event-watcher-window"></a>Das Fenster "Accessible Event Watcher"

Wenn Sie **AccEvent** starten, wird das Hauptfenster angezeigt. Im **AccEvent-Hauptfenster** werden die Benutzeroberflächenautomatisierung oder Microsoft Active Accessibility Ereignisse angezeigt, die von ausgeführten Anwendungen ausgelöst werden. Das Hauptfenster enthält die folgenden Hauptteile:

- Titelleiste. Zeigt den aktuellen Betriebsmodus und -status an.
- Menüleiste. Bietet Zugriff auf **die AccEvent-Funktionalität.**
- Datenansicht Zeigt Informationen zu jedem Ereignis an, einschließlich der Ereignis-ID und der ausgewählten Eigenschaften des Benutzeroberflächenelements, das das Ereignis ausgelöst hat.

**AccEvent** verfügt nur über eine grafische Benutzeroberfläche. Es gibt keine Befehlszeilenargumente für dieses Tool, aber Sie können andere Tools verwenden, um das Ausgabeprotokoll als Text zu verarbeiten.

Die folgende Abbildung  zeigt das AccEvent-Hauptfenster.

![Die Benutzeroberfläche für das barrierefreie Event Watcher-Tool](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Barrierefreie Event Watcher-Aufgaben

Dieser Abschnitt enthält Informationen zu häufig verwendeten **AccEvent-Aufgaben.**

### <a name="configuring-the-operating-mode"></a>Konfigurieren des Betriebsmodus

Sie verwenden das Menü **Modus,** um den **AccEvent-Betriebsmodus** zu konfigurieren und Einstellungen auszuwählen, die das Verhalten des Tools steuern. Sie können die folgenden Optionen auswählen.



| Wenn diese Option ausgewählt ist | **AccEvent** führt dies aus.                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Always on Top                | Wird über einer beliebigen anderen Benutzeroberfläche auf dem Bildschirm angezeigt.                                                                                                                                                                                    |
| UIA-Ereignisse                   | Zeigt Informationen zu Benutzeroberflächenautomatisierung Ereignissen an.                                                                                                                                                                                             |
| WinEvents (im Kontext)       | Zeigt Informationen zu Microsoft Active Accessibility Ereignissen (WinEvents) an, die an Hookfunktionen übergeben werden, die sich im Serveradressraum befinden. Weitere Informationen finden Sie unter [In-Context Hook Functions](in-context-hook-functions.md).         |
| WinEvents (außerhalb des Kontexts)   | Zeigt Informationen zu Microsoft Active Accessibility Ereignissen (WinEvents) an, die an Hookfunktionen übergeben werden, die sich im Clientadressraum befinden. Weitere Informationen finden Sie unter [Out-of-Context Hook Functions](out-of-context-hook-functions.md). |
| Hervorhebungsrechteck anzeigen     | Hebt ein Rechteck um das Benutzeroberflächenelement hervor, das das ausgewählte Ereignis ausgelöst hat.                                                                                                                                                                 |
| QuickInfo "Informationen anzeigen"     | Zeigt Ereignisinformationen in einer QuickInfo an.                                                                                                                                                                                                        |
| Einstellung                     | Zeigt das Dialogfeld **UIA Event Einstellungen** oder **WinEvent Einstellungen** an.                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtern von Benutzeroberflächenautomatisierung Ereignissen

Klicken Sie zum Konfigurieren der Benutzeroberflächenautomatisierung Ereignisse und Eigenschaften, die im **AccEvent-Fenster** angezeigt werden, auf das Menü **Modus,** wählen Sie **UIA-Ereignisse** und dann **Einstellungen** aus. Das Dialogfeld **UIA Event Einstellungen** wird angezeigt. Sie können dieses Dialogfeld auch verwenden, um nach Ereignissen zu filtern.

Das Dialogfeld **UIA-Ereignis Einstellungen** enthält die folgenden Bereiche:

- **Globale Ereignisse**

    Aktivieren Sie das **Kontrollkästchen FocusChangedEvent,** um Informationen zu globalen Ereignissen mit Fokusänderung anzuzeigen.

- **Ereignistyp**

    Wählen Sie die Ereignisse aus, an denen Sie interessiert sind.

- **Bereich**

    Wählen Sie das Benutzeroberflächenelement aus, auf das **AccEvent** auf Ereignisse lauschen soll.

- **Einschließen von Ereignissen aus**

    Wählen Sie **Direkt untergeordnete** Elemente aus, wenn Sie Ereignisse aus den unmittelbar untergeordneten Elementen des benutzeroberflächenelements anzeigen möchten, das im **Bereich Bereich** ausgewählt ist. Wenn Sie Ereignisse aus allen Nachfolgerelementen anzeigen möchten, wählen Sie **Alle Nachfolger aus.**

- **Berichtseigenschaften**

    Wählen Sie die Eigenschaften aus, die nach jedem Ereignis im Hauptfenster angezeigt werden sollen. Wenn Im Menü **Modus** die **Option Informations-QuickInfo anzeigen** ausgewählt ist, werden die ausgewählten Eigenschaften auch in einer QuickInfo angezeigt.

### <a name="filtering-active-accessibility-events"></a>Filtern von Active Accessibility Ereignissen

Klicken Sie zum Konfigurieren der Microsoft Active Accessibility Ereignisse und Eigenschaften, die im **AccEvent-Fenster** angezeigt werden, auf das Menü **Modus,** wählen Sie entweder **WinEvents (im Kontext)** oder **WinEvents (Außerhalb des Kontexts)** aus, und wählen Sie dann **Einstellungen** aus. Das Dialogfeld **WinEvent Einstellungen** wird angezeigt. Sie können dieses Dialogfeld auch verwenden, um nach Ereignissen zu filtern.

Das Dialogfeld **WinEvent Einstellungen** enthält die folgenden Bereiche:

- **Objekte**

    Wählen Sie die Objekte aus, auf die **AccEvent** auf Ereignisse lauschen soll. **AccEvent** kann auf Ereignisse lauschen, die von Fenstern, dem Cursor oder dem Caretereignis stammen. **Das Fenster** ist standardmäßig ausgewählt.

- **Ereignisse**

    Wählen Sie die Ereignisse aus, an denen Sie interessiert sind. Alle Ereignisse werden standardmäßig angezeigt.

- **Ereignisinformationen**

    Wählen Sie die Informationen aus, die nach dem Namen jedes Ereignisses im Hauptfenster angezeigt werden sollen.

- **Objekteigenschaften**

    Wählen Sie die Eigenschaften aus, die nach jedem Ereignis im Hauptfenster angezeigt werden sollen. Wenn Im Menü **Modus** die **Option Informations-QuickInfo anzeigen** ausgewählt ist, werden die ausgewählten Eigenschaften auch in einer QuickInfo angezeigt. **Name,** **Rolle** und **Status** sind standardmäßig ausgewählt.

- **Filterung**

    Wählen Sie eines der Optionsfelder im Filterabschnitt aus, um die Ereignisse zu filtern, die von den im Feld **hWNDs** angegebenen Fenstern ausgelöst werden. Das Optionsfeld **Nicht filtern** ist standardmäßig aktiviert.

    - Wählen Sie das Optionsfeld **Ausschließen** aus, um nur die Ereignisse anzuzeigen, die von anderen Objekten als den angegebenen Fenstern ausgelöst wurden.
    - Wählen Sie das Optionsfeld **Nur einschließen** aus, und geben Sie ein oder mehrere Fensterhandles an, um nur Ereignisse anzuzeigen, die von diesen Fenstern ausgelöst werden.
    - Aktivieren Sie das Kontrollkästchen **und Descendants,** um Ereignisse einzuschließt, die von den Nachfolgern der angegebenen Fenster ausgelöst werden.

- **Optionen**

    Aktivieren Sie eine der folgenden Optionen:

    

    | Wenn diese Option ausgewählt ist                                  | **AccEvent** führt dies aus.                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Verwenden von Invoke                                                    | Verwendet [IDispatch::Invoke,](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) um Objekteigenschaften abzurufen, anstatt [**IAccessible-Methoden zu**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verwenden.                               |
    | Immer Objekt abrufen (auch wenn keine Objekteigenschaften ausgewählt sind)     | Ruft das dem Ereignis zugeordnete Objekt ab, auch wenn im Bereich Objekteigenschaften keine Elemente ausgewählt sind.                                                                                        |
    | Anzeigen der Standardeigenschaft (zusätzlich zu ausgewählten Eigenschaften) | Zeigt ggf. die Standardeigenschaft für das dem Ereignis zugeordnete Objekt sowie die im Bereich Objekteigenschaften ausgewählten Elemente an.                                                      |
    | Anzeigen von Ereignisinformationen aus unsichtbaren/ausgeblendeten Fenstern       | Zeigt die ausgewählten Elemente im Bereich Ereignisinformationen für alle Objekte an, einschließlich der Elemente in unsichtbaren oder ausgeblendeten Fenstern.                                                                       |
    | Anzeigen vollständiger Ereignisinformationen aus unsichtbaren/ausgeblendeten Fenstern  | Zeigt die ausgewählten Elemente aus dem Bereich Ereignisinformationen und die ausgewählten (oder Standard)-Elemente aus dem Bereich Objekteigenschaften für alle Objekte an, einschließlich der Elemente in unsichtbaren oder ausgeblendeten Fenstern. |
    | Debugbreak beim nächsten Ereignis                                      | Bewirkt, dass eine Breakpointausnahme in dem Prozess auftritt, der das nächste WinEvent verursacht. Dies signalisiert dem Debugger, die Ausnahme zu behandeln.                                                        |

### <a name="using-the-event-menu"></a>Verwenden des Ereignismenüs

Verwenden Sie das Menü **Ereignis,** um die folgenden Aufgaben auszuführen:

| Wenn diese Option ausgewählt ist | **AccEvent** führt dies aus.                                    |
|------------------------------|-------------------------------------------------------|
| Starten der Überwachung              | Beginnt mit der Anzeige von Ereignisinformationen in der Datenansicht. |
| Beenden der Überwachung               | Beendet die Anzeige von Ereignisinformationen in der Datenansicht.  |
| Löschen des Ereignisverlaufs          | Löscht den Inhalt der Datenansicht.                 |
| Wählen Sie Alle Ereignisse aus.            | Wählt alle in der Datenansicht aufgeführten Ereignisse aus.           |
| Kopieren ausgewählter Ereignisse         | Kopiert die ausgewählten Ereignisse in die Zwischenablage.          |

### <a name="saving-active-accessibility-events"></a>Speichern von Active Accessibility Ereignissen

Um mit dem Speichern von Ereignissen in einer Textdatei zu beginnen, öffnen Sie das Menü **Datei,** und wählen **Sie Protokollierung in Datei starten** aus. **AccEvent** beginnt mit dem Schreiben von Ereignissen in die angegebene Datei, bis Sie im Menü **Datei** die Option **Protokollierung beenden** auswählen. Die Textdatei kann für die Problembehandlung und Überprüfung der Ereignisse zu einem späteren Zeitpunkt nützlich sein.

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [Testtools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)