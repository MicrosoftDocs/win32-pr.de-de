---
description: Auf dieser Seite werden einige der Programmieraufgaben aufgeführt, die häufig mit der XPS-Dokument-API ausgeführt werden.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Allgemeine Aufgaben der XPS-Dokumentprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7f71614344968bcc68e658021e1f34296a595d9fbf58be2d544c03c3dc428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846350"
---
# <a name="common-xps-document-programming-tasks"></a>Allgemeine Aufgaben der XPS-Dokumentprogrammierung

Auf dieser Seite werden einige der Programmieraufgaben aufgeführt, die häufig mit der XPS-Dokument-API ausgeführt werden.

## <a name="common-xps-document-tasks"></a>Allgemeine XPS-Dokumentaufgaben

Die folgenden Codebeispiele veranschaulichen einige der Programmieraufgaben, die häufig ausgeführt werden, wenn die XPS-Dokument-API für die Arbeit mit einer XPS OM verwendet wird.

<dl>

[Initialisieren einer XPS OM](xps-object-model-initialization.md)  
[Erstellen eines leeren XPS OM](create-a-blank-xps-om.md)  
[Lesen eines XPS-Dokuments in eine XPS OM](read-an-xps-document-into-an-xps-om.md)  
[Navigieren im XPS OM](navigate-the-xps-om.md)  
[Schreiben von Text in eine XPS OM](write-text-to-an-xps-om.md)  
[Zeichnen von Grafiken in einer XPS OM](draw-graphics-in-an-xps-om.md)  
[Platzieren von Bildern in einer XPS OM](place-images-in-an-xps-om.md)  
[Schreiben einer XPS OM in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)  
[Drucken einer XPS OM](print-an-xps-om.md)  
[Arbeiten mit XPS OM-Sammlungsschnittstellen](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Haftungsausschluss

Codebeispiele sind nicht als vollständige und funktionierende Programme vorgesehen. Die Codebeispiele, auf die auf dieser Seite verwiesen wird, führen z. B. keine Parameterüberprüfung, Fehlerüberprüfung oder Fehlerbehandlung aus. Verwenden Sie diese Beispiele als Ausgangspunkt, und fügen Sie dann den Code hinzu, der zum Erstellen einer stabilen Anwendung erforderlich ist. Weitere Informationen zu **HRESULT-Rückgabewerten** und Fehlerbehandlungsstrategien finden Sie unter [Fehlerbehandlung in COM.](../com/error-handling-in-com.md)

Bevor XPS OM-Schnittstellen verwendet werden können, muss COM im Thread initialisiert werden, wie im folgenden Beispielcode gezeigt.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Aus Gründen der Übersichtlichkeit verwenden diese Codebeispiele eine sehr einfache XPS OM, die für Ihre Anwendung möglicherweise nicht komplex genug ist. In den Codebeispielen, die einer Seite Inhalt hinzufügen, werden die visuellen Elemente einer Seite direkt zur Liste der visuellen Objekte der Seite hinzugefügt. In der Praxis empfiehlt es sich jedoch, visuelle Objekte in Canvasobjekte zu gruppieren, sodass mehrere Objekte als Gruppe verwendet werden können. Um die Unterstützung desselben Inhalts für mehr als eine Seitengröße zu aktivieren, können Sie den visuellen Inhalt einer Seite in ein einzelnes Canvas-Objekt gruppieren und dann eine Transformation auf den Zeichenbereich anwenden, um ihn auf die aktuelle Seitengröße zu skalieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in COM](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
