---
title: JAVATLB-Command-Line Tool
description: JAVATLB-Command-Line Tool
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714429"
---
# <a name="javatlb-command-line-tool"></a>JAVATLB-Command-Line Tool

JAVATLB ist eine Komponente von Visual J++ 5,0. JAVATLB ist eine Befehlszeilen Anwendung, die Klassendateien für ein COM-Objekt generiert. Methoden, die Datentypen enthalten, die nicht präzise und sicher in Java dargestellt werden können, werden nicht konvertiert.

Im Gegensatz zum Assistenten für die [Java-Typbibliothek](java-type-library-wizard.md)generiert JAVATLB keine Zusammenfassungs Datei mit den Informationen der Java-Typbibliothek.

Zum Generieren von Java-Klassendateien für ein einzelnes COM-Objekt führen Sie in der Eingabeaufforderung Folgendes aus:

**JAVATLB** - *Dateiname*

wobei *filename* der Name der Datei ist, die die Typbibliothek enthält. Diese Datei kann eine der folgenden Dateinamen Erweiterungen aufweisen: ". tlb", ". olb", ". ocx", ". dll" oder ". exe".

Um Java-Klassendateien für mehrere COM-Objekte zu generieren, führen Sie über die Eingabeaufforderung Folgendes aus:

**JAVATLB @ * * * Textdatei*

Dabei ist *Textfile* der Name einer Textdatei, die eine Liste der Dateien enthält, die die Typbibliotheken des COM-Objekts enthalten.

> [!Note]  
> In Visual J++ 6,0 wird das Befehlszeilen Tool JAVATLB durch das [Tool JActiveX](jactivex-command-line-tool.md)ersetzt. Weitere Informationen finden Sie in der Dokumentation zu Visual J++ 6,0.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




