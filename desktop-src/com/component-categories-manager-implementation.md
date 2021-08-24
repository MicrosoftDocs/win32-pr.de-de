---
title: Implementierung des Komponentenkategorien-Managers
description: Mit zunehmender Anzahl verfügbarer Komponenten wird es immer schwieriger, diese Komponenten zu verwalten. In Bezug auf die verfügbar gemachten Schnittstellen und die aufgaben, die sie ausführen, bieten viele Komponenten ähnliche Funktionen.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941ba5f422a4305a3bb6056d1d02648dde3bffc9c9f872fe7f7804ebb90a19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679211"
---
# <a name="component-categories-manager-implementation"></a>Implementierung des Komponentenkategorien-Managers

Mit zunehmender Anzahl verfügbarer Komponenten wird es immer schwieriger, diese Komponenten zu verwalten. In Bezug auf die verfügbar gemachten Schnittstellen und die aufgaben, die sie ausführen, bieten viele Komponenten ähnliche Funktionen.

Häufig müssen die Komponenten aufzählt werden, die in einem bestimmten Kontext verwendet werden können. Beispiele hierfür sind das **Dialogfeld Objekt** einfügen, das  in OLE-Verbunddokumenten verwendet wird, und das Dialogfeld Steuerelement einfügen, das in OLE-Steuerelementen verwendet wird. In diesen Dialogfeldern werden alle Komponenten aufgeführt, die die Schnittstellenverträge für Verbunddokumente oder Steuerelemente erfüllen (oder erfüllen). Diese vorhandenen Kategorien (OLE-Dokument, OLE-Steuerelement) implizieren keine exakte Schnittstellensignatur. OLE-Dokumente müssen einen bestimmten Satz von Kernschnittstellen (z. B. [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) oder [**IPersistStorage)**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)verfügbar machen, können aber auch zusätzliche Schnittstellen wie [**IOleLink verfügbar machen.**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)

In der Vergangenheit wurden Komponenten markiert, indem der **HKEY \_ CLASSES ROOT \_ \\ CLSID \\ {...}** ein für Menschen lesbarer Name ("Insertable", "Control" und so weiter) als Unterschlüssel hinzugefügt wurde. Registrierungsschlüssel, der der Komponente entspricht. Dies funktioniert gut für eine zentrale Definition von Kategorien, birgt jedoch das Risiko von Namenskollisionen, wenn viele unabhängige Parteien neue Kategorien definieren. Wie in anderen Bereichen von COM besteht die Lösung für die Bereitstellung eines erweiterbaren Namespace in der Verwendung von global eindeutigen Bezeichnern (GUIDs). Anstatt einen lesbaren Namen zu verwenden, wird jeder Kategorie eine eindeutige Zahl (CATID) zugewiesen.

Eine weitere Einschränkung bei der vorhandenen Kategorisierung ist, dass sie auf das Ausdrücken der Funktionen der Komponente selbst beschränkt ist. Viele Komponenten erfordern bestimmte Funktionen der Container. Wenn eine solche Komponente in einen Container eingefügt wird, kann die Einfügung fehlschlagen oder sich unerwartet verhalten, obwohl die Komponente die Verträge erfüllt, die von einer ihrer Kategorien impliziert werden. Um die Komponenten aufzählen zu können, die in bestimmten Situationen erfolgreich verwendet werden können, müssen die Funktionen der Komponente und des Containers berücksichtigt werden.

Aufgrund dieser Überlegungen wurden die folgenden Änderungen an der vorhandenen Kategorisierung vorgenommen:

-   Kategorien werden mithilfe von CATIDs angegeben, die global eindeutige Bezeichner sind.
-   Unter dem **Unterschlüssel Components** des **HKEY \_ CLASSES ROOT \_ \\ CLSID-Registrierungsschlüssels** wurden zwei separate Unterschlüssel entwickelt: "Implementierte Kategorien" und "Erforderliche Kategorien". Diese Unterschlüssel enthalten die Listen von CATIDs, die von der Komponente bereitgestellt werden oder die der Container der Komponente bereitstellen muss.

Um die Verwaltung der Komponentenkategorien zu erleichtern, werden Kategorien an einem zentralen Ort in der Registrierung aufgeführt: **HKEY \_ CLASSES ROOT \_ Component \\ Categories**. Dieser Schlüssel listet die installierten Kategorien sowohl mit ihrer CATID als auch mit lokalisierten, lesbaren Namen auf.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Kategorisieren nach Komponentenfunktionen](categorizing-by-component-capabilities.md)
-   [Kategorisieren nach Containerfunktionen](categorizing-by-container-capabilities.md)
-   [Der Komponentenkategorien-Manager](the-component-categories-manager.md)
-   [Standardklassen und Zuordnungen](default-classes-and-associations.md)
-   [Definieren von Komponentenkategorien](defining-component-categories.md)
-   [Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)

 

 




