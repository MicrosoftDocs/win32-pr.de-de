---
title: Das Betriebssystem steuert jetzt die Stromversorgung für optische Laufwerke
description: Das Betriebssystem steuert jetzt die Stromversorgung für optische Laufwerke
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc43ad47f6a9468c2850627f267d433bfa346d059231d5daa91e860d5a793aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593800"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>Das Betriebssystem steuert jetzt die Stromversorgung für optische Laufwerke

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>Beschreibung

In früheren Versionen von Windows die Stromversorgung des optischen Laufwerks nicht verwaltet, wenn das optische Laufwerk nicht verwendet wurde. Wenn nun auf dem laufwerksoptischen Laufwerk (OPTICAL Disk Drive, ODD) keine Medien vorhanden sind, schaltet das Betriebssystem die Stromversorgung des optischen Laufwerks aus. Dieses Feature wird als Zero Power ODD (ZPODD) bezeichnet. Das Feature gilt nur für optische Laufwerke, die einen Sata-Connector (Serial Advanced Technology Attachment) verwenden.

## <a name="manifestation"></a>Manifestation

Wir haben keine negativen Auswirkungen dieses neuen Verhaltens gefunden. Sie sollten sich jedoch darüber im Klaren sein, da dies zu unerwartetem Verhalten beim Schreiben von Mediensoftware führen kann.

## <a name="mitigation"></a>Minderung

Deaktivieren Sie diese Funktion in der Registrierung, um den Always On-Status wie zu ändern. Der absolute Pfad zum Registrierungswert ist:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Der Typ ist DWORD (32 Bit), und wenn der Wert 0 ist, ist ZPODD deaktiviert. Wenn es sich um einen anderen Wert handelt, ist ZPODD aktiviert.

## <a name="tests"></a>Tests

Testen Sie Ihre Software zum Schreiben von Medien auf Anomalien, die aufgrund dieses neuen Features auftreten. Informieren [Sie Microsoft über](mailto:OptIssue@microsoft.com) alle Probleme, die bei diesem neuen Feature auft sind.

 

 




