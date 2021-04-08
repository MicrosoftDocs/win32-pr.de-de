---
title: Importieren von System-Headerdateien
description: Obwohl es häufig möglich ist, die \ include-Direktive zum Einschließen von Header Dateien in Ihre IDL-Datei zu verwenden, wird dies nicht empfohlen.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- Importieren von mittlerer l-, System Header Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761589"
---
# <a name="importing-system-header-files"></a>Importieren von System-Headerdateien

Obwohl es häufig möglich ist, die **\# include** -Direktive zum Einschließen von Header Dateien in Ihre IDL-Datei zu verwenden, wird dies nicht empfohlen. Der mittlerer l-Compiler generiert stubvorgänge für alle Funktionen, die in der zu kompilierende IDL-Datei definiert sind. In der Regel enthält eine Header Datei eine Reihe von Prototypen, die Sie weder benötigen noch in die Stubdateien einschließen möchten, und ein **\# include** -Element fügt diese Definitionen effektiv in Ihre Haupt-IDL-Datei ein. Wenn außerdem nicht Remote fähige Typen in der Header Datei definiert sind, wird die IDL-Datei möglicherweise nicht kompiliert.

Es gibt zwei Möglichkeiten, Typdefinitionen aus Header Dateien in eine IDL-Datei einzubeziehen:

-   Verwenden Sie die [**Import**](import.md) -Direktive, um in eine Header Datei definierte Datentypen einzubeziehen. Anders als bei der **\# include** -Direktive der C-Sprache übernimmt die **Import** -Direktive nur den Typ und die Konstanten Definitionen und ignoriert Prozedur Prototypen. Diese Vorgehensweise funktioniert, solange die IDL-Hauptdatei nicht auf nicht Remote fähige Typen verweist, die in der Header Datei definiert sind.
-   Erstellen Sie eine IDL-Hilfsdatei mit einer Dummy-Schnittstelle, die die Header Dateien einschließt. Verwenden Sie dann die [**Import**](import.md) -Direktive, um die Hilfsdatei einzuschließen. Auf diese Weise werden nur die [**typedef**](typedef.md)s in den kompilierten Stub angezeigt. Beispiel:

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
