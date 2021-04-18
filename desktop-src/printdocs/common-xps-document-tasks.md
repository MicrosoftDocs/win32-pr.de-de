---
description: Auf dieser Seite werden einige der Programmieraufgaben aufgelistet, die häufig mit der XPS-Dokument-API ausgeführt werden.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Allgemeine XPS-Dokument Programmierungsaufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347352"
---
# <a name="common-xps-document-programming-tasks"></a>Allgemeine XPS-Dokument Programmierungsaufgaben

Auf dieser Seite werden einige der Programmieraufgaben aufgelistet, die häufig mit der XPS-Dokument-API ausgeführt werden.

## <a name="common-xps-document-tasks"></a>Allgemeine XPS-Dokument Aufgaben

Die folgenden Codebeispiele veranschaulichen einige der Programmieraufgaben, die häufig ausgeführt werden, wenn die XPS-Dokument-API zum Arbeiten mit einem XPS-OM verwendet wird.

<dl>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)  
[Erstellen eines leeren XPS-OMS](create-a-blank-xps-om.md)  
[Lesen eines XPS-Dokuments in ein XPS-OM](read-an-xps-document-into-an-xps-om.md)  
[Navigieren im XPS-OM](navigate-the-xps-om.md)  
[Schreiben von Text in ein XPS-OM](write-text-to-an-xps-om.md)  
[Zeichnen von Grafiken in einem XPS-OM](draw-graphics-in-an-xps-om.md)  
[Platzieren von Bildern in einem XPS-OM](place-images-in-an-xps-om.md)  
[Schreiben eines XPS-om in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)  
[Drucken eines XPS-OM](print-an-xps-om.md)  
[Arbeiten mit XPS OM-Sammlungs Schnittstellen](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Haftungsausschluss

Code Beispiele sind nicht als komplett und funktionierende Programme gedacht. In den Codebeispielen, die auf dieser Seite referenziert werden, wird z. b. keine Parameter Überprüfung, Fehlerüberprüfung oder Fehlerbehandlung durchgeführt. Verwenden Sie diese Beispiele als Ausgangspunkt, und fügen Sie dann den Code hinzu, der erforderlich ist, um eine robuste Anwendung zu erstellen. Weitere Informationen zu den **HRESULT** -Rückgabe Werten und Fehlerbehandlungsstrategien finden Sie unter [Fehlerbehandlung in com](../com/error-handling-in-com.md).

Bevor XPS OM-Schnittstellen verwendet werden können, muss com im Thread initialisiert werden, wie im folgenden Beispielcode gezeigt.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Aus Gründen der Übersichtlichkeit verwenden diese Codebeispiele ein sehr einfaches XPS-OM, das möglicherweise nicht komplex genug für Ihre Anwendung ist. In den Codebeispielen, die Inhalte zu einer Seite hinzufügen, werden die visuellen Elemente einer Seite in einem Fall direkt der Liste der visuellen Objekte der Seite hinzugefügt. in der Praxis möchten Sie jedoch möglicherweise visuelle Objekte in Canvas-Objekte gruppieren, sodass mehrere Objekte als Gruppe behandelt werden könnten. Um die Unterstützung desselben Inhalts für mehr als eine Seitengröße zu aktivieren, können Sie daher den visuellen Inhalt einer Seite in einem einzelnen Canvas-Objekt gruppieren und dann eine Transformation auf den Zeichenbereich anwenden, um ihn auf die aktuelle Seitengröße zu skalieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
