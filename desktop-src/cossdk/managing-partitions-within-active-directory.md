---
description: Als Alternative zur Verwaltung von Active Directory Partitionen über das Verwaltungs Tool "Active Directory Benutzer und Computer" können Sie COM+-Partitionen Programm gesteuert verwalten, indem Sie eine Reihe von COM+-Objekten in der Active Directory System Schnittstelle (ADSI) verwenden.
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Verwalten von Partitionen in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524176"
---
# <a name="managing-partitions-within-active-directory"></a>Verwalten von Partitionen in Active Directory

Als Alternative zur Verwaltung von Active Directory Partitionen über das Verwaltungs Tool "Active Directory Benutzer und Computer" können Sie COM+-Partitionen Programm gesteuert verwalten, indem Sie eine Reihe von COM+-Objekten in der Active Directory System Schnittstelle (ADSI) verwenden.

Unabhängig von der administrativen Methode, die Sie für die Verwaltung von COM+-Partitionen auswählen, gibt es eine allgemeine Abfolge von Schritten, die Administratoren befolgen müssen:

1.  Erstellen Sie die neuen COM+-Partitionen in Active Directory für Ihre Domäne.
2.  Erstellen Sie com+-Partitions Sätze innerhalb Active Directory, und ordnen Sie Sie den neu erstellten COM+-Partitionen zu.
3.  Konfigurieren Sie Ihre Active Directory Partitionen auf dem lokalen Computer mit dem entsprechenden COM+-Objekt. Wenn Sie eine Active Directory Partition auf einem lokalen Computer konfigurieren, wird automatisch ein **com+-Anwendungs** Ordner in diesem Partitions Ordner erstellt.
4.  Installieren Sie die com+-Anwendungen in den entsprechenden COM+-Partitionen.

Alle vorangehenden Schritte können Programm gesteuert mithilfe eines Satzes von Active Directory-Schnittstellen namens ADSI ausgeführt werden. Die verfügbaren Objekte zum Verwalten von Partitionen, die in ADSI verfügbar sind, lauten wie folgt:

-   DS \_ userpartitionsetlink- \_ Name
-   DS- \_ \_ partitionlinkname
-   Name der DS- \_ objectID \_
-   DS \_ defaultpartitionlinkname \_
-   Name des DS- \_ Benutzer Links \_
-   DS \_ partitionset- \_ Name
-   Name der DS- \_ Partition \_

Informationen zum Erstellen und Verwalten von COM+-Partitionen durch die Verwendung der Active Directory Benutzer und Computer und Verwaltungs Tools für Komponenten Dienste finden Sie in der Online Hilfe, die in den einzelnen Tools verfügbar ist.

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

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



