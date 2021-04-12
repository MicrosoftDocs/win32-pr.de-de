---
description: Administratoren können com+ verwenden, um COM+-Partitionen Programm gesteuert zu erstellen und zu konfigurieren.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Erstellen und Konfigurieren von COM+-Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523560"
---
# <a name="creating-and-configuring-com-partitions"></a>Erstellen und Konfigurieren von COM+-Partitionen

Administratoren können com+ verwenden, um COM+-Partitionen Programm gesteuert zu erstellen und zu konfigurieren. Tatsächlich können alle Erstellungs-und Konfigurationsaufgaben, die ein Administrator aus den Komponenten Diensten oder den Active Directory Verwaltungs Tools für Benutzer und Computer ausführen kann, mithilfe von com+-Sammlungen,-Objekten und-Schnittstellen oder über die Active Directory System Schnittstelle (ADSI) durchgeführt werden.

**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar. Die globale Partition ist die einzige verfügbare com+-Partition.

* * Windows 2000: * * der com+-Partitions Dienst ist in Windows 2000 nicht verfügbar.

> [!Note]  
> Der com+-Partitions Dienst ist standardmäßig nicht aktiviert. Um den com+-Partitions Dienst zu verwenden, müssen Sie ihn über das Verwaltungs Tool Komponenten Dienste oder durch Ändern der partitionsenabled-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung auf true aktivieren.

 

Zum Ausführen von Partitions bezogenen Aufgaben bietet com+ die folgenden Programmier Elemente:

-   Methoden und Eigenschaften der [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) -Schnittstelle in der [**comadmincatalog**](comadmincatalog.md) -Klasse:
    -   [**Currentpartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) -Eigenschaft.
    -   [**Currentpartitionid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) -Eigenschaft.
    -   [**Currentpartitionname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) -Eigenschaft.
    -   [**Flushpartitioncache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) -Methode.
    -   [**Getpartitionid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) -Methode.
    -   [**Getpartitionname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) -Methode.
    -   [**Globalpartitionid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) -Eigenschaft.
-   Eine Reihe von COM+-Objekten zum Erstellen und Verwalten von Partitionen in Active Directory.
-   Ein com+-Registrierungsschlüssel, **partitioncache**, zum Ändern der Partitions Cache Größe.
-   Eine Reihe von Partitions bezogenen [com+-Verwaltungs Sammlungen](com--administration-collections.md):
    -   [**Partitionen**](partitions.md) -Auflistung.
    -   [**Partitionusers**](partitionusers.md) -Auflistung.
    -   [**Rolesforpartition**](rolesforpartition.md) -Auflistung.
    -   [**Usersinpartitionrole**](usersinpartitionrole.md) -Auflistung.
-   Eigenschaften anderer [com+-Verwaltungs Sammlungen](com--administration-collections.md):
    -   PartitionID-Eigenschaft für die [**ApplicationInstance**](applicationinstances.md) -Auflistung.
    -   Apppartitionid-Eigenschaft in der [**Anwendungs**](applications.md) Auflistung.
    -   Die Eigenschaften partitiondescription, PartitionID und partitionName in der Auflistung [**filesforimport**](filesforimport.md) .
    -   Die Eigenschaften "dspartitionlookupabled", "localpartitionlookupabled" und "partitionsenabled" in der [**LocalComputer**](localcomputer.md) -Sammlung.
    -   Die Eigenschaften "eventclasspartitionid" und "abonneaspartitionid" in der " [**abonptionsforcomponent**](subscriptionsforcomponent.md) "-Auflistung.
    -   Die Eigenschaften eventclasspartitionid und abonneaspartitionid in der [**transientabonnements**](transientsubscriptions.md) -Auflistung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitions Metriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitions Caches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von lokalen Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



