---
title: Barrierefreiheits Tools-AccEvent (Barrierefreiheits Ereignis-Watcher)
description: Mithilfe von AccEvent (barrierefreie Ereignisüberwachung) können Entwickler und Tester überprüfen, ob die Benutzeroberflächen Elemente der Anwendung bei Änderungen an der Benutzeroberfläche echte Microsoft UI Automation-und Microsoft Active Accessibility-Ereignisse hervorrufen.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e6fa4896c0cfe3155536537099b1c00af8ebe5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390729"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Barrierefreiheits Tools-AccEvent (Barrierefreiheits Ereignis-Watcher)

Mithilfe von **AccEvent (barrierefreie Ereignisüberwachung)** können Entwickler und Tester überprüfen, ob die Benutzeroberflächen Elemente der Anwendung bei Änderungen an der Benutzeroberfläche echte Microsoft UI Automation-und Microsoft Active Accessibility-Ereignisse hervorrufen. Änderungen an der Benutzeroberfläche können auftreten, wenn sich der Fokus ändert oder wenn ein Benutzeroberflächen Element aufgerufen, ausgewählt oder eine Status-oder Eigenschafts Änderung aufweist.

**AccEvent** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform*>" des SDK-Installations Pfads (Accevent.exe).

> [!NOTE]
> **AccEvent** ist ein Legacy Tool. Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.

## <a name="requirements"></a>Anforderungen

**AccEvent** kann verwendet werden, um Barrierefreiheits Daten auf Systemen zu untersuchen, die nicht über eine Benutzeroberflächen Automatisierung verfügen. Sie wurden ursprünglich für Microsoft Active Accessibility geschrieben. Zum Untersuchen der Benutzeroberflächen Automatisierung muss die Benutzeroberflächen Automatisierung auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" unter [UI Automation](entry-uiauto-win32.md).

" **AccEvent** " wird als Teil der Gesamtmenge der Tools in der Windows SDK installiert, nicht als separater exe-Download. Die Windows SDK umfasst alle Tools für die Barrierefreiheit, die in diesem Abschnitt dokumentiert sind. [Holen Sie sich den Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Download Archiv, das von dieser Seite verknüpft ist, wenn Sie eine vorherige Version benötigen.)

Um " **AccEvent**" auszuführen, suchen Sie nach AccEvent.exe im \\ Ordner "bin \\ < *Version* > \\ < *Platform*>", und führen Sie ihn aus (Sie müssen in der Regel nicht als Administrator ausgeführt werden).

## <a name="the-accessible-event-watcher-window"></a>Das Fenster "Barrierefreiheits Ereignis-Watcher"

Wenn Sie " **AccEvent**" starten, wird das Hauptfenster angezeigt. Das Hauptfenster **AccEvent** zeigt die Benutzeroberflächenautomatisierungs-oder Microsoft Active Accessibility-Ereignisse an, die von Anwendungen ausgelöst werden, die ausführen. Das Hauptfenster besteht aus den folgenden Hauptkomponenten:

- Titelleiste. Zeigt den aktuellen Betriebsmodus und den aktuellen Status an.
- Menüleiste. Bietet Zugriff auf die Funktionen von " **AccEvent** ".
- Datenansicht. Zeigt Informationen zu jedem Ereignis an, einschließlich der Ereignis-ID und der ausgewählten Eigenschaften des Benutzeroberflächen Elements, das das Ereignis ausgelöst hat.

**AccEvent** verfügt nur über eine grafische Benutzeroberfläche. Es gibt keine Befehlszeilenargumente für dieses Tool, Sie können jedoch andere Tools verwenden, um das Ausgabeprotokoll als Text zu verarbeiten.

Die folgende Abbildung zeigt das Hauptfenster " **AccEvent** ".

