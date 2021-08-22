---
title: Übersetzen der COM-Objektsyntax für Programmiersprachen
description: Übersetzen der COM-Objektsyntax für Programmiersprachen
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6871046a80537dd39b4c9b502d945e28e46e719e637c4e6a629179dd3c6454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500080"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Übersetzen der COM-Objektsyntax für Programmiersprachen

Um ein COM-Objekt aus einer Anwendung aufzurufen, die in einer anderen Programmiersprache als der Programmiersprache geschrieben wurde, die zum Schreiben des COM-Objekts verwendet wurde, müssen Sie zuerst die Syntax des Objekts in Ihre Programmiersprache übersetzen. Führen Sie hierzu die folgenden Schritte aus:

1.  Zeigen Sie die Typbibliothek des COM-Objekts in der Syntax Ihrer Programmiersprache an. Dadurch erhalten Sie Beschreibungen der Klassen, Schnittstellen, Methoden, Eigenschaften und Ereignisse des Objekts in der verwendeten Sprachsyntax.

    Microsoft-Entwicklerprodukte bieten mehrere Tools, die Sie beim Anzeigen und Konvertieren von Typbibliotheken unterstützen. Weitere Informationen finden Sie unter [Type Library Viewers and Conversion Tools (Typbibliotheks-Viewer und Konvertierungstools)](type-library-viewers-and-conversion-tools.md) und [How Entwicklertools Use Type Libraries (Verwenden von Typbibliotheken).](how-developer-tools-use-type-libraries.md)

    Sobald Sie die Typbibliothek des Objekts in Ihrer bevorzugten Programmiersprache anzeigen können, können Sie dessen Syntax mit der Syntax in der Dokumentation für das Objekt vergleichen. Wenn das Objekt in einer anderen Programmiersprache als der verwendeten dokumentiert ist, können sich die Datentypen und die Syntax unterscheiden. Beschreibungen von Parametern, Rückgabewerten und Funktionen des Objekts sollten jedoch identisch sein.

2.  Berücksichtigen Sie alle besonderen Überlegungen bei der Übersetzung in Ihre Programmiersprache.

    Da jede Programmiersprache Konzepte definiert, die in anderen Sprachen möglicherweise keine Entsprechung aufweisen, funktioniert ein Teil der Funktionalität eines Objekts in einer anderen Sprache möglicherweise anders oder ist überhaupt nicht verfügbar. Beispielsweise erkennt die Visual Basic Programmiersprache keine C++-Datentypen ohne Vorzeichen, z. B. **unsignedâ long**. Eine in Visual Basic geschriebene Anwendung kann keine COM-Methoden verwenden, die Variablen vom Datentyp ohne Vorzeichen akzeptieren oder zurückgeben.

3.  Fügen Sie dem Projekt den kompilierten Code des COM-Objekts hinzu. Der kompilierte Code ist in der Regel in einer .dll- oder OCX-Datei enthalten. Dieser Schritt ist erforderlich, damit der Compiler die Klassen des COM-Objekts erkennt. Nachdem Sie das COM-Objekt hinzugefügt haben, kann Ihre Anwendung ihre Klassen und Schnittstellen verwenden.

In den folgenden Themen wird beschrieben, wie COM-Objekte in einer Vielzahl von Programmiersprachen übersetzt und verwendet werden:

-   [Übersetzen in C++](translating-to-c--.md)
-   [Übersetzen in Visual Basic](translating-to-visual-basic.md)
-   [Übersetzen in Java](translating-to-java.md)

In diesen Themen werden Konvertierungstools und -prozesse beschrieben, die von Microsoft-Entwicklerprodukten bereitgestellt werden. Anweisungen zum Programmieren von COM-Objekten mit entwicklungstools, die von anderen Unternehmen erstellt wurden, finden Sie in der Dokumentation zu diesen Entwicklungstools.

 

 




