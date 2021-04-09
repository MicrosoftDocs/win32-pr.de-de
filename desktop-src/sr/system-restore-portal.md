---
title: Systemwiederherstellung
description: Legt System Wiederherstellungspunkte fest und überwacht wichtige Systemänderungen von einem Programm, um ein Rollback des Systems in einen früheren Zustand zu ermöglichen. Schreiben Sie automatischen Wiederherstellungscode oder ein WMI-Skript, um den Systemstatus auf einem registrierten Wiederherstellungspunkt wiederherzustellen
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Systemwiederherstellung
- System Wiederherstellung, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101934"
---
# <a name="system-restore"></a>Systemwiederherstellung

## <a name="purpose"></a>Zweck

Bei der Systemwiederherstellung werden wichtige Systemänderungen auf dem Computer eines Benutzers automatisch überwacht und aufgezeichnet. Es wurde entwickelt, um Supportkosten zu senken und die Kundenzufriedenheit zu erhöhen, indem ein Benutzer eine Änderung rückgängig machen kann, die möglicherweise ein Problem mit dem System verursacht hat, oder bis zu einem Tag zurückgekehrt ist, an dem das System optimal funktioniert.

> [!Note]  
> Die folgende Dokumentation ist für Entwickler bestimmt. Wenn Sie ein Endbenutzer sind, der Informationen zur Verwendung der Systemwiederherstellung sucht, finden Sie weitere Informationen unter [Was ist die Systemwiederherstellung?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Entwicklergruppe

Die Systemwiederherstellungs-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Eine Vertrautheit mit Windows-Verwaltungsinstrumentation (WMI) ist erforderlich, um die Skript Schnittstelle zu verwenden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Systemwiederherstellungs-API wird ab Windows XP auf Client Betriebssystemen unterstützt. Informationen dazu, welche Betriebssysteme für die Verwendung eines bestimmten API-Elements erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der zugehörigen Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                | BESCHREIBUNG                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Übersicht](about-system-restore.md)<br/>      | Eine Übersicht über die Funktionsweise der System Wiederherstellung.<br/>                            |
| [Verweis](system-restore-reference.md)<br/> | Dokumentation der Funktionen, Strukturen und Klassen der System Wiederherstellung.<br/> |
| [Beispiele](using-system-restore.md)<br/>       | Ein Beispielprogramm, das in C geschrieben ist.<br/>                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

