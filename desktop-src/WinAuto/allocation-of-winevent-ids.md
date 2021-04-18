---
title: Zuordnung von WinEvent-IDs
description: Jedes WinEvent sollte nur für einen bestimmten Zweck verwendet werden. Die Verwendung eines Windows-Ereignisses für einen unbeabsichtigten Zweck kann Konflikte mit anderen Anwendungen oder dem Betriebssystem verursachen, was dazu führen kann, dass die Anwendungen oder das Betriebssystem instabil werden.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f339641e5a3b679f572bc3b60c3e68be7b65f2a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340910"
---
# <a name="allocation-of-winevent-ids"></a>Zuordnung von WinEvent-IDs

Jedes WinEvent sollte nur für einen bestimmten Zweck verwendet werden. Die Verwendung eines Windows-Ereignisses für einen unbeabsichtigten Zweck kann Konflikte mit anderen Anwendungen oder dem Betriebssystem verursachen, was dazu führen kann, dass die Anwendungen oder das Betriebssystem instabil werden.

Microsoft hat mehrere verschiedene Kategorien von WinEvents definiert und in jeder Kategorie mindestens einen Wertebereich für die Verwendung als WinEvent-IDs definiert. Der reservierte Bereich für die Community (0xa000 – 0xafff) ist für Anwendungen verfügbar, die neue WinEvents definieren müssen. Das Verwenden von Werten aus diesem Bereich trägt dazu bei, das Risiko von Kollisionen zu verringern. Entwickler, die neue WinEvents erstellen, müssen jedoch weiterhin zusammenarbeiten, um Konflikte zwischen Ihren Anwendungen zu vermeiden.

In der folgenden Tabelle werden die WinEvent-Kategorien und die Wertebereiche angezeigt, die für jede Kategorie definiert sind.



| Category                                                | Range         | Zurzeit verwendet | Kommentare                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Microsoft Active Accessibility-Ereignisse (System reserviert) | 0x0001-0x00FF | 0x0001-0x0020    | Ereignis-ID des Ereignis \_ Systems \_ \*                                                                     |
| Microsoft Active Accessibility-Ereignisse (System reserviert) | 0x4001-0x40ff | 0x4001-0x4007    | Ereignisse der Ereignis \_ Konsolen \_ \* Ereignis-ID                                                                    |
| Benutzeroberflächenautomatisierungs-Ereignisse (System reserviert)                  | 0x4e00-0x4eff | 0x4e20-0x4e33    | Ereignis-IDs der Benutzeroberflächen Automatisierung                                                                         |
| Benutzeroberflächenautomatisierungs-Ereignisse (System reserviert)                  | 0x7500-0x75ff | 0x7530-0x759b    | Benutzeroberflächenautomatisierungs-Eigenschaften-geänderte Ereignis-IDs                                                        |
| Microsoft Active Accessibility-Ereignisse (System reserviert) | 0X8000-0x80ff | 0X8000-0x8015    | Ereignis-IDs von Ereignis \_ Objekten \_ \*                                                                     |
| OEM reserviert                                            | 0x0101-0x01ff | 0x0101-0x0122    | IAccessible2-Ereignis-IDs                                                                          |
| Community reserviert                                      | 0xa000-0xafff | Keine             | Reserviert für neue Ereignisse, die von den Spezifikationen der Barrierefreiheit-Interoperabilität (AIA) definiert werden. |
| ATOM                                                    | 0xc000-0xFFFF | 0xc000-0xFFFF    | Reserviert für benutzerdefinierte Ereignisse, die zur Laufzeit zugeordnet werden                                                 |



 

In den folgenden Themen werden die WinEvent-Bereiche ausführlicher beschrieben.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Microsoft Active Accessibility-und Benutzeroberflächenautomatisierungs-Ereignisse

Fünf Bereiche von WinEvent-IDs sind für die Verwendung durch Microsoft Active Accessibility und Microsoft UI Automation reserviert. Der erste Bereich (0x0001 – 0x00FF) ist für Ereignisse auf Systemebene reserviert und wird in der Regel zum Beschreiben von Situationen verwendet, die sich auf alle Anwendungen im System auswirken. Der zweite Bereich (0x4001 – 0x40ff) ist für Windows-Konsolen spezifische Ereignisse reserviert. Der dritte (0x4e00 – 0x4eff) und vierte Bereich (0x7500 – 0x75ff) dienen der Reflektion von Benutzeroberflächenautomatisierungs-Ereignissen. Schließlich ist der fünfte Bereich (0X8000 – 0x80ff) für Ereignisse auf Objektebene, die sich auf Objekte innerhalb einer Anwendung beziehen.

Alle Microsoft Active Accessibility-und Benutzeroberflächenautomatisierungs-Ereignisse werden in den Header Dateien Winuser. h und UIAutomationClient. h definiert.

## <a name="oem-reserved-events"></a>Reservierte OEM-Ereignisse

Der reservierte Bereich des OEM ist für alle Personen offen, die WinEvents als Kommunikationsmechanismus verwenden müssen. Entwickler sollten Ereignis Definitionen zusammen mit ihren Parametern (oder auch mit zugeordneten Objekttypen) für die Ereignisverarbeitung definieren und veröffentlichen, damit versehentliche Konflikte von Ereignis-IDs vermieden werden können. In der IAccessible2-Spezifikation wird ein Teil des reservierten OEM-Bereichs verwendet.

## <a name="community-reserved-events"></a>Reservierte Community-Ereignisse

Der reservierte Bereich für die Community richtet sich nach den von der Barrierefreiheits-Interoperabilitäts-Alliance (AIA) für die Verwendung in der gesamten Branche angegebenen Entwicklern wird dringend empfohlen, eine offizielle Spezifikation zu definieren und zu veröffentlichen, bevor Werte aus diesem Bereich verwendet werden.

## <a name="atom-events"></a>Atom-Ereignisse

Der Atom-Bereich ist für Ereignis-IDs reserviert, die zur Laufzeit über die Benutzeroberflächenautomatisierungs-Erweiterbarkeits-API zugeordnet werden. Verwenden Sie für keinen anderen Zweck die Werte aus dem Atom-Bereich. Die Verwendung der [**globaladdatom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) -Funktion mit einer Zeichen folgen-GUID ist die empfohlene Methode zum Zuordnen von WinEvents aus dem Atom-Bereich.

## <a name="using-values-from-a-reserved-range"></a>Verwenden von Werten aus einem reservierten Bereich

Gemäß der WinEvent-Spezifikation können Werte aus dem vom System reservierten Bereich oder einem anderen nicht definierten Bereich nicht verwendet werden, ohne das SDK zu überarbeiten. Bei neuen WinEvents sollten Anwendungen Werte aus den reservierten reservierten Bereichen OEM oder Community verwenden. Bevor Sie ein neues WinEvent verwenden, werden Entwickler dringend darauf hingewiesen, ihre Spezifikationen offen und weitgehend gemeinsam zu nutzen. Sie sollten mit der Interoperabilitäts-Interoperabilität arbeiten, um die WinEvent-Spezifikationen zu definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Interoperabilität mit Barrierefreiheit](https://www.atia.org/)
</dt> </dl>

 

 