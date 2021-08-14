---
title: Auflisten von Anwendungsverzeichnispartitionen in einer Gesamtstruktur
description: Wie Domänenpartitionen wird jede Anwendungsverzeichnispartition durch ein crossRef-Objekt im Partitionscontainer der Konfigurationspartition dargestellt.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Auflisten von Anwendungsverzeichnispartitionen in einer Gesamtstruktur-AD
- Anwendungsverzeichnispartitionen AD , Auflisten in einer Gesamtstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e8d48b2fc93ad7a879f76f2bbaa130186706ef957320612c866cb3b9f892c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191367"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Auflisten von Anwendungsverzeichnispartitionen in einer Gesamtstruktur

Wie Domänenpartitionen wird jede Anwendungsverzeichnispartition durch ein [**crossRef-Objekt**](/windows/desktop/ADSchema/c-crossref) im Partitionscontainer der Konfigurationspartition dargestellt. Jedes **crossRef-Objekt** speichert Daten über die entsprechende Partition.

Ein [**crossRef-Objekt,**](/windows/desktop/ADSchema/c-crossref) das eine Domänenpartition darstellt, unterscheidet sich von einem **crossRef-Objekt,** das eine Anwendungsverzeichnispartition durch den Inhalt des [**systemFlags-Attributs**](/windows/desktop/ADSchema/a-systemflags) darstellt. Für das **crossRef-Objekt,** das eine Domänenpartition darstellt, sind sowohl die [**\_ \_ \_ NTDS \_ NC-Flags ADS SYSTEMFLAG CR**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) als auch ADS **\_ SYSTEMFLAG CR NTDS DOMAIN im systemFlags-Attribut \_ \_ \_** festgelegt.  Für das **crossRef-Objekt,** das eine Anwendungsverzeichnispartition darstellt, ist das **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC-Flag** festgelegt, und das **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ DOMAIN-Flag** wird nicht im **systemFlags-Attribut** festgelegt.

Für die [**crossRef-Objekte,**](/windows/desktop/ADSchema/c-crossref) die die Schema- und Konfigurationspartitionen darstellen, ist auch das [**\_ \_ \_ NTDS \_ NC-Flag ADS SYSTEMFLAG CR**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) festgelegt, und das **\_ \_ \_ NTDS \_ DOMAIN-Flag ADS SYSTEMFLAG CR** wird nicht im [**systemFlags-Attribut**](/windows/desktop/ADSchema/a-systemflags) festgelegt. Dies erfordert, dass diese beiden **crossRef-Objekte** durch den Inhalt des [**nCName-Attributs**](/windows/desktop/ADSchema/a-ncname) unterschieden werden. Das **nCName-Attribut** für das **crossRef-Objekt,** das den Schemacontainer darstellt, ist mit dem **schemaNamingContext-Attribut** des RootDSE-Objekts identisch. Ebenso ist das **nCName-Attribut** für das **crossRef-Objekt,** das den Configuration-Container darstellt, mit dem **configurationNamingContext-Attribut** des RootDSE-Objekts identisch.

**Führen Sie die folgenden Schritte aus, um alle Anwendungsverzeichnispartitionen in einer Gesamtstruktur zu identifizieren.**

1.  Suchen Sie im Container Partitionen der Konfigurationspartition nach allen [**crossRef-Objekten,**](/windows/desktop/ADSchema/c-crossref) oder enumerationen Sie sie auf.
2.  Wenn für ein [**crossRef-Objekt**](/windows/desktop/ADSchema/c-crossref) das [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC-Flag**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) nicht festgelegt ist oder das NTDS DOMAIN-Flag ADS SYSTEMFLAG CR im [**systemFlags-Attributwert**](/windows/desktop/ADSchema/a-systemflags) festgelegt ist, schließen Sie das Objekt aus dem Resultset aus. **\_ \_ \_ \_**
3.  Schließen Sie die Schemapartition aus dem Resultset aus, indem Sie das [**nCName-Attribut**](/windows/desktop/ADSchema/a-ncname) des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) mit dem **schemaNamingContext-Attribut** des RootDSE-Objekts vergleichen.
4.  Schließen Sie die Configuration-Partition aus dem Resultset aus, indem Sie das [**nCName-Attribut**](/windows/desktop/ADSchema/a-ncname) des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) mit dem **configurationNamingContext-Attribut** des RootDSE-Objekts vergleichen.
5.  Die verbleibenden [**crossRef-Objekte**](/windows/desktop/ADSchema/c-crossref) im Resultset stellen alle Anwendungsverzeichnispartitionen dar.

 

 