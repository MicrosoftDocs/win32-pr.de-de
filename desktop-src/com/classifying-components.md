---
title: Klassifizieren von Komponenten
description: Klassifizieren von Komponenten
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e8382c1cbada72c2a8ab480ded78702424736850299b9e5e9fad7b328e3280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048708"
---
# <a name="classifying-components"></a>Klassifizieren von Komponenten

Während ein Client in der Lage ist, die Liste der CLSIDs in der Registrierung zu durchsuchen und eine zu verwendende Komponente auszuwählen, ist das Laden jeder Komponente in der Registrierung und das Abfragen der unterstützten Schnittstellen sehr zeitaufwändig. Um zu bestimmen, ob eine Komponente die Schnittstellen unterstützt, die vor dem Erstellen einer Instanz der Komponente erforderlich sind, wurde eine Methode zum Klassifizieren von Komponenten in Kategorien entwickelt.

Eine Komponentenkategorie ist ein Satz von Schnittstellen, denen eine GUID mit dem Namen CATID zugewiesen wurde. Komponenten, die alle Schnittstellen in einer Komponentenkategorie implementieren, registrieren sich selbst als Mitglieder dieser Komponentenkategorie. Komponenten, die zu einer bestimmten Komponentenkategorie gehören, können dann aus der Registrierung ausgewählt werden. Indem sie sich selbst als Mitglied einer Komponentenkategorie registriert, garantiert die Komponente, dass sie alle Memberschnittstellen in der Komponentenkategorie unterstützt.

Eine Komponente kann ein Member vieler Kategorien sein. Sie ist nicht auf die Unterstützung von Schnittstellen in einer Komponentenkategorie beschränkt. Sie kann jede Schnittstelle zusätzlich zu den Schnittstellen in einer Komponentenkategorie unterstützen.

Im Gegensatz zur Standardregistrierung von Komponenten, bei der Entwickler Code schreiben müssen, der Objekte manuell registriert, automatisieren Komponentenkategorien einen Großteil dieser Arbeit. Die sechs Methoden der [**ICatRegister-Schnittstelle**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definieren Komponentenkategorien und registrieren Objekte, die sie implementieren oder erfordern. Das [Component Categories Manager-Objekt](the-component-categories-manager.md) implementiert diese Schnittstelle. Weitere Informationen zur Verwendung von Komponentenkategorien finden Sie unter **ICatRegister** und [**ICatInformation.**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 




