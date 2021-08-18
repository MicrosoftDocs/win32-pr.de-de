---
description: Das Feature COM+-Partitionen enthält einen Partitionscache. Dieser Cache speichert Zuordnungen zwischen Benutzern und Partitionen und ist so konzipiert, dass sich wiederholender Active Directory-Zugriff vermieden wird.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Konfigurieren des Partitionscaches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906e36065244ab7f2ffa54cad5a7aca33a0c152744af2b6017edb95a8a960b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128962"
---
# <a name="configuring-the-partition-cache"></a>Konfigurieren des Partitionscaches

Das Feature COM+-Partitionen enthält einen Partitionscache. Dieser Cache speichert Zuordnungen zwischen Benutzern und Partitionen und ist so konzipiert, dass sich wiederholender Active Directory-Zugriff vermieden wird.

## <a name="changing-cache-size"></a>Ändern der Cachegröße

Der Partitionscache besteht aus drei Tabellen, deren Größe geändert werden kann, um die Leistung zu verbessern. Diese Tabellen bestehen aus der Anzahl der SID-Einträge im Cache, der Anzahl der Organisationseinheiteneinträge im Cache und der Anzahl der Partitionseinträge im Cache.

Um diese Tabellengrößen zu ändern, können Administratoren die Werte eines Registrierungsschlüssels ändern. Der Registrierungsschlüssel und seine Werte sind wie folgt:

**HKLM \\ SOFTWARE \\ Microsoft \\ COM3 \\ PartitionCache**



| Schlüsselwerte                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSid-Einträge**<br/>       | Enthält den REG \_ DWORD-Wert für die Anzahl der SID-Einträge im Cache (default=512). Dieser Wert sollte auf einen Wert festgelegt werden, der größer als die Anzahl eindeutiger Identitäten ist, die ein Computer im Zeitfenster für die Cacheinvalidierung warten wird.<br/>                                                                                                                                                  |
| **NumName-Einträge**<br/>      | Enthält den REG \_ DWORD-Wert für die Anzahl der Oe-Namenseinträge im Cache (default=64). Dieser Wert sollte auf einen Wert festgelegt werden, der größer als die Anzahl der eindeutigen OE-Namen ist, die ein Computer im Zeitfenster für die Cacheinvalidierung warten wird.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Enthält den REG \_ DWORD-Wert für die Anzahl der Partitionseinträge im Cache (default=1024).<br/> Im Zeitfenster für die Cacheinvalidierung sollte der DWORD-Wert auf eine Zahl festgelegt werden, die größer als die Anzahl der eindeutigen Partitionen ist, die ein Computer bedient. Dies liegt daran, dass der Kontext einer Komponente eine Partitions-ID für eine Partition enthalten kann, die sich nicht auf diesem Computer befindet. <br/> |
| **EntryExpiration**<br/>     | Enthält den REG \_ DWORD-Wert für die Taktanzahl (jeder Tick = ~7 Minuten), bis ein Cacheeintrag ungültig wird (default=4 (~28 Minuten)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Leeren des Caches

Da COM+ die Standardpartition für Benutzer zwischenspeichert, sollten Sie diese Methode aufrufen, nachdem Sie die Standardpartition für einen Benutzer in Active Directory geändert haben. Administratoren können dies programmgesteuert tun, indem sie die [**FlushPartitionCache-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitionsmetriken](collecting-partition-metrics.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten lokaler Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




