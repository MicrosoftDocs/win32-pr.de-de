---
title: COM-Objekte und -Schnittstellen
description: COM-Objekte und -Schnittstellen
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a663b5d6e5966422927e37f1501924bf8ec8921210c9d38765153dc0d80fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501550"
---
# <a name="com-objects-and-interfaces"></a>COM-Objekte und -Schnittstellen

COM ist eine Technologie, mit der Objekte so einfach wie innerhalb eines einzelnen Prozesses über Prozess- und Computergrenzen hinweg interagieren können. COM ermöglicht dies, indem angegeben wird, dass die einzige Möglichkeit zum Bearbeiten der einem Objekt zugeordneten Daten über eine Schnittstelle *des* Objekts ist. Wenn dieser Begriff in dieser Dokumentation verwendet wird, bezieht er sich auf eine Implementierung im Code einer binärkonformen COM-Schnittstelle, die einem -Objekt zugeordnet ist.

COM verwendet die *Wortschnittstelle* in einem anderen Sinn als die, die in der Regel in der Visual C++ wird. Eine C++-Schnittstelle bezieht sich auf alle Funktionen, die von einer Klasse unterstützt werden und die Clients eines Objekts aufrufen können, um damit zu interagieren. Eine COM-Schnittstelle bezieht sich auf eine vordefinierte Gruppe verwandter Funktionen, die von einer COM-Klasse implementiert werden, aber eine bestimmte Schnittstelle stellt nicht notwendigerweise alle Funktionen dar, die die Klasse unterstützt.

Der Verweis auf  ein Objekt, das eine Schnittstelle implementiert, bedeutet, dass das Objekt Code verwendet, der jede Methode der Schnittstelle implementiert und COM-binärkonforme Zeiger auf diese Funktionen für die COM-Bibliothek bietet. COM stellt diese Funktionen dann jedem Client zur Verfügung, der nach einem Zeiger auf die Schnittstelle fragt, unabhängig davon, ob sich der Client innerhalb oder außerhalb des Prozesses befindet, der diese Funktionen implementiert.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Schnittstellen und Schnittstellenimplementierung](interfaces-and-interface-implementations.md)
-   [Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)](interface-pointers-and-interfaces.md)
-   [IUnknown und Schnittstellenvererbung](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](interfaces.md)
</dt> </dl>

 

 




