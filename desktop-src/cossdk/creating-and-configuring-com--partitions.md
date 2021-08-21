---
description: Administratoren können COM+ verwenden, um COM+-Partitionen programmgesteuert zu erstellen und zu konfigurieren.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Erstellen und Konfigurieren von COM+-Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cc9623272d4aba345cc666deb5c63965584af94f42dbf869b00cf7d52a2f30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858990"
---
# <a name="creating-and-configuring-com-partitions"></a>Erstellen und Konfigurieren von COM+-Partitionen

Administratoren können COM+ verwenden, um COM+-Partitionen programmgesteuert zu erstellen und zu konfigurieren. Tatsächlich können alle Erstellungs- und Konfigurationsaufgaben, die ein Administrator über die Komponentendienste oder die Active Directory-Benutzer und -Computer-Verwaltungstools ausführen kann, mithilfe von COM+-Sammlungen, -Objekten und -Schnittstellen oder über die Active Directory-Systemschnittstelle (ADSI) ausgeführt werden.

**Windows XP:** Com+-Partitionen können nicht erstellt, konfiguriert oder delegiert werden. Die globale Partition ist die einzige verfügbare COM+-Partition.

**Windows 2000: ** Der COM+-Partitionsdienst ist in Windows 2000 nicht verfügbar.

> [!Note]  
> Der COM+-Partitionsdienst ist standardmäßig nicht aktiviert. Um den COM+-Partitionsdienst verwenden zu können, müssen Sie ihn über das Verwaltungstool komponentendienste oder durch Ändern der PartitionsEnabled-Eigenschaft in der [**LocalComputer-Sammlung**](localcomputer.md) in True aktivieren.

 

Um partitionsbezogene Aufgaben auszuführen, stellt COM+ die folgenden Programmierelemente zur Verfügung:

-   Methoden und Eigenschaften der [**ICOMAdminCatalog2-Schnittstelle**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) in der [**COMAdminCatalog-Klasse:**](comadmincatalog.md)
    -   [**CurrentPartition-Eigenschaft.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition)
    -   [**CurrentPartitionID-Eigenschaft.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid)
    -   [**CurrentPartitionName-Eigenschaft.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname)
    -   [**FlushPartitionCache-Methode.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache)
    -   [**GetPartitionID-Methode.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid)
    -   [**GetPartitionName-Methode.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname)
    -   [**GlobalPartitionID-Eigenschaft.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid)
-   Eine Reihe von COM+-Objekten zum Erstellen und Verwalten von Partitionen in Active Directory.
-   Ein COM+-Registrierungsschlüssel, **PartitionCache,** zum Ändern der Größe des Partitionscaches.
-   Eine Reihe partitionsbezogener [COM+-Verwaltungssammlungen:](com--administration-collections.md)
    -   [**Partitionssammlung.**](partitions.md)
    -   [**PartitionUsers-Auflistung.**](partitionusers.md)
    -   [**RolesForPartition-Auflistung.**](rolesforpartition.md)
    -   [**UsersInPartitionRole-Auflistung.**](usersinpartitionrole.md)
-   Eigenschaften anderer [COM+-Verwaltungssammlungen:](com--administration-collections.md)
    -   PartitionID-Eigenschaft für die [**ApplicationInstances-Auflistung.**](applicationinstances.md)
    -   AppPartitionID-Eigenschaft für die [**Anwendungssammlung.**](applications.md)
    -   Die Eigenschaften PartitionDescription, PartitionID und PartitionName für die [**FilesForImport-Auflistung.**](filesforimport.md)
    -   Die Eigenschaften DSPartitionLookupEnabled, LocalPartitionLookupEnabled und PartitionsEnabled in der [**LocalComputer-Sammlung.**](localcomputer.md)
    -   Die Eigenschaften EventClassPartitionID und SubscriberPartitionID für die [**SubscriptionsForComponent-Auflistung.**](subscriptionsforcomponent.md)
    -   Die Eigenschaften EventClassPartitionID und SubscriberPartitionID für die [**TransientSubscriptions-Auflistung.**](transientsubscriptions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitionsmetriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitionscaches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von lokalen Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



