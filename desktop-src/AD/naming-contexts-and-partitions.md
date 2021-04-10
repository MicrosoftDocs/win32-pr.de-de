---
title: Benennungs Kontexte und Verzeichnis Partitionen
description: Jeder Domänen Controller in einer Domänen Gesamtstruktur, die von Active Directory Domain Services gesteuert wird, umfasst Verzeichnis Partitionen
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Namenskontexte und Verzeichnis Partitionen AD
- Namenskontexte AD, Informationen zu
- Verzeichnis Partitionen AD, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39934f0236e927bff281230c41a303f5e6d2bb0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948556"
---
# <a name="naming-contexts-and-directory-partitions"></a>Benennungs Kontexte und Verzeichnis Partitionen

Jeder Domänen Controller in einer Domänen Gesamtstruktur, die von Active Directory Domain Services gesteuert wird, umfasst [*Verzeichnis Partitionen*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) Verzeichnis Partitionen werden auch als [*Namenskontexte*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85))bezeichnet. Eine Verzeichnis Partition ist ein zusammenhängender Teil des gesamten Verzeichnisses, der über einen unabhängigen Replikations Bereich und Zeit Planungsdaten verfügt. Standardmäßig enthält der Active Directory-Domäne-Dienst für ein Unternehmen die folgenden Partitionen:

-   [*Schema Partition*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85)): die Schema Partition enthält die **classSchema** -und **attributeSchema** -Objekte, die die Objekttypen definieren, die in der Gesamtstruktur vorhanden sein können. Jeder Domänen Controller in der Gesamtstruktur verfügt über ein Replikat derselben Schema Partition.
-   [*Konfigurations Partition*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85)): die Konfigurations Partition enthält Replikations Topologie und andere Konfigurationsdaten, die in der Gesamtstruktur repliziert werden müssen. Jeder Domänen Controller in der Gesamtstruktur verfügt über ein Replikat derselben Konfigurations Partition.
-   [*Domänen Partition*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)): die Domänen Partition enthält die Verzeichnisobjekte, z. b. Benutzer und Computer, die mit der lokalen Domäne verknüpft sind. Eine Domäne kann über mehrere Domänen Controller verfügen, und eine Gesamtstruktur kann mehrere Domänen aufweisen. Jeder Domänen Controller speichert ein vollständiges Replikat der Domänen Partition für seine lokale Domäne, speichert jedoch keine Replikate der Domänen Partitionen für andere Domänen.

Mit Windows Server 2003 wird die *Anwendungsverzeichnis Partition* eingeführt, die die Möglichkeit bietet, den Umfang der Replikation zu steuern und die Platzierung von Replikaten auf eine Weise zu ermöglichen, die für dynamische Daten besser geeignet ist. Weitere Informationen zu Anwendungsverzeichnis Partitionen finden Sie unter Informationen [zu Anwendungsverzeichnis Partitionen](about-application-directory-partitions.md).

Weitere Informationen dazu, wie Active Directory Domain Services die Konsistenz zwischen den verschiedenen Replikaten einer Verzeichnis Partition beibehalten, finden Sie unter [Replikation und Datenintegrität](replication-and-data-integrity.md).

 

 