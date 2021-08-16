---
title: Importieren von System-Headerdateien
description: Obwohl es häufig möglich ist, die \include-Anweisung zu verwenden, um Headerdateien in Ihre IDL-Datei einzufügen, wird dies nicht empfohlen.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- Importieren von MIDL- und Systemheaderdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070351ecd47b24d16d3baa2dde33b0199b02f4bf12e8ccc8f5628564a88dd6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383877"
---
# <a name="importing-system-header-files"></a>Importieren von System-Headerdateien

Obwohl es häufig möglich ist, die **\# include-Direktive** zu verwenden, um Headerdateien in Ihre IDL-Datei einzufügen, wird dies nicht empfohlen. Der MIDL-Compiler generiert Stubs für alle Funktionen, die in der zu kompilierenden IDL-Datei definiert sind. In der Regel enthält eine Headerdatei eine Reihe von Prototypen, die Sie weder benötigen noch in Ihre Stubdateien einschließen möchten, und ein **\# Include** fügt alle diese Definitionen effektiv in Ihre IDL-Hauptdatei ein. Wenn in der Headerdatei nicht benutzerdefinierte Typen definiert sind, wird die IDL-Datei möglicherweise nicht kompiliert.

Es gibt zwei Möglichkeiten, Typdefinitionen aus Headerdateien in eine IDL-Datei einzufügen:

-   Verwenden Sie die [**Importdirektive,**](import.md) um datentypen einzufügen, die in einer Headerdatei definiert sind. Im Gegensatz zur **\# C-Language Include-Direktive** greift die **Importdirektive** nur Typ- und Konstantendefinitionen auf und ignoriert Prozedurprototypen. Dieser Ansatz funktioniert, solange Ihre IDL-Hauptdatei nicht auf nicht bearbeitbare Typen verweist, die in der Headerdatei definiert sind.
-   Erstellen Sie eine Hilfs-IDL-Datei mit einer Dummyschnittstelle, die die Headerdateien enthält. Verwenden Sie dann die [**Importdirektive,**](import.md) um die Hilfsdatei einzufügen. Auf diese Weise werden nur die [**typedef-s**](typedef.md)in den kompilierten Stubs angezeigt. Beispiel:

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
