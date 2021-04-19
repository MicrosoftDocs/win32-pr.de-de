---
description: Die com+-Partitions Funktion enthält einen Partitions Cache. Dieser Cache speichert Benutzer-zu-Partition-Zuordnungen und ist darauf ausgelegt, sich wiederholende Active Directory Zugriffe zu vermeiden.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Konfigurieren des Partitions Caches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346248"
---
# <a name="configuring-the-partition-cache"></a>Konfigurieren des Partitions Caches

Die com+-Partitions Funktion enthält einen Partitions Cache. Dieser Cache speichert Benutzer-zu-Partition-Zuordnungen und ist darauf ausgelegt, sich wiederholende Active Directory Zugriffe zu vermeiden.

## <a name="changing-cache-size"></a>Ändern der Cache Größe

Der Partitions Cache besteht aus drei Tabellen, deren Größe geändert werden kann, um die Leistung zu verbessern. Diese Tabellen bestehen aus der Anzahl der SID-Einträge im Cache, der Anzahl der OU-Einträge im Cache und der Anzahl der Partitions Einträge im Cache.

Um diese Tabellen Größen zu ändern, können Administratoren die Werte eines Registrierungsschlüssels ändern. Der Registrierungsschlüssel und die zugehörigen Werte lauten wie folgt:

**HKLM \\ Software \\ Microsoft \\ COM3 \\ partitioncache**



| Schlüsselwerte                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Numsidentries**<br/>       | Enthält den reg \_ DWORD-Wert für die Anzahl der SID-Einträge im Cache (Standardwert = 512). Dieser Wert sollte auf einen Wert festgelegt werden, der größer als die Anzahl der eindeutigen Identitäten ist, die ein Computer im Zeitfenster für die Cache Invalidierung verwendet.<br/>                                                                                                                                                  |
| **Numnameentries**<br/>      | Enthält den reg \_ DWORD-Wert für die Anzahl der Organisationseinheiten-namens Einträge im Cache (Standard = 64). Dieser Wert sollte auf einen Wert festgelegt werden, der größer als die Anzahl der eindeutigen Organisationseinheiten Namen ist, die ein Computer im Zeitfenster für die Cache Invalidierung verarbeitet.<br/>                                                                                                                                                 |
| **Numpartitionentries**<br/> | Enthält den reg \_ DWORD-Wert für die Anzahl der Partitions Einträge im Cache (Standardwert = 1024).<br/> Im Zeitfenster für die Cache Validierung sollte der DWORD-Wert auf eine Zahl festgelegt werden, die größer als die Anzahl der eindeutigen Partitionen ist, die von einem Computer gewartet werden. Dies liegt daran, dass der Kontext einer Komponente eine Partitions-ID für eine Partition enthalten kann, die nicht auf diesem Computer gespeichert ist. <br/> |
| **Entryablauf**<br/>     | Enthält den reg \_ DWORD-Wert für die Tick-Anzahl (jedes Tick = ~ 7 Minuten), bis ein Cache Eintrag ungültig wird (Standardwert = 4 (~ 28 Minuten)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Leeren des Caches

Da com+ die Standard Partition für Benutzer zwischenspeichert, können Sie diese Methode nach dem Ändern der Standard Partition für einen Benutzer im Active Directory abrufen. Administratoren können dies Programm gesteuert durch Aufrufen der [**flushpartitioncache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) -Methode durchführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitions Metriken](collecting-partition-metrics.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von lokalen Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




