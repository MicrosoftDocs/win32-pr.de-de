---
title: Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)
description: Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa23d53f529c43fa7529d657108cc75cb6a23b15
ms.sourcegitcommit: d482e4276cc06515e9fade2f253a257ffc418ce5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2019
ms.locfileid: "106337545"
---
# <a name="interface-pointers-and-interfaces"></a>Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)

Eine Instanz einer Schnittstellen Implementierung ist tatsächlich ein Zeiger auf ein Array von Zeigern auf Methoden, d. h. eine Funktions Tabelle, die auf eine Implementierung aller Methoden verweist, die in der-Schnittstelle angegeben sind. Objekte mit mehreren Schnittstellen können Zeiger auf mehr als eine Funktions Tabelle bereitstellen. Jeder Code, der über einen Zeiger verfügt, über den er auf das Array zugreifen kann, kann die Methoden in dieser Schnittstelle aufrufen.

Genau diese mehrfache Dereferenzierung ist unpraktisch, daher wird der Zeiger auf die Schnittstellen Funktions Tabelle, die ein anderes Objekt zum Aufrufen seiner Methoden benötigen muss, einfach als *Schnittstellen Zeiger* bezeichnet. Sie können Funktionstabellen in einer C-Anwendung oder fast automatisch mithilfe von Visual C++ (oder anderen objektorientierten Sprachen, die com unterstützen) manuell erstellen.

Mit der entsprechenden Compilerunterstützung (die in C und C++ verankert ist) kann ein Client eine Schnittstellen Methode über den Namen, nicht die Position im Array, abrufen. Da es sich bei einer Schnittstelle um einen-Typ handelt, kann der Compiler die Typen von Parametern und Rückgabewerte für die einzelnen Schnittstellen Methodenaufrufe überprüfen. Wenn ein Client dagegen ein Positions basiertes Aufruf Schema verwendet, ist diese Typüberprüfung auch in C oder C++ nicht verfügbar.

Jede Schnittstelle ist ein unveränderlicher Vertrag einer funktionalen Gruppe von Methoden. Sie verweisen zur Laufzeit auf eine Schnittstelle mit einer global eindeutigen Schnittstellen-ID (IID). Diese IID, bei der es sich um eine bestimmte Instanz einer von com unterstützten Globally Unique Identifier (GUID) handelt, ermöglicht einem Client, ein Objekt genau anzufordern, unabhängig davon, ob es die Semantik der Schnittstelle unterstützt, ohne unnötige Aufwand und ohne die Verwirrung, die in einem System aufgrund der Verwendung mehrerer Versionen derselben Schnittstelle mit dem gleichen Namen auftreten könnte.

Zusammenfassend ist es wichtig, zu verstehen, was eine COM-Schnittstelle ist, und ist nicht:

-   Eine COM-Schnittstelle ist nicht mit einer C++-Klasse identisch. Die rein virtuelle Definition enthält keine Implementierung. Wenn Sie ein C++-Programmierer sind, können Sie die Implementierung einer Schnittstelle als Klasse definieren. Dies liegt jedoch unter der Überschrift der Implementierungsdetails, die com nicht angibt. Eine Instanz eines Objekts, das eine Schnittstelle implementiert, muss erstellt werden, damit die Schnittstelle tatsächlich vorhanden ist. Darüber hinaus können unterschiedliche Objektklassen eine Schnittstelle anders implementieren, aber Sie können in Binär Form austauschbar verwendet werden, solange das Verhalten der Schnittstellen Definition entspricht.
-   Eine COM-Schnittstelle ist kein Objekt. Es handelt sich einfach um eine verwandte Gruppe von Funktionen und ist der binäre Standard, über den Clients und Objekte kommunizieren. Solange Sie Zeiger auf Schnittstellen Methoden bereitstellen kann, kann das Objekt in jeder beliebigen Sprache mit einer beliebigen internen Zustands Darstellung implementiert werden.
-   COM-Schnittstellen sind stark typisiert. Jede Schnittstelle verfügt über eine eigene Schnittstellen-ID (eine GUID), die die Möglichkeit der Duplizierung überflüssig macht, die mit einem anderen Benennungs Schema auftreten könnte.
-   COM-Schnittstellen sind unveränderlich. Sie können keine neue Version einer alten Schnittstelle definieren und Ihr denselben Bezeichner zuordnen. Durch das Hinzufügen oder Entfernen von Methoden einer Schnittstelle oder das Ändern der Semantik wird eine neue Schnittstelle erstellt, nicht die neue Version einer alten Schnittstelle. Daher kann eine neue Schnittstelle nicht mit einer alten Schnittstelle in Konflikt stehen. Allerdings können-Objekte mehrere Schnittstellen gleichzeitig unterstützen und Schnittstellen verfügbar machen, die aufeinander folgende Revisionen einer Schnittstelle mit unterschiedlichen bezeichlern sind. Folglich ist jede Schnittstelle ein separater Vertrag, und systemweite Objekte müssen nicht darauf achten, ob die Version der Schnittstelle, die Sie aufrufen, die erwartete Version der Schnittstelle ist. Die Schnittstellen-ID (IID) definiert den Schnittstellen Vertrag explizit und eindeutig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Objekte und-Schnittstellen](com-objects-and-interfaces.md)
</dt> </dl>

 

 




