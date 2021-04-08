---
title: Das Component Object Model
description: Das Component Object Model
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708039"
---
# <a name="the-component-object-model"></a>Das Component Object Model

Das Microsoft Component Object Model (com) ist ein plattformunabhängiges, verteiltes, objektorientiertes System zum Erstellen von binären Softwarekomponenten, die interagieren können. COM ist die Grundtechnologie für OLE (Verbund Dokumente) von Microsoft, ActiveX (Internet fähige Komponenten) und andere.

Um com (und damit alle COM-basierten Technologien) zu verstehen, ist es wichtig zu verstehen, dass es sich nicht um eine objektorientierte Sprache, sondern um einen Standard handelt. Und com gibt nicht an, wie eine Anwendung strukturiert werden soll. die Details der Sprache, Struktur und Implementierung bleiben dem Anwendungsentwickler überlassen. Stattdessen gibt com ein Objektmodell und Programmier Anforderungen an, die COM-Objekte (auch com-Komponenten genannt oder manchmal *einfach)* zum interagieren mit anderen Objekten aktivieren. Diese Objekte können sich innerhalb eines einzelnen Prozesses, in anderen Prozessen und sogar auf Remote Computern befinden. Sie können in verschiedenen Sprachen geschrieben werden und sind möglicherweise strukturell sehr verschieden, weshalb com als *binärer Standard* bezeichnet wird. ein Standard, der angewendet wird, nachdem ein Programm in Binär Computercode übersetzt wurde.

Die einzige sprach Anforderung für com besteht darin, dass Code in einer Sprache generiert wird, die Struktur von Zeigern erstellen kann, und entweder explizit oder implizit Funktionen mithilfe von Zeigern aufruft. Objektorientierte Sprachen wie C++ und Smalltalk bieten Programmier Mechanismen, die die Implementierung von COM-Objekten vereinfachen, aber Sprachen wie C, Java und VBScript können zum Erstellen und Verwenden von COM-Objekten verwendet werden.

Com definiert die wesentliche Natur eines COM-Objekts. Im Allgemeinen besteht ein Software Objekt aus einem Satz von Daten und den Funktionen, die die Daten bearbeiten. Ein COM-Objekt ist ein Objekt, in dem der Zugriff auf die Daten eines Objekts ausschließlich über eine oder mehrere Sätze verwandter Funktionen erzielt wird. Diese Funktions Sätze werden als *Schnittstellen* bezeichnet, und die Funktionen einer Schnittstelle werden als *Methoden* bezeichnet. Außerdem erfordert com, dass die einzige Möglichkeit zum Zugriff auf die Methoden einer Schnittstelle über einen Zeiger auf die-Schnittstelle ist.

Abgesehen von der Angabe des standardmäßigen Binär Objekt Standards definiert com bestimmte grundlegende Schnittstellen, die Funktionen bereitstellen, die allen COM-basierten Technologien gemeinsam sind, und bietet eine kleine Anzahl von Funktionen, die für alle Komponenten erforderlich sind. COM definiert auch, wie Objekte über eine verteilte Umgebung zusammenarbeiten, und verfügt über zusätzliche Sicherheitsfunktionen, die zur Bereitstellung der System-und Komponenten Integrität beitragen.

Die folgenden Themen in diesem Abschnitt beschreiben grundlegende com-Probleme im Zusammenhang mit dem Entwerfen von COM-Objekten:

-   [COM-Objekte und-Schnittstellen](com-objects-and-interfaces.md)
-   [Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
-   [Wieder verwenden von Objekten](reusing-objects.md)
-   [Die com-Bibliothek](the-com-library.md)
-   [Verwalten der Speicher Belegung](managing-memory-allocation.md)

 

 




