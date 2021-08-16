---
title: Zwischenspeichern des Ergebnisses (clientseitig)
description: Bei der clientseitigen Zwischenspeicherung wird das Ergebnis im Clientspeicher gespeichert, was zu Leistungsverbesserungen für die Clientseite führt.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Zwischenspeichern des Ergebnisses (clientseitiges) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2394c4f9e3213261bc52e15ada6fa9416703706fedeccaf144493821133e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840500"
---
# <a name="caching-the-result-client-side"></a>Zwischenspeichern des Ergebnisses (clientseitig)

Bei der clientseitigen Zwischenspeicherung wird das Ergebnis im Clientspeicher gespeichert, was zu Leistungsverbesserungen für die Clientseite führt. Ein Client kann ein Objekt wiederholt ohne mehrere Fahrten zum Server erneut besuchen. Standardmäßig speichert ADSI das Ergebnisset für die Clients zwischen. Dies ermöglicht ADSI, Clients eine SQL Cursorunterstützung zu bieten. Sie können ein bestimmtes Ergebnisset mehrmals durch iterieren.

ADSI ermöglicht Es Clients auch, den Cache zu deaktivieren, um den Arbeitsspeicherbedarf zu reduzieren. Wenn die clientseitige Zwischenspeicherung deaktiviert ist, verwaltet der Client das ResultSet nicht im Arbeitsspeicher. Jede Zeile wird nach dem Abrufen durch die Anwendung wieder frei. Das Deaktivieren der clientseitigen Zwischenspeicherung kann nützlich sein, um die clientseitigen Speicheranforderungen in Solchen Fällen zu verringern, in denen Sie nur einen einzelnen Pass durch das Resultset machen möchten. Wenn Clients das Ergebnis jedoch nicht zwischenspeichern, geben sie die Cursorunterstützung auf.

Weitere Informationen zum Zwischenspeichern von Ergebnissen mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Zwischenspeichern von Ergebnis mit IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




