---
title: Anhang A Supported Benutzeroberfläche Elements Reference
description: Dieser Anhang enthält Informationen zu den vom System bereitgestellten Benutzeroberflächenelementen, die von Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP und Windows 2000 Server verfügbar gemacht werden.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e434eec9a480f46bb352dbd5b523b8b5c9cde6624c9d94372703d054e945bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994370"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Anhang A: Referenz zu Benutzeroberfläche Unterstützten Elementen

Dieser Anhang enthält Informationen zu den vom System bereitgestellten Benutzeroberflächenelementen, die von Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP und Windows 2000 Server verfügbar gemacht werden. Durch diese Unterstützung können Client-Hilfsprogramme Informationen zu vom System bereitgestellten Benutzeroberflächenelementen in Anwendungen erhalten, die keine Microsoft Active Accessibility.

Oleacc.dll unterstützt Steuerelemente, die in den Benutzeroberflächenelementen User32.dll, Comctl32.dll und Windows definiert sind. Insbesondere werden die folgenden Typen von Benutzeroberflächenelementen unterstützt (aufgelistet Windows Klassennamen).



| Windows Klassenname                   | Benutzeroberflächenelementtyp                                         | Windows Vista-Updates                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Listenfelder                                              | Keine                                                                                                                                                                                                                 |
| Schaltfläche                               | Schaltflächen, Optionsfelder, Kontrollkästchen, Gruppenfelder | Geteilte Schaltflächen können 0 (null) oder mehr unterteilen.                                                                                                                                                                        |
| statischen                               | Bezeichnungen                                                  | Keine                                                                                                                                                                                                                 |
| Bearbeiten                                 | Textfelder                                              | Keine                                                                                                                                                                                                                 |
| Kombinationsfeld                             | Kombinationsfelder, Dropdownlisten                            | Keine                                                                                                                                                                                                                 |
| ScrollBar                            | Bildlaufleisten                                             | [**EVENT \_ OBJECT \_ CONTENTSCROLLED ist**](event-constants.md) ein neues Ereignis für Das Steuerelement, das bildlauffunktionen hat, aber keine Standardbildlaufleiste als Teil des Steuerelements enthält. |
| \#32768                              | BENUTZERmenüs                                              | Keine                                                                                                                                                                                                                 |
| \#32770                              | BENUTZERdialogfelder                                       | Keine                                                                                                                                                                                                                 |
| \#32771                              | Alt-Tab-Fenster                                          | Nur im klassischen Modus verfügbar.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Statusleisten                                             | Keine                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Statusleisten                                           | Neue Farboptionen für Statusleisten werden von den Eigenschaften Microsoft Active Accessibility microsoft Benutzeroberflächenautomatisierung nicht verfügbar gemacht.                                                                                         |
| msctls \_ hotkey32                     | Hot-Key-Steuerelemente                                        | Keine                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbars, Schieberegler                                      | Keine                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Auf-Ab- oder Drehungssteuerelemente                                | Keine                                                                                                                                                                                                                 |
| SysAnimate32                         | Animationssteuerelement                                       | Keine                                                                                                                                                                                                                 |
| SysTabControl32                      | Registersteuerelement                                             | Keine                                                                                                                                                                                                                 |
| SysHeader32                          | Listenansichtsheader                                       | Keine                                                                                                                                                                                                                 |
| SysListView32                        | Listenansichtssteuerelemente                                      | Keine                                                                                                                                                                                                                 |
| SysTreeView32                        | Strukturansichtssteuerelemente                                      | Keine                                                                                                                                                                                                                 |
| SysDateTimePick32 (Versionen 5 und 6) | Datums- und/oder Uhrzeitauswahl                                 | Version 6 dieses Steuerelements in Windows Vista verfügt über eine native [**IAccessible-Implementierung.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                                                                                                           |
| SysIPAddress32                       | IP-Adresssteuerelemente                                     | Keine                                                                                                                                                                                                                 |
| \_QuickInfos-Klasse32                    | Quickinfos                                                | Keine                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Symbolleisten                                                | Keine                                                                                                                                                                                                                 |
| RICHEDIT, RichEdit20A, RichEdit20W   | Textfelder                                             | Keine                                                                                                                                                                                                                 |
| SysMonthCal32 (Versionen 5 und 6)     | Monatskalender                                          | Version 6 dieses Steuerelements in Windows Vista verfügt über eine native [**IAccessible-Implementierung.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                                                                                                           |



 

Obwohl einige Unterstützung für vom System bereitgestellte Benutzeroberflächenelemente von Microsoft Active Accessibility unter Microsoft Windows NT 4.0 mit Service Pack 4 bereitgestellt wird, ist diese Unterstützung eingeschränkt.

In diesem Anhang sind die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden aufgeführt, Microsoft Active Accessibility für jedes Benutzeroberflächenelement unterstützt werden. Falls zutreffend, werden in der Dokumentation auch die [WinEvents](winevents-infrastructure.md) aufgeführt, die vom Benutzeroberflächenelement ausgelöst werden, und es werden zusätzliche Informationen zu den unterstützten Eigenschaften und Methoden enthalten. Sie enthält auch Informationen zu Objektrollen und deren unterstützten **IAccessible-Methoden** und -Eigenschaften.

Mithilfe dieser Details können Cliententwickler unnötige Aufrufe an nicht unterstützte Eigenschaften und Methoden vermeiden. Diese Informationen informieren Serverentwickler auch darüber, welche Eigenschaften und Methoden ihre benutzerdefinierten Steuerelemente unterstützen sollten und welche WinEvents von ihren Steuerelementen ausgelöst werden sollen.

Verwenden Sie die Informationen in diesem Anhang als Leitfaden. Es wird dringend empfohlen, die tools Microsoft Active Accessibility verwenden, um das erwartete Verhalten für Benutzeroberflächenelemente oder Objektrollen zu überprüfen.

Weitere Informationen finden Sie in den folgenden Themen:

-   [How Active Accessibility Exposes Benutzeroberfläche Elements](how-active-accessibility-exposes-user-interface-elements.md)
-   [Benutzeroberfläche Elementverweis](user-interface-element-reference.md)

 

 




