---
description: BLOB-Komponenten
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: BLOB-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bd9ab8389cdd49a266855106891a91fcfbd0b4f69c7d22b5855143b34f376c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367482"
---
# <a name="blob-components"></a>BLOB-Komponenten

Ein Blob (Binary Large Object) umfasst die folgenden hierarchischen Komponenten:

-   Besitzer
-   Kategorien
-   `Tags`
-   Werte

## <a name="textual-representation"></a>Textdarstellung

Der Einfachheit halber werden BLOBs im Format Owner:Category:Tag:Value angezeigt, in dem sie angezeigt werden, wenn sie in einer Datei gespeichert werden. Die interne Struktur des BLOB ist nicht transparent, da es Zeiger und Tabellen darstellt. Hier sehen Sie beispielsweise einen Eintrag aus einem BLOB, der zum Konfigurieren eines NPP verwendet werden kann:

``` syntax
NPP:Configure:BufferSize=32768
```

Der Besitzer ist NPP. Die Kategorie ist "Configure", das Tag "BufferSize" und der Wert "32768".

 

 



