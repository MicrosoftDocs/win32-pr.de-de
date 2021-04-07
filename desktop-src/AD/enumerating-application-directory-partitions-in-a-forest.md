---
title: Auflisten von Anwendungsverzeichnis Partitionen in einer Gesamtstruktur
description: Ebenso wie Domänen Partitionen wird jede Anwendungsverzeichnis Partition durch ein CrossRef-Objekt im Partitions Container der Konfigurations Partition dargestellt.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Auflisten von Anwendungsverzeichnis Partitionen in einer Gesamtstruktur-AD
- Anwendungsverzeichnis Partitionen AD, Enumeration in einer Gesamtstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038761"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Auflisten von Anwendungsverzeichnis Partitionen in einer Gesamtstruktur

Ebenso wie Domänen Partitionen wird jede Anwendungsverzeichnis Partition durch ein [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt im Partitions Container der Konfigurations Partition dargestellt. Jedes **CrossRef** -Objekt speichert Daten über die entsprechende Partition.

Ein [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt, das eine Domänen Partition darstellt, wird von einem **CrossRef** -Objekt unterschieden, das eine Anwendungsverzeichnis Partition durch den Inhalt des [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attributs darstellt. Das **CrossRef** -Objekt, das eine Domänen Partition darstellt, verfügt über die [**AD- \_ Systemflag \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) -und **ADS \_ Systemflag \_ CR \_ NTDS- \_ Domänen** Kennzeichen, die im **systemFlags** -Attribut festgelegt sind. Für das **CrossRef** -Objekt, das eine Anwendungsverzeichnis Partition darstellt, wird das **AD \_ Systemflag \_ CR \_ NTDS \_ NC** -Flag festgelegt, und das **ADS \_ Systemflag \_ CR \_ NTDS- \_ domänenflag** wird im **systemFlags** -Attribut nicht festgelegt.

Für die [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekte, die die Schema-und Konfigurations Partitionen darstellen, wird auch das c#-Flag "hat [**ADS \_ Systemflag \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) " festgelegt, und das **AD- \_ Systemflag \_ CR \_ NTDS- \_ Domänen** Kennzeichen wird nicht im [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut festgelegt Dies erfordert, dass diese beiden **CrossRef** -Objekte durch den Inhalt des [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attributs unterschieden werden. Das **NCName** -Attribut für das **CrossRef** -Objekt, das den Schema Container darstellt, ist identisch mit dem **schemaNamingContext** -Attribut des RootDSE-Objekts. Ebenso ist das **NCName** -Attribut für das **CrossRef** -Objekt, das den Konfigurations Container darstellt, identisch mit dem **configurationNamingContext** -Attribut des RootDSE-Objekts.

**Führen Sie die folgenden Schritte aus, um alle Anwendungsverzeichnis Partitionen in einer Gesamtstruktur zu identifizieren:**

1.  Suchen Sie im Container Partitionen der Konfigurations Partition nach allen [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekten, oder zählen Sie diese auf.
2.  Wenn für ein [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt das [**ADS \_ Systemflag \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) -Flag nicht festgelegt ist oder das **ADS \_ Systemflag \_ CR \_ NTDS- \_ domänenflag** im [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut Wert festgelegt ist, schließen Sie das Objekt aus dem Resultset aus.
3.  Schließen Sie die Schema Partition aus dem Resultset aus, indem Sie das [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts mit dem **schemaNamingContext** -Attribut des RootDSE-Objekts vergleichen.
4.  Schließen Sie die Konfigurations Partition aus dem Resultset aus, indem Sie das [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts mit dem **configurationNamingContext** -Attribut des RootDSE-Objekts vergleichen.
5.  Die restlichen [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekte im Resultset repräsentieren alle Anwendungsverzeichnis Partitionen.

 

 