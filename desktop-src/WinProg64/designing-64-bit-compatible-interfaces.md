---
title: Entwerfen von 64-Bit-kompatiblen Schnittstellen
description: Abwärts Kompatibilitätsprobleme treten auf, wenn Sie einer Schnittstelle neue Datentypen oder Methoden hinzufügen, alte Datentypen ändern oder Datentypen nicht ordnungsgemäß verwenden.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- Abwärtskompatibilität 64-Bit-Windows-Programmierung
- 64-Bit-kompatible Schnittstellen 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Kompatibilität
- Kompatibilität 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309947"
---
# <a name="designing-64-bit-compatible-interfaces"></a>Entwerfen von 64-Bit-kompatiblen Schnittstellen

Das Portieren von 32-Bit-Fenstern auf 64-Bit-Windows sollte keinerlei Probleme für verteilte Anwendungen verursachen, egal ob Sie Remote Prozedur Aufrufe (RPC) direkt oder über DCOM verwenden. Das RPC-Programmiermodell gibt wohl definierte Datengrößen und ganzzahlige Typen an, die an jedem Ende der Verbindung dieselbe Größe haben. Außerdem werden im LLP64 Abstract Data Model, das für 64-Bit-Windows entwickelt wurde, nur die Zeiger auf 64 Bits erweitert – alle anderen ganzzahligen Datentypen bleiben 32 Bits. Da Zeiger für jede Seite der Client/Server-Verbindung lokal sind und normalerweise als **null** -Marker oder nicht-**null** -Marker übertragen werden, kann das marshallingmodul verschiedene Zeiger Größen an jedem Ende einer Verbindung transparent verarbeiten.

Es treten jedoch abwärts Kompatibilitätsprobleme auf, wenn Sie einer Schnittstelle neue Datentypen oder Methoden hinzufügen, alte Datentypen ändern oder Datentypen nicht ordnungsgemäß verwenden. In den folgenden Themen wird erläutert, wie Sie diese Situationen vermeiden können (sofern möglich) und wie Sie robuste Problem Umgehungen entwerfen können, wenn es nicht möglich ist, Sie zu vermeiden.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Ändern einer vorhandenen Schnittstelle](changing-an-existing-interface.md)
-   [Vermeiden von Informationen ausblenden](avoiding-information-hiding.md)
-   [Vermeiden von Polymorphie](avoiding-polymorphism.md)
-   [Verwenden neuer Datentypen in ihrer IDL-Datei](using-new-data-types-in-your-idl-file.md)
-   [Vorbereiten der Anwendung für 64-Bit-Windows](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>Verwandte Abschnitte

Wenn Sie noch nicht mit den neuen Datentypen, der Arbeitsumgebung und den API-Änderungen für 64-Bit-Windows vertraut sind, finden Sie weitere Informationen unter [vorbereiten für 64-Bit-Windows](getting-ready-for-64-bit-windows.md).

 

 




