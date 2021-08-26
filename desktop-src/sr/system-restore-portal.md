---
title: Systemwiederherstellung
description: Legt Systemwiederherstellungspunkte fest und überwacht wichtige Systemänderungen eines Programms, um ein Rollback des Systems in einen vorherigen Zustand zu ermöglichen. Schreiben Sie automatischen Wiederherstellungscode oder ein WMI-Skript, um den Systemstatus auf einem registrierten Wiederherstellungspunkt wiederherzustellen.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Systemwiederherstellung
- Systemwiederherstellung, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4472806aa2c0b6f8a29cc4e687d16e262639a66c65bda37fdca970c6c38b656f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111290"
---
# <a name="system-restore"></a>Systemwiederherstellung

## <a name="purpose"></a>Zweck

Die Systemwiederherstellung überwacht und zeichnet wichtige Systemänderungen auf dem Computer eines Benutzers automatisch auf. Es wurde entwickelt, um die Supportkosten zu senken und die Kundenzufriedenheit zu erhöhen, indem es einem Benutzer ermöglicht wird, eine Änderung rückgängig zu machen, die möglicherweise ein Problem mit dem System verursacht hat, oder auf einen Tag zurück zu wechseln, an dem das System optimal war.

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler. Wenn Sie endbenutzer sind und Informationen zur Verwendung der Systemwiederherstellung suchen, finden Sie weitere Informationen unter [Was ist die Systemwiederherstellung?.](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Entwicklergruppe

Die Systemwiederherstellungs-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Für die Verwendung der Skriptschnittstelle Windows Vertrautheit mit der Verwaltungsinstrumentation (WMI) erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Systemwiederherstellungs-API wird auf Clientbetriebssystemen unterstützt, die mit Windows XP beginnen. Informationen dazu, welche Betriebssysteme für die Verwendung eines bestimmten API-Elements erforderlich sind, finden Sie im Abschnitt Anforderungen der Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                | Beschreibung                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Übersicht](about-system-restore.md)<br/>      | Eine Übersicht über die Funktionsweise der Systemwiederherstellung.<br/>                            |
| [Referenz](system-restore-reference.md)<br/> | Dokumentation zu Systemwiederherstellungsfunktionen, -strukturen und -klassen.<br/> |
| [Beispiele](using-system-restore.md)<br/>       | Ein in C geschriebenes Beispielprogramm.<br/>                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

