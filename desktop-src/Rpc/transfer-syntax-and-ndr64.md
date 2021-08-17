---
title: Übertragungssyntax und NDR64
description: Das NDR-Wire Protocol, auch als Übertragungssyntax bezeichnet, ermöglicht RPC-Aufrufen das Durchlaufen des Netzwerks.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433e68689ec4c960adbb43ddc19ec3e9e37765db57cfe6bf87c86c096720b771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011228"
---
# <a name="transfer-syntax-and-ndr64"></a>Übertragungssyntax und NDR64

Das NDR-Wire Protocol, auch als Übertragungssyntax bezeichnet, ermöglicht RPC-Aufrufen das Durchlaufen des Netzwerks. Das Wire Protocol definiert die Wire-Darstellung eines RPC-Aufrufs, z. B. die Reihenfolge, in der Datenmitglieder gemarshallt werden, die Ausrichtung der Daten im Netzwerk, zusätzliche Informationen, die in den Daten enthalten sind, und andere Probleme. Das NDR64-Protokoll ist eine Erweiterung der 32-Bit-basierten NDR-Übertragungssyntax, die speziell entwickelt wurde, um Entwicklern, die auf 64-Bit-Systeme abzielen, eine optimierte Leistung zu ermöglichen.

Die Unterschiede zwischen dem NDR-Kabelformat und dem NDR64-Kabelformat beheben die unterschiedliche Größe von Zeigern in einer 64-Bit-Umgebung sowie andere Probleme. Die Mechanismen von NDR64 werden von RPC verarbeitet. Entwickler müssen nur den MIDL-Befehlszeilenschalter [**/protocol**](/windows/desktop/Midl/-protocol) verwenden, um die Vorteile von NDR64 auf 64-Bit-Plattformen zu nutzen. NDR64 ist nur auf 64-Bit-Plattformen verfügbar.

 

 