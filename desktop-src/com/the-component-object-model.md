---
title: Das Component Object Model
description: Das Component Object Model
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad81adeaf41670468dd41bbf344a3fd7358c14f4b3cbeb2e482812a083ecfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462340"
---
# <a name="the-component-object-model"></a>Das Component Object Model

Microsoft Component Object Model (COM) ist ein plattformunabhängiges, verteiltes, objektorientiertes System zum Erstellen binärer Softwarekomponenten, die interagieren können. COM ist die Grundlagetechnologie für OLE (Verbunddokumente), ActiveX (internetfähige Komponenten) von Microsoft und andere.

Um COM (und somit alle COM-basierten Technologien) zu verstehen, ist es wichtig zu verstehen, dass es sich nicht um eine objektorientierte Sprache, sondern um einen Standard handelt. Com gibt auch nicht an, wie eine Anwendung strukturiert werden soll. Sprach-, Struktur- und Implementierungsdetails bleiben dem Anwendungsentwickler erhalten. Stattdessen gibt COM ein Objektmodell und Programmieranforderungen an, die es COM-Objekten (auch als COM-Komponenten oder manchmal einfach als Objekte *bezeichnet)* ermöglichen, mit anderen Objekten zu interagieren. Diese Objekte können sich innerhalb eines einzelnen Prozesses, in anderen Prozessen und sogar auf Remotecomputern finden. Sie können in verschiedenen Sprachen geschrieben werden, und sie können strukturell recht unterschiedlich sein, weshalb COM als binärer Standard *bezeichnet wird.* Ein Standard, der angewendet wird, nachdem ein Programm in Binärcomputercode übersetzt wurde.

Die einzige Sprachanforderung für COM ist, dass Code in einer Sprache generiert wird, die Strukturen von Zeigern erstellen und Funktionen entweder explizit oder implizit über Zeiger aufrufen kann. Objektorientierte Sprachen wie C++ und Smalltalk bieten Programmiermechanismen, die die Implementierung von COM-Objekten vereinfachen, aber Sprachen wie C, Java und VBScript können zum Erstellen und Verwenden von COM-Objekten verwendet werden.

COM definiert die wesentliche Natur eines COM-Objekts. Im Allgemeinen besteht ein Softwareobjekt aus einem Satz von Daten und den Funktionen, die die Daten bearbeiten. Ein COM-Objekt ist ein Objekt, bei dem der Zugriff auf die Daten eines Objekts ausschließlich über eine oder mehrere Sätze verwandter Funktionen erfolgt. Diese Funktionssätze werden als *Schnittstellen bezeichnet,* und die Funktionen einer Schnittstelle werden als Methoden *bezeichnet.* Darüber hinaus erfordert COM, dass die einzige Möglichkeit, zugriff auf die Methoden einer Schnittstelle zu erhalten, über einen Zeiger auf die Schnittstelle ist.

Neben der Angabe des grundlegenden binären Objektstandards definiert COM bestimmte grundlegende Schnittstellen, die Funktionen bereitstellen, die allen COM-basierten Technologien gemeinsam sind, und stellt eine kleine Anzahl von Funktionen bereit, die alle Komponenten benötigen. COM definiert auch, wie Objekte in einer verteilten Umgebung zusammenarbeiten, und hat Sicherheitsfeatures hinzugefügt, um die System- und Komponentenintegrität zu gewährleisten.

In den folgenden Themen in diesem Abschnitt werden grundlegende COM-Probleme im Zusammenhang mit dem Entwerfen von COM-Objekten beschrieben:

-   [COM-Objekte und -Schnittstellen](com-objects-and-interfaces.md)
-   [Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
-   [Wiederverwendung von Objekten](reusing-objects.md)
-   [Die COM-Bibliothek](the-com-library.md)
-   [Verwalten der Speicherzuordnung](managing-memory-allocation.md)

 

 




