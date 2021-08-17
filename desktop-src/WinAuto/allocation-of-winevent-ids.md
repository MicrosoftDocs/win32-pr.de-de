---
title: Zuordnung von WinEvent-IDs
description: Jedes WinEvent ist nur für einen bestimmten Zweck vorgesehen. Die Verwendung eines WinEvent für einen unbeabsichtigten Zweck kann konflikte mit anderen Anwendungen oder dem Betriebssystem verursachen, was dazu führen kann, dass die Anwendungen oder das Betriebssystem instabil werden.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e877c6adcba79870d887e0bdb0d2eb9137d9e04fda4c1cc770414d0dd01f96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326882"
---
# <a name="allocation-of-winevent-ids"></a>Zuordnung von WinEvent-IDs

Jedes WinEvent ist nur für einen bestimmten Zweck vorgesehen. Die Verwendung eines WinEvent für einen unbeabsichtigten Zweck kann konflikte mit anderen Anwendungen oder dem Betriebssystem verursachen, was dazu führen kann, dass die Anwendungen oder das Betriebssystem instabil werden.

Microsoft hat mehrere verschiedene Kategorien von WinEvents definiert und für jede Kategorie einen oder mehrere Wertebereiche definiert, die als WinEvent-IDs verwendet werden können. Der Community reservierte Bereich (0xA000 – 0xAFFF) ist für Anwendungen verfügbar, die neue WinEvents definieren müssen. Die Verwendung von Werten aus diesem Bereich trägt dazu bei, das Risiko von Kollisionen zu reduzieren. Entwickler, die neue WinEvents erstellen, müssen jedoch weiterhin zusammenarbeiten, um Konflikte zwischen ihren Anwendungen zu vermeiden.

Die folgende Tabelle zeigt die WinEvent-Kategorien und die Wertebereiche, die für jede Kategorie definiert sind.



| Kategorie                                                | Range         | Derzeit verwendet | Kommentare                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Microsoft Active Accessibility Ereignisse (systemdeserviert) | 0x0001-0x00FF | 0x0001-0x0020    | EVENT \_ \_ \* SYSTEM-Ereignis-IDs                                                                     |
| Microsoft Active Accessibility Ereignisse (systemdeserviert) | 0x4001-0x40FF | 0x4001-0x4007    | \_ \_ \* EREIGNISKONSOLEn-Ereignis-IDs                                                                    |
| Benutzeroberflächenautomatisierung Ereignisse (system reserviert)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | Benutzeroberflächenautomatisierung Ereignis-IDs                                                                         |
| Benutzeroberflächenautomatisierung Ereignisse (system reserviert)                  | 0x7500-0x75FF | 0x7530-0x759B    | Benutzeroberflächenautomatisierung eigenschaftenveränderte Ereignis-IDs                                                        |
| Microsoft Active Accessibility Ereignisse (systemdeserviert) | 0x8000-0x80FF | 0x8000-0x8015    | EVENT \_ \_ \* OBJECT-Ereignis-IDs                                                                     |
| OEM reserviert                                            | 0x0101-0x01FF | 0x0101-0x0122    | IAccessible2-Ereignis-IDs                                                                          |
| Community Reserviert                                      | 0xA000-0xAFFF | Keine             | Reserviert für neue Ereignisse, die durch Spezifikationen der Accessibility Interoperability Alliance (AIA) definiert werden |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Reserviert für benutzerdefinierte Ereignisse, die zur Laufzeit zugeordnet werden                                                 |



 

In den folgenden Themen werden die WinEvent-Bereiche ausführlicher beschrieben.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>ereignisse Microsoft Active Accessibility und Benutzeroberflächenautomatisierung

Fünf WinEvent-IDs sind für die Verwendung durch Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung reserviert. Der erste Bereich (0x0001 – 0x00FF) ist für Ereignisse auf Systemebene reserviert, die in der Regel zum Beschreiben von Situationen verwendet werden, die sich auf alle Anwendungen im System auswirken. Der zweite Bereich (0x4001 – 0x40FF) ist für Windows konsolenspezifische Ereignisse reserviert. Der dritte (0x4E00– 0x4EFF) und der vierte Bereich (0x7500 – 0x75FF) dienen der Reflektion von Benutzeroberflächenautomatisierung Ereignissen. Schließlich gilt der fünfte Bereich (0x8000 – 0x80FF) für Ereignisse auf Objektebene, die sich auf Situationen beziehen, die für Objekte innerhalb einer Anwendung spezifisch sind.

Alle Microsoft Active Accessibility- und Benutzeroberflächenautomatisierung-Ereignisse werden in den Headerdateien WinUser.h und UIAutomationClient.h definiert.

## <a name="oem-reserved-events"></a>Reservierte OEM-Ereignisse

Der reservierte OEM-Bereich ist für alle Benutzer offen, die WinEvents als Kommunikationsmechanismus verwenden müssen. Entwickler sollten Ereignisdefinitionen zusammen mit ihren Parametern (oder auch mit zugeordneten Objekttypen) für die Ereignisverarbeitung definieren und veröffentlichen, damit versehentliche Konflikte von Ereignis-IDs vermieden werden können. Die IAccessible2-Spezifikation verwendet einen Teil des reservierten OEM-Bereichs.

## <a name="community-reserved-events"></a>Community Reservierte Ereignisse

Der Community reservierte Bereich gilt für WinEvents, die von der Accessibility Interoperability Alliance (AIA) für die Verwendung in der gesamten Branche angegeben werden. Entwicklern wird dringend empfohlen, eine offizielle Spezifikation zu definieren und zu veröffentlichen, bevor Werte aus diesem Bereich verwendet werden.

## <a name="atom-events"></a>ATOM-Ereignisse

Der ATOM-Bereich ist für Ereignis-IDs reserviert, die zur Laufzeit über die Benutzeroberflächenautomatisierung Erweiterbarkeits-API zugeordnet werden. Verwenden Sie die Werte aus dem ATOM-Bereich nicht für andere Zwecke. Die Verwendung der [**GlobalAddAtom-Funktion**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) mit einer Zeichenfolgen-GUID ist die empfohlene Methode zum Zuordnen von WinEvents aus dem ATOM-Bereich.

## <a name="using-values-from-a-reserved-range"></a>Verwenden von Werten aus einem reservierten Bereich

Gemäß der WinEvent-Spezifikation können Werte aus dem reservierten Systembereich oder einem anderen nicht definierten Bereich ohne Überarbeitung des SDK nicht verwendet werden. Bei neuen WinEvents sollten Anwendungen Werte aus reservierten OEM- oder Community reservierten Bereichen verwenden. Vor der Verwendung eines neuen WinEvents wird Entwicklern dringend empfohlen, ihre Spezifikationen offen und umfassend zu teilen, und sie sollten mit der Accessibility Interoperability Alliance zusammenarbeiten, um WinEvent-Spezifikationen zu definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Accessibility Interoperability Alliance](https://www.atia.org/)
</dt> </dl>

 

 