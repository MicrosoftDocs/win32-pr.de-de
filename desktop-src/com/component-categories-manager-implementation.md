---
title: Implementierung des Komponenten Kategorien-Managers
description: Wenn die Anzahl der verfügbaren Komponenten zunimmt, wird es zunehmend schwieriger, diese Komponenten zu verwalten. Im Hinblick auf die Schnittstellen, die Sie verfügbar machen, und die Aufgaben, die Sie ausführen, bieten viele Komponenten eine ähnliche Funktionalität.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2414567beba159c05ea08b3561f0a97ddda1cb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948068"
---
# <a name="component-categories-manager-implementation"></a>Implementierung des Komponenten Kategorien-Managers

Wenn die Anzahl der verfügbaren Komponenten zunimmt, wird es zunehmend schwieriger, diese Komponenten zu verwalten. Im Hinblick auf die Schnittstellen, die Sie verfügbar machen, und die Aufgaben, die Sie ausführen, bieten viele Komponenten eine ähnliche Funktionalität.

Häufig müssen die Komponenten aufgelistet werden, die in einem bestimmten Kontext verwendet werden können. Beispiele hierfür sind das Dialogfeld " **Objekt einfügen** ", das in OLE-Verbund Dokumenten verwendet wird, und das Dialogfeld " **Steuerelement einfügen** " in OLE-Steuerelementen In diesen Dialogfeldern werden alle Komponenten aufgelistet, die die Schnittstellen Verträge für Verbund Dokumente oder Steuerelemente erfüllen (oder den Anspruch darauf erfüllen). Diese vorhandenen Kategorien (OLE-Dokument, OLE-Steuerelement) implizieren keine exakte Schnittstellen Signatur. OLE-Dokumente müssen einen bestimmten Satz von Kern Schnittstellen (z. b. [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) oder [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)) verfügbar machen, können aber auch zusätzliche Schnittstellen wie [**iolelink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)verfügbar machen.

In der Vergangenheit wurden Komponenten gekennzeichnet, indem ein lesbarer Name ("Insertable", "Control" usw.) als Unterschlüssel für die Stamm- **\_ \_ \\ CLSID \\ {...} der HKEY-Klassen** hinzugefügt wurde. Registrierungsschlüssel, der der Komponente entspricht. Dies funktioniert gut für eine zentrale Definition von Kategorien, birgt jedoch Risiken Namenskollisionen, wenn viele unabhängige Parteien neue Kategorien definieren. Wie in anderen Bereichen von com liegt die Lösung zur Bereitstellung eines erweiterbaren Namespace in der Verwendung von GUIDs (Global Unique Identifier). Anstatt einen lesbaren Namen zu verwenden, wird jeder Kategorie eine eindeutige Zahl (CATID) zugewiesen.

Eine weitere Einschränkung bei der vorhandenen Kategorisierung besteht darin, dass Sie auf das Ausdrücken der Funktionen der Komponente selbst beschränkt ist. Viele Komponenten erfordern bestimmte Funktionen aus den Containern. Wenn eine solche Komponente in einen Container eingefügt wird, kann die Einfügung fehlschlagen oder sich unerwartet Verhalten, auch wenn die Komponente die Verträge erfüllt, die von einer ihrer Kategorien impliziert werden. Zum Auflisten der Komponenten, die in bestimmten Situationen erfolgreich verwendet werden können, müssen die Funktionen der Komponente und des Containers berücksichtigt werden.

Aufgrund dieser Überlegungen wurden die folgenden Änderungen an der vorhandenen Kategorisierung vorgenommen:

-   Kategorien werden mithilfe von CATIDs angegeben, die global eindeutige Bezeichner sind.
-   Unter dem **Komponenten** Unterschlüssel des Stamm- **\_ \_ \\ CLSID** -Registrierungsschlüssels der HKEY-Klassen wurden zwei separate Unterschlüssel ("implementierte Kategorien" und "erforderliche Kategorien") entwickelt. Diese Unterschlüssel enthalten die Listen der CATIDs, die von der Komponente bereitgestellt werden, oder die der Container der Komponente bereitstellen muss.

Um die Verwaltung der Komponenten Kategorien zu vereinfachen, werden Kategorien an einem zentralen Ort in der Registrierung aufgeführt: **HKEY- \_ Klassen Stamm \_ \\ Komponenten Kategorien**. Mit diesem Schlüssel werden die installierten Kategorien sowohl mit ihrer CATID als auch mit lokalisierten, lesbaren Namen aufgelistet.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Kategorisierung nach Komponenten Funktionen](categorizing-by-component-capabilities.md)
-   [Kategorisierung nach Container Funktionen](categorizing-by-container-capabilities.md)
-   [Der Komponenten Kategorien-Manager](the-component-categories-manager.md)
-   [Standardklassen und-Zuordnungen](default-classes-and-associations.md)
-   [Definieren von Komponenten Kategorien](defining-component-categories.md)
-   [Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)

 

 




