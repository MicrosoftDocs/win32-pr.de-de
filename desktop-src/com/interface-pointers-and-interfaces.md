---
title: Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)
description: Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abeb6040c2e55168fee1aa2c73db0056de557d0ddafaed6499e7da048dfc56de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854370"
---
# <a name="interface-pointers-and-interfaces"></a>Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)

Eine Instanz einer Schnittstellenimplementierungen ist tatsächlich ein Zeiger auf ein Array von Zeigern auf Methoden, d. h. eine Funktionstabelle, die auf eine Implementierung aller in der -Schnittstelle angegebenen Methoden verweist. Objekte mit mehreren Schnittstellen können Zeiger auf mehrere Funktionstabellen bereitstellen. Jeder Code, der über einen Zeiger verfügt, über den er auf das Array zugreifen kann, kann die Methoden in dieser Schnittstelle aufrufen.

Genau über diese mehrfache Dekonstruktion zu sprechen, ist unpraktisch. Stattdessen wird der Zeiger auf die Schnittstellenfunktionstabelle, die ein anderes Objekt zum Aufrufen seiner Methoden benötigen muss, einfach als *Schnittstellenzeiger* bezeichnet. Sie können Funktionstabellen manuell in einer C-Anwendung oder fast automatisch erstellen, indem Sie Visual C++ (oder andere objektorientierte Sprachen, die COM unterstützen) verwenden.

Bei entsprechender Compilerunterstützung (die in C und C++ inhärent ist) kann ein Client eine Schnittstellenmethode über seinen Namen und nicht über seine Position im Array aufrufen. Da es sich bei einer Schnittstelle um einen Typ handelt, kann der Compiler die Parametertypen und Rückgabewerte jedes Schnittstellenmethodenaufrufs anhand der Methodennamen überprüfen. Wenn ein Client dagegen ein positionsbasiertes Aufrufschema verwendet, ist eine solche Typüberprüfung selbst in C oder C++ nicht verfügbar.

Jede Schnittstelle ist ein unveränderlicher Vertrag einer Funktionsgruppe von Methoden. Sie verweisen zur Laufzeit mit einem global eindeutigen Schnittstellenbezeichner (GLOBALLY UNIQUE Interface Identifier, IID) auf eine Schnittstelle. Diese IID, eine bestimmte Instanz einer guid (Globally Unique Identifier), die von COM unterstützt wird, ermöglicht es einem Client, ein Objekt genau zu fragen, ob es die Semantik der Schnittstelle unterstützt, ohne unnötigen Aufwand und ohne die Verwirrung, die in einem System entstehen könnte, wenn mehrere Versionen derselben Schnittstelle mit dem gleichen Namen vorhanden sind.

Zusammenfassend ist es wichtig zu verstehen, was eine COM-Schnittstelle ist und nicht:

-   Eine COM-Schnittstelle ist nicht identisch mit einer C++-Klasse. Die reine virtuelle Definition enthält keine Implementierung. Wenn Sie C++-Programmierer sind, können Sie die Implementierung einer Schnittstelle als Klasse definieren. Dies fällt jedoch unter die Überschrift der Implementierungsdetails, die com nicht angibt. Eine Instanz eines Objekts, das eine Schnittstelle implementiert, muss erstellt werden, damit die Schnittstelle tatsächlich vorhanden ist. Darüber hinaus können verschiedene Objektklassen eine Schnittstelle implementieren, die jedoch synonym in binärer Form verwendet werden kann, solange das Verhalten der Schnittstellendefinition entspricht.
-   Eine COM-Schnittstelle ist kein Objekt. Es handelt sich einfach um eine verwandte Gruppe von Funktionen und ist der binäre Standard, über den Clients und Objekte kommunizieren. Solange sie Zeiger auf Schnittstellenmethoden bereitstellen kann, kann das Objekt in einer beliebigen Sprache mit einer beliebigen internen Zustandsdarstellung implementiert werden.
-   COM-Schnittstellen sind stark typisiert. Jede Schnittstelle verfügt über einen eigenen Schnittstellenbezeichner (GUID), wodurch die Möglichkeit der Duplizierung vermieden wird, die bei jedem anderen Benennungsschema auftreten kann.
-   COM-Schnittstellen sind unveränderlich. Sie können keine neue Version einer alten Schnittstelle definieren und ihr den gleichen Bezeichner geben. Durch das Hinzufügen oder Entfernen von Methoden einer Schnittstelle oder das Ändern der Semantik wird eine neue Schnittstelle erstellt, nicht eine neue Version einer alten Schnittstelle. Aus diesem Grund kann eine neue Schnittstelle keinen Konflikt mit einer alten Schnittstelle verursachen. Objekte können jedoch mehrere Schnittstellen gleichzeitig unterstützen und Schnittstellen verfügbar machen, die aufeinander folgende Revisionen einer Schnittstelle mit unterschiedlichen Bezeichnern sind. Daher ist jede Schnittstelle ein separater Vertrag, und systemweite Objekte müssen sich keine Gedanken darüber machen, ob die Version der Schnittstelle, die sie aufrufen, die erwartete Ist. Die Schnittstellen-ID (IID) definiert den Schnittstellenvertrag explizit und eindeutig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Objekte und -Schnittstellen](com-objects-and-interfaces.md)
</dt> </dl>

 

 




