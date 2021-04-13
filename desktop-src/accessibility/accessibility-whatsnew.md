---
description: Beschreibt die neuesten Neuerungen und Aktualisierungen der Features, Tools, Dokumentationen und Beispiele für Windows-Barrierefreiheit.
title: Neues in Windows-Barrierefreiheit für Entwickler
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 44d8c453b09bc73e71006e132199c18b275860af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483883"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>Neue Windows-Barrierefreiheits Features, Tools, Dokumentation und Beispiele für Entwickler

Die Windows-Plattform wird ständig mit neuen Barrierefreiheits-und Automatisierungs Features für Entwickler aktualisiert.

[Installieren Sie die Tools und das SDK](https://developer.microsoft.com/windows/downloads/#_blank) unter Windows 10, und Sie sind bereit, um entweder eine neue universelle Windows-APP zu erstellen oder zu erfahren, wie Sie Ihren vorhandenen app-Code unter Windows verwenden können.

Weitere Informationen zu den neuesten Tools, die zum Testen der Barrierefreiheits Implementierung Ihrer Windows-und Webanwendungen verfügbar sind, finden Sie unter [Testen auf Barrierefreiheit](accessibility-testwithuia.md).

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>Neuerungen beim Windows 10-Update vom Mai 2019 (Version 1903)

Die folgenden Features, Tools, Anleitungen für Entwickler, Beispiele und Videos wurden für das [Windows 10-Update von Mai 2019](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97)zur Verfügung gestellt.

| Release | Plattform | Funktion | BESCHREIBUNG | Link |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | Benutzeroberflächen Automatisierung unterstützt IAccessible2 | Benutzeroberflächenautomatisierungs-Clients können jetzt nahtlos auf Informationen von IAccessible2-Anbietern wie dem Chrome-Browser zugreifen. | – |
| 1903 | UWP | Sichtbarkeit der Scrollleiste  | Scrollleisten werden automatisch ausgeblendet, wenn Sie nicht mit interagiert werden. | [Uisettings. autohidescrollbars (Eigenschaft)](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | Benutzeroberflächen Automatisierung unterstützt strukturiertes Markup | Die MathML-Verarbeitung ist beabsichtigt, aber nicht eingeschränkt. | – |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>Neuerungen beim Windows 10-Update vom Oktober 2018 (Version 1809)

Die folgenden Features, Tools, Anleitungen für Entwickler, Beispiele und Videos wurden für das [Windows 10-Update vom Oktober 2018](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97)zur Verfügung gestellt.

| Release | Plattform | Funktion | BESCHREIBUNG | Link |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | Benutzeroberflächen Automatisierung unterstützt Änderungs Ereignisse für aktive Text Positionen | Benutzeroberflächenautomatisierungs-Anbieter können eine Anfangsposition innerhalb eines Text Bereichs explizit festlegen. Hilfstechnologieclients (at) können diese Position dann an einen Benutzer weiterleiten. Wenn ein Benutzer beispielsweise auf eine Verknüpfung mit einem Anker auf derselben Seite klickt (ein Lesezeichen Link), wird der neue Speicherort für die bereitgestellt. | [IUIAutomation6-Schnittstelle](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Benutzeroberflächen Automatisierung unterstützt das Zusammenfügen von Ereignissen | Verbessert die Leistung durch den Versuch, doppelte sequenzielle MSAA-und UIA-Text Änderungs Ereignisse zu erkennen, zu filtern und zu ignorieren, die von einigen Anbietern ausgelöst wurden | [IUIAutomation6-Schnittstelle](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Benutzeroberflächen Automatisierung unterstützt Verbindungs Wiederherstellungs Verhalten | Nachrichten von einem Benutzeroberflächenautomatisierungs-Client an einen Anbieter werden (standardmäßig zwei Sekunden) angehalten, wenn der Anbieter nicht reagiert. Dadurch wird die Häufigkeit erweiterter Timeouts reduziert und die Überflutung eines nicht reagierenden Anbieters mit Ereignissen und Anforderungen minimiert. | [IUIAutomation6-Schnittstelle](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | UWP | Erweiterte Bildschirm Lesedienste | Überprüfen Sie auf den Clients den hörbaren Bildschirm Lese Speicherort (Steuerung oder Inhalt) und den Lesemodus. | [Screenreaderservice-Klasse](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32, UWP | Benutzeroberflächen Automatisierung unterstützt Dialogfenster | Benutzeroberflächenautomatisierungs-Anbieter können UIA-Elemente speziell als Dialogfenster markieren. Häufig werden Dialogfelder für Benutzer unterschiedlich dargestellt.  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[Contentdialog-Klasse](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  UWP | Textskalierung  | Skaliert die Textgröße in Anwendungen und Webseiten. | [Uisettings. textscalefactor Changed-Ereignis](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[Textskalierung](/windows/uwp/design/input/text-scaling) |