![die Benutzeroberfläche für das barrierefreie ereigniswatchertool](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Barrierefreie ereigniswatchertasks

Dieser Abschnitt enthält Informationen zu häufig verwendeten **AccEvent** -Aufgaben.

### <a name="configuring-the-operating-mode"></a>Konfigurieren des Betriebsmodus

Verwenden Sie das Menü **Modus** , um den Betriebsmodus **AccEvent** zu konfigurieren, und wählen Sie Einstellungen aus, mit denen das Verhalten des Tools gesteuert wird. Sie können die folgenden Optionen auswählen.



| Wenn diese Option ausgewählt ist | **AccEvent** führt dies aus                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Immer im Vordergrund                | Wird auf dem Bildschirm oberhalb einer anderen Benutzeroberfläche angezeigt.                                                                                                                                                                                    |
| UIA-Ereignisse                   | Zeigt Informationen zu Benutzeroberflächenautomatisierungs-Ereignissen an.                                                                                                                                                                                             |
| WinEvents (im Kontext)       | Zeigt Informationen zu Microsoft-Active Accessibility Ereignissen (WinEvents) an, die an Hook-Funktionen im Server Adressraum übermittelt werden. Weitere Informationen finden Sie unter [in-context-Hook-Funktionen](in-context-hook-functions.md).         |
| WinEvents (nicht im Kontext)   | Zeigt Informationen zu Microsoft-Active Accessibility Ereignissen (WinEvents) an, die an Hook-Funktionen im Client Adressraum übermittelt werden. Weitere Informationen finden Sie unter [Funktionen für den Out-of-Context-Hook](out-of-context-hook-functions.md). |
| Hervorhebungs Rechteck anzeigen     | Hebt ein Rechteck um das UI-Element hervor, das das ausgewählte Ereignis ausgelöst hat.                                                                                                                                                                 |
| Info Info anzeigen     | Zeigt Ereignis Informationen in einer QuickInfo an.                                                                                                                                                                                                        |
| Einstellungen                     | Zeigt das Dialogfeld **UIA-Ereignis Einstellungen** oder **WinEvent-Einstellungen** an.                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtern von Benutzeroberflächen-Automatisierungs Ereignissen

Klicken Sie zum Konfigurieren der Benutzeroberflächenautomatisierungs-Ereignisse und-Eigenschaften, die im Fenster **AccEvent** angezeigt werden, auf das Menü **Modus** , wählen Sie **UIA-Ereignisse** aus, und wählen Sie dann **Einstellungen** aus. Das Dialogfeld **UIA-Ereignis Einstellungen** wird angezeigt. Sie können dieses Dialogfeld auch verwenden, um nach Ereignissen zu filtern.

Das Dialogfeld " **UIA-Ereignis Einstellungen** " enthält die folgenden Bereiche:

- **Globale Ereignisse**

    Aktivieren Sie das Kontrollkästchen **focuschangedevent** , um Informationen zu globalen Ereignissen mit Fokus Änderungen anzuzeigen.

- **Ereignistyp**

    Wählen Sie die Ereignisse aus, die für Sie von Interesse sind.

- **Bereich**

    Wählen Sie das UI-Element aus, auf das von **AccEvent** für Ereignisse gelauscht werden soll.

- **Ereignisse einschließen aus**

    Wählen Sie **direkt** untergeordnete Elemente aus, wenn Sie Ereignisse von den unmittelbar untergeordneten Elementen des Benutzeroberflächen Elements sehen möchten, das im **Bereichs** Fenster ausgewählt wurde. Wenn Sie Ereignisse von allen untergeordneten Elementen anzeigen möchten, wählen Sie **alle** Nachfolger aus.

- **Berichtseigenschaften**

    Wählen Sie die Eigenschaften aus, die nach jedem Ereignis im Hauptfenster angezeigt werden sollen. Wenn **QuickInfo anzeigen** im Menü **Modus** ausgewählt ist, werden die ausgewählten Eigenschaften auch in einer QuickInfo angezeigt.

### <a name="filtering-active-accessibility-events"></a>Filtern von Active Accessibility Ereignissen

Klicken Sie zum Konfigurieren der Microsoft Active Accessibility-Ereignisse und-Eigenschaften, die im Fenster **AccEvent** angezeigt werden, auf das Menü **Modus** , wählen Sie entweder **WinEvents (im Kontext)** oder **WinEvents (nicht im Kontext) aus**, und wählen Sie dann **Einstellungen** aus. Das Dialogfeld **WinEvent-Einstellungen** wird angezeigt. Sie können dieses Dialogfeld auch verwenden, um nach Ereignissen zu filtern.

Das Dialogfeld **WinEvent-Einstellungen** enthält die folgenden Bereiche:

- **Objekte**

    Wählen Sie die Objekte aus, die von **AccEvent** für Ereignisse überwacht werden sollen. **AccEvent** kann Ereignisse überwachen, die von Windows, vom Cursor oder von der Einfügemarke stammen. Das **Fenster** ist standardmäßig ausgewählt.

- **Ereignisse**

    Wählen Sie die Ereignisse aus, die für Sie von Interesse sind. Alle Ereignisse werden standardmäßig angezeigt.

- **Ereignis Informationen**

    Wählen Sie die Informationen aus, die nach dem Namen der einzelnen Ereignisse im Hauptfenster angezeigt werden sollen.

- **Objekteigenschaften**

    Wählen Sie die Eigenschaften aus, die nach jedem Ereignis im Hauptfenster angezeigt werden sollen. Wenn **QuickInfo anzeigen** im Menü **Modus** ausgewählt ist, werden die ausgewählten Eigenschaften auch in einer QuickInfo angezeigt. **Name**, **Rolle** und **Status** sind standardmäßig ausgewählt.

- **Filterung**

    Wählen Sie im Filterabschnitt eine der Options Felder aus, um die Ereignisse zu filtern, die von den im Feld **HWNDs** angegebenen Fenstern ausgelöst werden. Standardmäßig ist das Optionsfeld **nicht filtern** ausgewählt.

    - Aktivieren Sie das Optionsfeld **ausschließen** , um nur die Ereignisse anzuzeigen, die von anderen Objekten als den angegebenen Fenstern ausgelöst wurden.
    - Aktivieren Sie das Optionsfeld **nur einschließen** , und geben Sie ein oder mehrere Fenster Handles an, um nur Ereignisse anzuzeigen, die von diesen Fenstern ausgelöst werden.
    - Aktivieren Sie das Kontrollkästchen **und** , um Ereignisse einzuschließen, die von den nachfolgenden Elementen des angegebenen Windows ausgelöst werden.

- **Optionen**

    Aktivieren Sie eine der folgenden Optionen:

    

    | Wenn diese Option ausgewählt ist                                  | **AccEvent** führt dies aus                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Aufruf verwenden                                                    | Verwendet [IDispatch:: Aufrufen](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) zum Abrufen von Objekteigenschaften anstelle der Verwendung von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden.                               |
    | Objekt immer erhalten (auch wenn keine Objekteigenschaften ausgewählt sind)     | Ruft das-Objekt ab, das dem-Ereignis zugeordnet ist, auch wenn im Bereich Objekteigenschaften keine Elemente ausgewählt sind.                                                                                        |
    | Standard Eigenschaft anzeigen (zusätzlich zu den ausgewählten Eigenschaften) | Zeigt die Standard Eigenschaft (sofern vorhanden) für das Objekt an, das dem Ereignis zugeordnet ist, zusammen mit den Elementen, die im Bereich "Objekteigenschaften" ausgewählt sind.                                                      |
    | Anzeigen von Ereignis Informationen von unsichtbar/ausgeblendeten Fenstern       | Zeigt die ausgewählten Elemente aus dem Bereich Ereignis Informationen für alle Objekte an, einschließlich der Elemente in unsichtbaren oder ausgeblendeten Fenstern.                                                                       |
    | Vollständige Ereignis Informationen von unsichtbar/verborgenen Fenstern anzeigen  | Zeigt die ausgewählten Elemente aus dem Bereich Ereignis Informationen und die ausgewählten (oder Standard-) Elemente aus dem Bereich Eigenschaften des Objekts für alle Objekte an, einschließlich derjenigen, die in nicht sichtbaren oder ausgeblendeten Fenstern angezeigt werden. |
    | Beim nächsten Ereignis unterbrechen                                      | Bewirkt, dass eine breakpointausnahme in dem Prozess auftritt, der das nächste WinEvent-Ereignis auslöst. Dies signalisiert dem Debugger, die Ausnahme zu behandeln.                                                        |

### <a name="using-the-event-menu"></a>Verwenden des Menüs "Ereignis"

Verwenden Sie das Menü **Ereignis** , um die folgenden Aufgaben auszuführen:

| Wenn diese Option ausgewählt ist | **AccEvent** führt dies aus                                    |
|------------------------------|-------------------------------------------------------|
| Lauschen starten              | Beginnt mit dem Anzeigen von Ereignis Informationen in der Datenansicht. |
| Lauschen nicht mehr               | Beendet das Anzeigen von Ereignis Informationen in der Datenansicht.  |
| Ereignis Verlauf löschen          | Löscht den Inhalt der Datenansicht.                 |
| Alle Ereignisse auswählen            | Wählt alle Ereignisse aus, die in der Datenansicht aufgeführt sind.           |
| Ausgewählte Ereignisse kopieren         | Kopiert die ausgewählten Ereignisse in die Zwischenablage.          |

### <a name="saving-active-accessibility-events"></a>Speichern von Active Accessibility Ereignissen

Öffnen Sie das Menü **Datei** , und wählen Sie **Protokollierung in Datei starten** aus, um das Speichern von Ereignissen in einer Textdatei zu beginnen. **AccEvent** beginnt mit dem Schreiben von Ereignissen in die angegebene Datei, bis Sie im Menü **Datei** die Option **Protokollierung abbrechen** auswählen. Die Textdatei kann für die Problembehandlung und das Überprüfen der Ereignisse zu einem späteren Zeitpunkt nützlich sein.

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [TestTools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)