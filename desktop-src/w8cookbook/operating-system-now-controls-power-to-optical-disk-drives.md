---
title: Betriebssystem steuert jetzt die Stromversorgung auf optischen Laufwerken
description: Betriebssystem steuert jetzt die Stromversorgung auf optischen Laufwerken
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730736"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>Betriebssystem steuert jetzt die Stromversorgung auf optischen Laufwerken

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

In früheren Versionen von Windows wurde die Stromversorgung des optischen Laufwerks nicht verwaltet, als das optische Laufwerk nicht verwendet wurde. Wenn auf dem optischen Laufwerk (ungerade) kein Medium vorhanden ist, schaltet das Betriebssystem die Stromversorgung auf dem optischen Laufwerk aus. Diese Funktion wird als Zero Power Odd (zpodd) bezeichnet. Diese Funktion gilt nur für optische Laufwerke, die einen Slimline SATA (Serial Advanced Technology Attachment)-Connector verwenden.

## <a name="manifestation"></a>Ausstrahlung

Wir haben keine negativen Auswirkungen von diesem neuen Verhalten festgestellt. Sie sollten sich jedoch bewusst sein, da dies zu unerwartetem Verhalten von Medien-Schreibsoftware führen kann.

## <a name="mitigation"></a>Minderung

Um den AlwaysOn-Status wiederherzustellen, deaktivieren Sie diese Funktionalität in der Registrierung. Der absolute Pfad zum Registrierungs Wert lautet:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Der Typ ist "DWORD (32 Bit)", und wenn der Wert 0 ist, wird zpodd deaktiviert. Wenn es sich um einen anderen Wert handelt, ist zpodd aktiviert.

## <a name="tests"></a>Tests

Testen Sie Ihre Medien zum Schreiben von Software auf Anomalien, die aufgrund dieses neuen Features auftreten. [Informieren Sie Microsoft](mailto:OptIssue@microsoft.com) über Probleme, die Sie mit dieser neuen Funktion finden.

 

 




