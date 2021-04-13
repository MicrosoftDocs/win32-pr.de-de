---
title: Implementieren von IClassFactory
description: Implementieren von IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391044"
---
# <a name="implementing-iclassfactory"></a>Implementieren von IClassFactory

Wenn ein Client eine CLSID verwendet, um die Erstellung einer Objektinstanz anzufordern, besteht der erste Schritt in der Erstellung eines Klassen Objekts, einem zwischen Objekt, das eine Implementierung der Methoden der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle enthält. Während com mehrere Instanzen Erstellungs Funktionen bereitstellt, ist der erste Schritt bei der Implementierung dieser Funktionen die Erstellung eines Klassen Objekts.

Daher müssen alle Server die Methoden der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle implementieren, die zwei Methoden enthält:

-   " [**Kreatabstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)". Diese Methode muss eine nicht initialisierte Instanz des-Objekts erstellen und einen Zeiger auf eine angeforderte Schnittstelle für das-Objekt zurückgeben.
-   [**Lock Server**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Diese Methode erhöht lediglich den Verweis Zähler für das Klassenobjekt, um sicherzustellen, dass der Server im Arbeitsspeicher bleibt und nicht heruntergefahren wird, bevor der Client dafür bereit ist.

Damit ein Server für seine eigene Lizenzierung verantwortlich ist, definiert com [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), das seine Definition von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)erbt. Daher muss ein Server, der **IClassFactory2** implementiert, definitionsgemäß die Methoden von **IClassFactory** implementieren.

COM bietet auch Hilfsfunktionen zum Implementieren von Prozess externen Servern. Weitere Informationen finden Sie unter [Implementierung von Out-of-Process-Server Implementierungen](out-of-process-server-implementation-helpers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuständigkeiten von com-Servern](com-server-responsibilities.md)
</dt> <dt>

[Lizenzierung und IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 