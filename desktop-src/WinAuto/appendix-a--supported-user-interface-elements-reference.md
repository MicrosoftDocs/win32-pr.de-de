---
title: Anhang A unterstützter Verweis auf Benutzeroberflächen Elemente
description: Dieser Anhang enthält Informationen zu den vom System bereitgestellten UI-Elementen, die von Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP und Windows 2000 Server verfügbar gemacht werden.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f75cd4251ed7d75d9aa6a2d83387a51a8b157e9
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "106340679"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Anhang A: Referenz zu unterstützten Benutzeroberflächen Elementen

Dieser Anhang enthält Informationen zu den vom System bereitgestellten UI-Elementen, die von Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP und Windows 2000 Server verfügbar gemacht werden. Diese Unterstützung ermöglicht es Client Dienstprogrammen, Informationen über vom System bereitgestellte Benutzeroberflächen Elemente in Anwendungen zu erhalten, die Microsoft Active Accessibility nicht implementieren.

Oleacc.dll unterstützt Steuerelemente, die in den Benutzeroberflächen Elementen User32.dll, Comctl32.dll und Windows definiert sind. Insbesondere werden die folgenden Typen von Benutzeroberflächen Elementen unterstützt (aufgelistet nach Windows-Klassenname).



| Windows-Klassenname                   | Typ der Benutzeroberflächen Elemente                                         | Windows Vista-Updates                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Listenfelder                                              | Keine                                                                                                                                                                                                                 |
| Schaltfläche                               | Schaltflächen, Options Felder, Check-Schaltflächen, Gruppen Felder | Unterteilte Schaltflächen können NULL oder mehr untergeordnete Elemente enthalten.                                                                                                                                                                        |
| statischen                               | Bezeichnungen                                                  | Keine                                                                                                                                                                                                                 |
| Bearbeiten                                 | Textfelder                                              | Keine                                                                                                                                                                                                                 |
| Kombinationsfeld                             | Kombinations Felder, Dropdown Listen                            | Keine                                                                                                                                                                                                                 |
| ScrollBar                            | Bildlaufleisten                                             | [**Ereignis \_ Objekt \_ contentscrollt**](event-constants.md) ist ein neues Ereignis für Steuerelemente, die über scrollfunktionen verfügen, aber keine Standard Scrollleiste als Teil des-Steuer Elements enthalten. |
| \#32768                              | Benutzermenüs                                              | Keine                                                                                                                                                                                                                 |
| \#32770                              | Benutzer Dialogfelder                                       | Keine                                                                                                                                                                                                                 |
| \#32771                              | Fenster "alt-Registerkarte"                                          | Nur im klassischen Modus verfügbar.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Statusleisten                                             | Keine                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Status anzeigen                                           | Neue Farboptionen für Status leisten werden von den Eigenschaften Microsoft Active Accessibility oder Microsoft UI Automation nicht verfügbar gemacht.                                                                                         |
| msctls \_ hotkey32                     | Hot Key-Steuerelemente                                        | Keine                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbars, Schieberegler                                      | Keine                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Auf-ab-oder Dreh Steuerelemente                                | Keine                                                                                                                                                                                                                 |
| SysAnimate32                         | Animationssteuerelement                                       | Keine                                                                                                                                                                                                                 |
| SysTabControl32                      | Registersteuerelement                                             | Keine                                                                                                                                                                                                                 |
| SysHeader32                          | Listen Ansichts Header                                       | Keine                                                                                                                                                                                                                 |
| SysListView32                        | Listenansicht-Steuerelemente                                      | Keine                                                                                                                                                                                                                 |
| SysTreeView32                        | Strukturansicht-Steuerelemente                                      | Keine                                                                                                                                                                                                                 |
| SysDateTimePick32 (Versionen 5 und 6) | Datums-und/oder Zeitauswahl                                 | Version 6 dieses Steuer Elements in Windows Vista verfügt über eine native [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung.                                                                                                           |
| SysIPAddress32                       | IP-Adress Steuerelemente                                     | Keine                                                                                                                                                                                                                 |
| Quick Infos \_ class32                    | Quick Infos                                                | Keine                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Symbolleisten                                                | Keine                                                                                                                                                                                                                 |
| RichEdit, RichEdit20A, RichEdit20W   | Textfelder                                             | Keine                                                                                                                                                                                                                 |
| SysMonthCal32 (Versionen 5 und 6)     | Monatskalender                                          | Version 6 dieses Steuer Elements in Windows Vista verfügt über eine native [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung.                                                                                                           |



 

Obwohl die Unterstützung für vom System bereitgestellte Benutzeroberflächen Elemente von Microsoft Active Accessibility auf Microsoft Windows NT 4,0 mit Service Pack 4 bereitgestellt wird, ist diese Unterstützung eingeschränkt.

In diesem Anhang werden die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aufgelistet, die von Active Accessibility Microsoft für jedes Benutzeroberflächen Element unterstützt werden. Falls zutreffend, listet die Dokumentation auch die vom Benutzeroberflächen Element Auslösern [WinEvents](winevents-infrastructure.md) auf und enthält zusätzliche Informationen zu den unterstützten Eigenschaften und Methoden. Außerdem enthält es Informationen zu Objekt Rollen und den unterstützten **IAccessible** -Methoden und-Eigenschaften.

Diese Details können Client Entwicklern helfen, unnötige Aufrufe an nicht unterstützten Eigenschaften und Methoden zu vermeiden. Diese Informationen können außerdem Server Entwicklern mitteilen, welche Eigenschaften und Methoden Ihre benutzerdefinierten Steuerelemente unterstützen sollen und welche WinEvents Ihre Steuerelemente auslöst.

Verwenden Sie die Informationen in diesem Anhang als Leitfaden. Wir empfehlen dringend, dass Sie die Microsoft Active Accessibility-Tools verwenden, um das erwartete Verhalten für Benutzeroberflächen Elemente oder Objekt Rollen zu überprüfen.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Verfügbar machen von Active Accessibility Benutzeroberflächen Elemente](how-active-accessibility-exposes-user-interface-elements.md)
-   [Verweis auf Benutzeroberflächen Element](user-interface-element-reference.md)

 

 




