---
description: BLOB-Komponenten
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: BLOB-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217174"
---
# <a name="blob-components"></a>BLOB-Komponenten

Ein Binary Large Object (BLOB) umfasst die folgenden hierarchischen Komponenten:

-   Besitzer
-   Kategorien
-   `Tags`
-   Werte

## <a name="textual-representation"></a>Textdarstellung

Aus praktischer Gründen werden blobdateien im Format owner: Category: Tag: value angezeigt, das Sie beim Speichern in einer Datei anzeigen. Die interne Struktur des BLOBs ist nicht transparent, da Sie Zeiger und Tabellen darstellt. Hier ist beispielsweise ein Eintrag aus einem BLOB, der zum Konfigurieren eines NPP verwendet werden kann:

``` syntax
NPP:Configure:BufferSize=32768
```

Der Besitzer ist NPP. Die Kategorie ist configure, das Tag ist bufferSize und der Wert 32768.

 

 



