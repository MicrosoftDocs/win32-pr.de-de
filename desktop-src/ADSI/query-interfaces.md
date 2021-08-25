---
title: Abfrageschnittstellen
description: Für Verzeichnissuchen können drei Arten von ADSI-Schnittstellen verwendet werden. Die Anwendungsumgebung und andere Anforderungen können angeben, welche Schnittstelle verwendet wird.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Abfrageschnittstellen ADSI
- Abfragen ADSI , Abfrageschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637720"
---
# <a name="query-interfaces"></a>Abfrageschnittstellen

Für Verzeichnissuchen können drei Arten von ADSI-Schnittstellen verwendet werden. Die Anwendungsumgebung und andere Anforderungen können angeben, welche Schnittstelle verwendet wird.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** ist eine einfache COM-Schnittstelle, die nur für C/C++-Programmierer verfügbar ist. Weitere Informationen finden Sie unter [Suchen mit der IDirectorySearch-Schnittstelle.](searching-with-idirectorysearch.md)
-   Ado. Die ADO-Schnittstellen (ActiveX Data Object) sind Automatisierungsschnittstellen, die OLE DB verwenden. Verwenden Sie ADO für Abfragen in Anwendungen, die auf Automation basieren. Dazu gehören Visual Basic Anwendungen, Active Server Pages usw. Weitere Informationen finden Sie unter [Suchen mit ActiveX Datenobjekten.](searching-with-activex-data-objects-ado.md)
-   OLE DB. OLE DB besteht aus einer Reihe von C/C++-Schnittstellen, die zum Abfragen von Datenbanken verwendet werden. Durch die Unterstützung dieser Schnittstellen können ADSI-Anbieter erweiterte OLE DB Features implementieren, z. B. verteilte Abfragen mit anderen OLE DB Anbietern. Weitere Informationen finden Sie unter [Suchen mit OLE DB](searching-with-ole-db.md).

 

 




