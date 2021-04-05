---
title: COM-Objekte und-Schnittstellen
description: COM-Objekte und-Schnittstellen
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707787"
---
# <a name="com-objects-and-interfaces"></a>COM-Objekte und-Schnittstellen

COM ist eine Technologie, mit der Objekte innerhalb eines einzelnen Prozesses über Prozess-und Computer Grenzen hinweg interagieren können. COM ermöglicht dies durch Angabe, dass die einzige Möglichkeit zum Bearbeiten der einem Objekt zugeordneten Daten über eine *Schnittstelle* des Objekts ist. Wenn dieser Begriff in dieser Dokumentation verwendet wird, bezieht er sich auf eine Implementierung im Code einer Binär-kompatiblen com-Schnittstelle, die einem Objekt zugeordnet ist.

COM verwendet die Word- *Schnittstelle* in einem anderen Sinne als das, das normalerweise in Visual C++ Programmierung verwendet wird. Eine C++-Schnittstelle bezieht sich auf alle Funktionen, die von einer Klasse unterstützt werden, und die Clients eines Objekts können aufzurufen, um mit ihm zu interagieren. Eine COM-Schnittstelle verweist auf eine vordefinierte Gruppe verwandter Funktionen, die eine COM-Klasse implementiert, aber eine bestimmte Schnittstelle stellt nicht notwendigerweise alle Funktionen dar, die von der Klasse unterstützt werden.

Das verweisen auf ein *Objekt,* das eine-Schnittstelle implementiert, bedeutet, dass das-Objektcode verwendet, der jede Methode der Schnittstelle implementiert und com-Binär-kompatible Zeiger auf diese Funktionen der com-Bibliothek bereitstellt. COM stellt diese Funktionen dann jedem Client zur Verfügung, der einen Zeiger auf die-Schnittstelle anfordert, unabhängig davon, ob sich der Client innerhalb oder außerhalb des Prozesses befindet, der diese Funktionen implementiert.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Schnittstellen und Schnittstellen Implementierungen](interfaces-and-interface-implementations.md)
-   [Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)](interface-pointers-and-interfaces.md)
-   [IUnknown und Schnittstellen Vererbung](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](interfaces.md)
</dt> </dl>

 

 




