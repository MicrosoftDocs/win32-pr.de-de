---
title: Zwischenspeichern des Ergebnisses (Client seitig)
description: Das Client seitige Zwischenspeichern speichert das Resultset im Client Speicher und bietet Leistungsverbesserungen für die Clientseite.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Zwischenspeichern des Ergebnisses (Client seitig) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947355"
---
# <a name="caching-the-result-client-side"></a>Zwischenspeichern des Ergebnisses (Client seitig)

Das Client seitige Zwischenspeichern speichert das Resultset im Client Speicher und bietet Leistungsverbesserungen für die Clientseite. Ein Client kann ein Objekt wiederholt ohne mehrere Fahrten zum Server erneut überprüfen. Standardmäßig speichert ADSI das Resultset für die Clients zwischen. Dadurch kann ADSI Clients die SQL-ähnliche Cursor Unterstützung bereitstellen. Sie können ein bestimmtes Resultset mehrmals durchlaufen.

Mit ADSI können Clients den Cache auch deaktivieren, um die Arbeitsspeicher Anforderungen zu reduzieren. Wenn das Client seitige Zwischenspeichern deaktiviert ist, behält der Client das Resultset nicht im Arbeitsspeicher. Jede Zeile wird freigegeben, nachdem Sie von der Anwendung abgerufen wurde. Die Deaktivierung der Client seitigen Zwischenspeicherung kann nützlich sein, um die Client seitigen Speicheranforderungen in Fällen zu verringern, in denen Sie nur einen einzigen Durchlauf durch das Resultset durchführen möchten. Wenn Clients das Ergebnis jedoch nicht zwischenspeichern, erhalten Sie Cursor Unterstützung.

Weitere Informationen zum Zwischenspeichern von Ergebnissen mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Ergebnis Zwischenspeicherung mit idirector ysearch](result-caching-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




