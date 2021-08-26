---
description: Als Alternative zur Verwaltung von Active Directory-Partitionen über das Active Directory-Benutzer und -Computer-Verwaltungstool können Sie COM+-Partitionen programmgesteuert mithilfe einer Reihe von COM+-Objekten innerhalb der Active Directory-Systemschnittstelle (ADSI) verwalten.
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Verwalten von Partitionen in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c0aebc9ca52dee005a0343e504756e3e117c3e012098e529fb6d52033428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070580"
---
# <a name="managing-partitions-within-active-directory"></a>Verwalten von Partitionen in Active Directory

Als Alternative zur Verwaltung von Active Directory-Partitionen über das Active Directory-Benutzer und -Computer-Verwaltungstool können Sie COM+-Partitionen programmgesteuert mithilfe einer Reihe von COM+-Objekten innerhalb der Active Directory-Systemschnittstelle (ADSI) verwalten.

Unabhängig von der administrativen Technik, die Sie für die Verwaltung von COM+-Partitionen auswählen, gibt es eine allgemeine Abfolge von Schritten, die Administratoren befolgen müssen:

1.  Erstellen Sie die neuen COM+-Partitionen in Active Directory für Ihre Domäne.
2.  Erstellen Sie COM+-Partitionssätze in Active Directory, und ordnen Sie sie Ihren neu erstellten COM+-Partitionen zu.
3.  Konfigurieren Sie Ihre Active Directory-Partitionen auf Ihrem lokalen Computer mithilfe des entsprechenden COM+-Objekts. Wenn Sie eine Active Directory-Partition auf einem lokalen Computer konfigurieren, wird in diesem Partitionsordner automatisch ein **Ordner COM+-Anwendungen** erstellt.
4.  Installieren Sie Ihre COM+-Anwendungen in den entsprechenden COM+-Partitionen.

Alle oben genannten Schritte können programmgesteuert mithilfe einer Gruppe von Active Directory-Schnittstellen namens ADSI durchgeführt werden. Für die Verwaltung von Partitionen, die in ADSI verfügbar sind, stehen folgende Objekte zur Verfügung:

-   DS \_ USERPARTITIONSETLINK-NAME \_
-   DS \_ PARTITIONLINK \_ NAME
-   DS \_ OBJECTID \_ NAME
-   DS \_ \_ DEFAULTPARTITIONLINK-NAME
-   DS \_ USERLINK \_ NAME
-   DS \_ PARTITIONSET \_ NAME
-   \_DS-PARTITIONSNAME \_

Informationen zum Erstellen und Verwalten von COM+-Partitionen mithilfe der Verwaltungstools Active Directory-Benutzer und -Computer und Komponentendienste finden Sie in der Onlinehilfe, die in den einzelnen Tools verfügbar ist.

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

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



