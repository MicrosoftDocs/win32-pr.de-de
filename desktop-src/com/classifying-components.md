---
title: Klassifizierender Komponenten
description: Klassifizierender Komponenten
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856616"
---
# <a name="classifying-components"></a>Klassifizierender Komponenten

Während ein Client die Liste der CLSIDs in der Registrierung durchsuchen und eine zu verwendende Komponente auswählen kann, ist das Laden der einzelnen Komponenten in der Registrierung und das Abfragen für die unterstützten Schnittstellen sehr zeitaufwändig. Um zu bestimmen, ob eine Komponente die erforderlichen Schnittstellen vor dem Erstellen einer Instanz der Komponente unterstützt, wurde eine Methode zum Klassifizieren von Komponenten in Kategorien entwickelt.

Eine Komponenten Kategorie ist ein Satz von Schnittstellen, denen eine Guid namens CATID zugewiesen wurde. Komponenten, die alle Schnittstellen in einer Komponenten Kategorie implementieren, registrieren sich selbst als Mitglieder dieser Komponenten Kategorie. Komponenten, die zu einer bestimmten Komponenten Kategorie gehören, können dann aus der Registrierung ausgewählt werden. Wenn Sie sich selbst als Mitglied einer Komponenten Kategorie registrieren, gewährleistet die Komponente, dass Sie alle Member-Schnittstellen in der Komponenten Kategorie unterstützt.

Eine Komponente kann Mitglied vieler Kategorien sein. Es ist nicht auf die Unterstützung von Schnittstellen in einer Komponenten Kategorie beschränkt. Zusätzlich zu den Komponenten in einer Komponenten Kategorie kann Sie beliebige Schnittstellen unterstützen.

Im Gegensatz zur Standard Registrierung von-Komponenten, bei denen Entwickler Code schreiben müssen, mit dem-Objekte manuell registriert werden, werden in Komponenten Kategorien viele dieser Aufgaben automatisiert. Die sechs Methoden der [**itorregister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) -Schnittstelle definieren Komponenten Kategorien und registrieren Objekte, die Sie implementieren oder erfordern. Das [Komponenten Kategorien-Manager](the-component-categories-manager.md) -Objekt implementiert diese Schnittstelle. Weitere Informationen zur Verwendung von Komponenten Kategorien finden Sie unter **i-Register** und [**ikatinformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 




