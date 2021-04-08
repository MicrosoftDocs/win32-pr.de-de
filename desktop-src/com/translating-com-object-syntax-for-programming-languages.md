---
title: Übersetzen der COM-Objekt Syntax für Programmiersprachen
description: Übersetzen der COM-Objekt Syntax für Programmiersprachen
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855999"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Übersetzen der COM-Objekt Syntax für Programmiersprachen

Zum Abrufen eines COM-Objekts aus einer Anwendung, die in einer anderen Programmiersprache als der verwendet wird, um das COM-Objekt zu schreiben, müssen Sie zuerst die Syntax des Objekts in Ihre Programmiersprache übersetzen. Führen Sie hierzu die folgenden Schritte aus:

1.  Zeigen Sie die Typbibliothek des COM-Objekts in der Syntax der Programmiersprache an. Dadurch erhalten Sie Beschreibungen der Klassen, Schnittstellen, Methoden, Eigenschaften und Ereignisse des Objekts in der verwendeten Sprachsyntax.

    Microsoft-Entwickler Produkte bieten verschiedene Tools, die Sie beim Anzeigen und Umrechnen von Typbibliotheken unterstützen. Weitere Informationen finden Sie unter [Typbibliotheks-Viewer und-Konvertierungs Tools](type-library-viewers-and-conversion-tools.md) und [Entwicklertools Verwenden von Typbibliotheken](how-developer-tools-use-type-libraries.md).

    Wenn Sie die Typbibliothek des Objekts in Ihrer bevorzugten Programmiersprache anzeigen können, können Sie die zugehörige Syntax mit der in der Dokumentation für das Objekt vergleichen. Wenn das Objekt in einer anderen Programmiersprache als der von Ihnen verwendeten Programmiersprache dokumentiert ist, können die Datentypen und die Syntax abweichen, aber die Beschreibungen der Parameter, Rückgabewerte und die Funktionalität des Objekts sollten identisch sein.

2.  Berücksichtigen Sie besondere Überlegungen für die Übersetzung in Ihre Programmiersprache.

    Da jede Programmiersprache Konzepte definiert, die möglicherweise in anderen Sprachen nicht gleichwertig sind, können einige Funktionen eines Objekts in einer anderen Sprache unterschiedlich funktionieren oder überhaupt nicht verfügbar sein. Beispielsweise erkennt die Programmiersprache Visual Basic nicht signierte C++-Datentypen, wie z. b. **"unsignedLong"**. Eine in Visual Basic geschriebene Anwendung kann keine com-Methoden verwenden, die nicht signierte Datentyp Variablen akzeptieren oder zurückgeben.

3.  Fügen Sie dem Projekt den kompilierten Code des COM-Objekts hinzu. Der kompilierte Code ist in der Regel in einer DLL-oder OCX-Datei enthalten. Dieser Schritt ist erforderlich, damit der Compiler die Klassen des COM-Objekts erkennen kann. Nachdem Sie das COM-Objekt hinzugefügt haben, kann die Anwendung seine Klassen und Schnittstellen verwenden.

In den folgenden Themen wird beschrieben, wie COM-Objekte in einer Vielzahl von Programmiersprachen übersetzt und verwendet werden:

-   [Übersetzen in C++](translating-to-c--.md)
-   [Übersetzen in Visual Basic](translating-to-visual-basic.md)
-   [Übersetzen in Java](translating-to-java.md)

In diesen Themen werden die Konvertierungs Tools und-Prozesse beschrieben, die von Microsoft-Entwickler Produkten Anweisungen zum Programmieren von COM-Objekten mit von anderen Unternehmen erstellten Entwicklungs Tools finden Sie in der Dokumentation der Entwicklungs Tools.

 

 




