---
title: IUnknown und Schnittstellen Vererbung
description: IUnknown und Schnittstellen Vererbung
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341966"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown und Schnittstellen Vererbung

Vererbung in com bedeutet nicht, dass Code wieder verwendet werden kann. Da keine Implementierungen Schnittstellen zugeordnet sind, bedeutet die Schnittstellen Vererbung nicht die Code Vererbung. Dies bedeutet lediglich, dass der Vertrag, der einer Schnittstelle zugeordnet ist, in einer reinen C++-Basisklasse geerbt und geändert werden – entweder durch Hinzufügen neuer Methoden oder durch Weiterqualifizierung der zulässigen Verwendung von Methoden. Es gibt keine selektive Vererbung in com. Wenn eine Schnittstelle von einer anderen Schnittstelle erbt, umfasst Sie alle Methoden, die von der anderen Schnittstelle definiert werden.

Die Vererbung wird in den vordefinierten com-Schnittstellen sparsam verwendet. Alle vordefinierten Schnittstellen (und benutzerdefinierte Schnittstellen, die Sie definieren) erben ihre Definitionen von der wichtigen Schnittstelle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), die drei wichtige Methoden enthält: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Alle COM-Objekte müssen die **IUnknown** -Schnittstelle implementieren, da Sie mithilfe von **QueryInterface** die Möglichkeit bietet, zwischen den verschiedenen Schnittstellen, die von einem Objekt unterstützt werden, und der Möglichkeit zur Verwaltung der Lebensdauer mithilfe von **adressf** und **Release** frei zu verschieben.

Wenn Sie ein Objekt erstellen, das [Aggregationen](aggregation.md)unterstützt, müssen Sie einen Satz von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Funktionen für alle Schnittstellen und eine eigenständige **IUnknown** -Schnittstelle implementieren. In jedem Fall implementiert jedes Objekt, das implementiert wird, **IUnknown** -Methoden. Weitere Informationen finden [Sie im Abschnitt verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md) .

Es gibt zwar einige Schnittstellen, die ihre Definitionen zusätzlich zu [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)von einer zweiten Schnittstelle erben, aber die Mehrzahl erbt lediglich die **IUnknown** -Schnittstellen Methoden. Dadurch sind die meisten Schnittstellen relativ kompakt und leicht zu kapseln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Objekte und-Schnittstellen](com-objects-and-interfaces.md)
</dt> </dl>

 

 