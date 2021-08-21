---
title: Regeln für die Implementierung von QueryInterface
description: Regeln für die Implementierung von QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0d0df2d0382c670ed6f4a323f55dcdd1b187430282abe6699da186e574e390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047868"
---
# <a name="rules-for-implementing-queryinterface"></a>Regeln für die Implementierung von QueryInterface

Es gibt drei Hauptregeln, die die Implementierung der [**IUnknown::QueryInterface-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein COM-Objekt steuern:

-   Objekte müssen eine Identität haben.
-   Der Satz von Schnittstellen für eine Objektinstanz muss statisch sein.
-   Es muss möglich sein, eine beliebige Schnittstelle für ein Objekt von einer anderen Schnittstelle aus erfolgreich abfragen zu können.

## <a name="objects-must-have-identity"></a>Objekte müssen eine Identität haben

Für jede objektinstanz muss ein Aufruf von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) mit IID IUnknown immer den gleichen physischen \_ Zeigerwert zurückgeben. Auf diese Weise können Sie **QueryInterface** für zwei schnittstellen aufrufen und die Ergebnisse vergleichen, um zu bestimmen, ob sie auf die gleiche Instanz eines Objekts zeigen.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>Der Satz von Schnittstellen für eine Objektinstanz muss statisch sein.

Der Satz von Schnittstellen, auf die über [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) auf ein Objekt zugegriffen werden kann, muss statisch und nicht dynamisch sein. Wenn **QueryInterface** einmal S OK für eine bestimmte IID zurückgibt, darf sie bei nachfolgenden Aufrufen desselben Objekts nie \_ E \_ NOINTERFACE zurückgeben. Wenn **QueryInterface** E NOINTERFACE für eine bestimmte IID zurückgibt, dürfen nachfolgende Aufrufe für dieselbe IID für dasselbe Objekt niemals \_ S \_ OK zurückgeben.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Eine erfolgreiche Abfrage für eine beliebige Schnittstelle für ein Objekt muss über eine beliebige andere Schnittstelle möglich sein.

Das heißt, wenn der folgende Code verwendet wird:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

Es gelten die folgenden Regeln:

-   Wenn Sie über einen Zeiger auf eine Schnittstelle für ein Objekt verfügen, muss ein Aufruf wie der folgende [**an QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für dieselbe Schnittstelle erfolgreich sein:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Wenn ein Aufruf von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für einen zweiten Schnittstellenzeiger erfolgreich ist, muss auch ein Aufruf von **QueryInterface** von diesem Zeiger für die erste Schnittstelle erfolgreich sein. Wenn pB erfolgreich erhalten wurde, muss auch Folgendes erfolgreich sein:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Jede Schnittstelle muss in der Lage sein, abfragen zu können, ob eine andere Schnittstelle für ein Objekt verwendet wird. Wenn pB erfolgreich erhalten wurde und Sie erfolgreich eine dritte Schnittstelle (IC) mit diesem Zeiger abfragen, müssen Sie auch in der Lage sein, ic mit dem ersten Zeiger, pA, erfolgreich abfragen zu können. In diesem Fall muss die folgende Sequenz erfolgreich sein:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Schnittstellenimplementierungen müssen einen Indikator ausstehender Zeigerverweise auf alle Schnittstellen eines bestimmten Objekts verwalten. Sie sollten eine ganze **Zahl ohne Vorzeichen für** den Zähler verwenden.

Wenn ein Client wissen muss, dass Ressourcen frei wurden, muss er vor dem Aufruf von [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)eine Methode in einer Schnittstelle des Objekts mit semantischer Semantik auf höherer Ebene verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 