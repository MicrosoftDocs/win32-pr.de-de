---
title: Abfrageschnittstellen
description: Zum Durchführen von Verzeichnis suchen können drei Typen von ADSI-Schnittstellen verwendet werden. Die Anwendungsumgebung und andere Anforderungen geben möglicherweise an, welche Schnittstelle verwendet wird.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Abfrageschnittstellen ADSI
- Abfragen von ADSI, Abfrageschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855260"
---
# <a name="query-interfaces"></a>Abfrageschnittstellen

Zum Durchführen von Verzeichnis suchen können drei Typen von ADSI-Schnittstellen verwendet werden. Die Anwendungsumgebung und andere Anforderungen geben möglicherweise an, welche Schnittstelle verwendet wird.

-   [**Idirectoriysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **Idirector ysearch** ist eine grundlegende COM-Schnittstelle, die nur für C/C++-Programmierer verfügbar ist. Weitere Informationen finden Sie unter [Suchen mit der idirector ysearch-Schnittstelle](searching-with-idirectorysearch.md).
-   ADOs. Die ADO-Schnittstellen (ActiveX Data Object) sind Automatisierungs Schnittstellen, die OLE DB verwenden. Verwenden Sie ADO für Abfragen in Anwendungen, die auf Automation basieren. Dazu zählen Visual Basic Anwendungen, Active Server Seiten usw. Weitere Informationen finden Sie unter [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB ist ein Satz von C/C++-Schnittstellen, mit denen Datenbanken abgefragt werden. Durch die Unterstützung dieser Schnittstellen können ADSI-Anbieter erweiterte OLE DB Features implementieren, z. b. verteilte Abfragen mit anderen OLE DB Anbietern. Weitere Informationen finden Sie unter [Suchen mit OLE DB](searching-with-ole-db.md).

 

 




