---
title: Regeln für die Implementierung von QueryInterface
description: Regeln für die Implementierung von QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337875"
---
# <a name="rules-for-implementing-queryinterface"></a>Regeln für die Implementierung von QueryInterface

Es gibt drei Hauptregeln, die die Implementierung der [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für ein COM-Objekt Steuern:

-   Objekte müssen über eine Identität verfügen.
-   Der Satz von Schnittstellen für eine Objektinstanz muss statisch sein.
-   Es muss möglich sein, für jede beliebige Schnittstelle eines Objekts von einer beliebigen anderen Schnittstelle aus erfolgreich eine Abfrage durchzusetzen.

## <a name="objects-must-have-identity"></a>Objekte müssen über eine Identität verfügen.

Für eine beliebige Objektinstanz muss ein [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufrufe mit IID \_ IUnknown immer denselben physischen Zeiger Wert zurückgeben. Dies ermöglicht es Ihnen, **QueryInterface** für zwei beliebige Schnittstellen aufzurufen und die Ergebnisse zu vergleichen, um zu bestimmen, ob Sie auf dieselbe Instanz eines Objekts zeigen.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>Der Satz von Schnittstellen für eine Objektinstanz muss statisch sein.

Der Satz von Schnittstellen, der über [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Objekt zugänglich ist, muss statisch und nicht dynamisch sein. Wenn **QueryInterface** \_ z. b. für eine bestimmte IID einmal OK zurückgibt, darf es niemals E \_ nointerface für nachfolgende Aufrufe desselben Objekts zurückgeben. Wenn **QueryInterface** \_ für eine bestimmte IID e nointerface zurückgibt, dürfen nachfolgende Aufrufe für dieselbe IID für das gleiche Objekt niemals S OK zurückgeben \_ .

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Es muss möglich sein, für jede Schnittstelle eines Objekts von einer beliebigen anderen Schnittstelle aus erfolgreich eine Abfrage durchzusetzen.

Das heißt, wenn der folgende Code angezeigt wird:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

die folgenden Regeln gelten:

-   Wenn Sie über einen Zeiger auf eine Schnittstelle für ein Objekt verfügen, muss ein-Befehl wie der folgende für [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für die gleiche Schnittstelle erfolgreich ausgeführt werden:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Wenn ein Abruf von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für einen zweiten Schnittstellen Zeiger erfolgreich ist, muss auch der **QueryInterface** -Rückruf von diesem Zeiger für die erste Schnittstelle erfolgreich ausgeführt werden. Wenn PB erfolgreich abgerufen wurde, muss Folgendes ebenfalls erfolgreich sein:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Jede Schnittstelle muss in der Lage sein, beliebige andere Schnittstellen in einem Objekt abzufragen. Wenn PB erfolgreich abgerufen wurde und Sie erfolgreich eine dritte Schnittstelle (IC) mithilfe dieses Zeigers abgefragt haben, müssen Sie auch in der Lage sein, mithilfe des ersten Zeigers (PA) erfolgreich eine Abfrage für den IC durchgeführt werden. In diesem Fall muss die folgende Sequenz erfolgreich ausgeführt werden:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Schnittstellen Implementierungen müssen einen Gegenstand von ausstehenden Zeiger verweisen auf alle Schnittstellen eines bestimmten Objekts beibehalten. Sie sollten eine **Ganzzahl ohne** Vorzeichen für den-Wert verwenden.

Wenn ein Client wissen muss, dass Ressourcen freigegeben wurden, muss er eine Methode in einer Schnittstelle für das Objekt mit einer Semantik auf höherer Ebene verwenden, bevor [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 