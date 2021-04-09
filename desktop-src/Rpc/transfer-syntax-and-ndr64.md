---
title: Übertragungs Syntax und NDR64
description: Das NDR Wire Protocol, auch als Übertragungs Syntax bezeichnet, ermöglicht RPC-aufrufen, das Netzwerk zu durchlaufen.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039027"
---
# <a name="transfer-syntax-and-ndr64"></a>Übertragungs Syntax und NDR64

Das NDR Wire Protocol, auch als Übertragungs Syntax bezeichnet, ermöglicht RPC-aufrufen, das Netzwerk zu durchlaufen. Das Wire-Protokoll definiert die Netzwerkdarstellung eines RPC-Aufrufs, z. b. die Reihenfolge, in der Datenmember gemarshallt werden, die Ausrichtung der Daten im Netzwerk, zusätzliche Informationen, die in den Daten enthalten sind, und andere Probleme. Das NDR64-Protokoll ist eine Erweiterung der 32-Bit-basierten NDR-Übertragungs Syntax, die speziell erstellt wird, damit Entwickler, die auf 64-Bit-Systeme abzielen, eine optimierte Leistung erzielen können.

Die Unterschiede zwischen dem NDR-Wire-Format und dem NDR64 Wire-Format adressieren die unterschiedliche Größe von Zeigern in einer 64-Bit-Umgebung sowie andere Probleme. Die NDR64-Mechanismen werden von RPC behandelt. Entwickler müssen nur die Befehlszeilenoption/[**Protocol**](/windows/desktop/Midl/-protocol)**all** Mittel l verwenden, um die Vorteile von NDR64 auf 64-Bit-Plattformen zu erhalten. NDR64 ist nur auf 64-Bit-Plattformen verfügbar.

 

 