---
description: Bevor eine Anwendung die verteilte Routing Tabelle (DRT) durchsuchen kann, muss eine Suchabfrage erstellt werden.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Durchsuchen einer verteilten Routing Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347517"
---
# <a name="searching-a-distributed-routing-table"></a>Durchsuchen einer verteilten Routing Tabelle

Bevor eine Anwendung die verteilte Routing Tabelle (DRT) durchsuchen kann, muss eine Suchabfrage erstellt werden. Der gewünschte Schlüsselwert wird von der Anwendung angegeben, wenn die [**drtstartsearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) -Funktion aufgerufen wird. Das Verhalten der Suche wird anhand der Informationen bestimmt, die von der Anwendung in der [**DRT- \_ Such \_**](/windows/desktop/api/drt/ns-drt-drt_search_info) Informationsstruktur angegeben werden.

In der Regel wird ein Anwendungs Ereignis signalisiert, wenn die Suche Ergebnisse erkennt und eine andere am Ende der Suche. Wenn jedoch in der [**DRT- \_ Such \_ Info**](/windows/desktop/api/drt/ns-drt-drt_search_info)der Wert für " **fterative** " festgelegt ist, kann ein Anwendungs Ereignis signalisiert werden, wenn der Kontakt mit jedem Knoten auf die gleiche Weise hergestellt wird.

Nachdem ein Ereignis signalisiert wurde, ruft die Anwendung die [**drtgetsearchresult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) -Funktion für die Ergebnisse auf. Wenn der zurückgegebene Code **S \_ OK** ist, wird auf die Ergebnisse in der [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result) Struktur verwiesen, die von der API zurückgegeben wird. Die zurückgegebenen Ergebnisse fallen in den Wertebereich, der in [**DRT- \_ Such \_ Informationen**](/windows/desktop/api/drt/ns-drt-drt_search_info)angegeben ist. Wenn bei der Suche keine Übereinstimmungen gefunden werden, wird nur der DRT E-Wert zurückgegeben, der beim Abschluss der Ergebnis Rückgabe **\_ \_ nicht \_ mehr** verwendet wird.

Die folgenden Informationen geben Aufschluss darüber, wie die in [**DRT- \_ Such \_ Informationen**](/windows/desktop/api/drt/ns-drt-drt_search_info) enthaltenen Elemente es einer Anwendung ermöglichen, das Suchverhalten der DRT-Infrastruktur genau zu bestimmen:

## <a name="fallowcurrentinstancematch"></a>"f" currentinstancematch

Standardmäßig enthalten die DRT-Suchergebnisse nur Übereinstimmungen, die außerhalb des lokalen Knotens gefunden wurden. Durch Festlegen von " **sallowcurrentinstancematch** " wird angegeben, dass die Suchergebnisse auch Übereinstimmungen in der lokalen DRT-Instanz enthalten.

## <a name="cmaxendpoints"></a>cmaxendpoints

Die Menge und der Bereich der Ergebnisse, die von der Suche zurückgegeben werden, werden von der Anwendung mit den Werten **cmaxendpoints** (Menge) und **pminimumkey** und **pmaximumkey** (Range) angegeben, und es wird von der [**DRT- \_ Such \_ Information**](/windows/desktop/api/drt/ns-drt-drt_search_info)darauf verwiesen.

Wenn **cmaxendpoints = 1**, sucht die DRT-Infrastruktur nach einem Schlüssel und gibt eine Entsprechung innerhalb des Bereichs zurück, der durch die Werte **pminimumkey** und **pmaximumkey** in [**DRT- \_ Such \_ Informationen**](/windows/desktop/api/drt/ns-drt-drt_search_info)angegeben wird. Diese Entsprechung kann entweder eine genaue Entsprechung oder die nächstgelegene Entsprechung im Bereich sein. Wenn keine Entsprechung gefunden wird, wird **DRT \_ E \_ nicht \_ mehr** zurückgegeben.

Wenn **cmaxendpoints > 1**, gibt die DRT-Infrastruktur Übereinstimmungen innerhalb des Bereichs bis zum Wert von **cmaxendpoints** zurück. Die zurückgegebenen Übereinstimmungen können eine genaue Übereinstimmung oder die nächsten übereinstimmenden Ergebnisse innerhalb des Bereichs enthalten. Wenn **pminimumkey** und **pmaximumkey** auf denselben Wert festgelegt sind, wird außerdem eine Suche nur für diesen Wert durchgeführt, wobei **DRT \_ E \_ nicht \_ mehr** zurückgegeben wird, wenn er nicht gefunden wurde.

## <a name="fanymatchinrange"></a>fanymatchinrange

Das **fanymatchinrange** -Element gibt an, ob die Suche angehalten wird, nachdem sich die erste Entsprechung innerhalb des angegebenen Bereichs befindet, oder ob die Suche für die nächstgelegene Entsprechung mit dem in der [**drtstartsearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) -API angegebenen Schlüssel fortgesetzt wird. Wenn **fanymatchinrange** festgelegt ist, wird die Suche mit **cmaxendpoints = 1** ausgeführt, unabhängig vom angegebenen Wert von **cmaxendpoints** in [**DRT- \_ Such \_ Informationen**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>"fterativ"

Der **Member "** Member" gibt an, ob jeder Knoten, der von der DRT-Infrastruktur während der Suche kontaktiert wird, über die Schlüssel-/Endpunktdaten verfügt, die der Anwendung über das [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result)zur Verfügung gestellt werden. Wenn Sie "" auf " **true**" **festlegen, wird** der Wert von " **cmaxendpoints = 1** " erzwungen. Wenn " **fterative** " in einer Suchabfrage für das DRT auf " **true** " festgelegt ist, wird die Anwendung nach Kontakt mit jedem Knoten oder "Hop" zurückgerufen. Jedes Hop-Ergebnis enthält einen Schlüssel, der angibt, welcher Knoten von der DRT als nächstes durchsucht wird. Ein Hop-Ergebnis wird über [**drtgetsearchresult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) als ein DRT-Übereinstimmungs **\_ \_ zwischen** Ergebnis zurückgegeben.

## <a name="pminimumkey-and-pmaximumkey"></a>pminimumkey und pmaximumkey

Die Member **pminimumkey** und **pmaximumkey** können verwendet werden, um nach Schlüsseln zu suchen, die in einem Bereich liegen. Wenn das **fanymatchinrange** -Element auf **false** festgelegt ist, gibt der DRT die nächstgelegenen Schlüssel an das Such Ziel zurück (angegeben mithilfe des pkey-Arguments, das in der [**drtstartsearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) -Funktion übergeben wird), das innerhalb des Bereichs liegt. Beachten Sie, dass das an **drtstartsearch** weiter gegebene *pkey* -Argument in den von **pminimumkey** und **pmaximumkey** definierten Bereich liegen muss. Um nach einem präzisen Schlüssel zu suchen, legen Sie **pminimumkey**, **pmaximumkey** und *pkey* auf denselben Wert fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren und Aufheben der Registrierung von Schlüsseln](registering-and-deregistering-keys.md)
</dt> <dt>

[Informationen zu verteilten Routing Tabellen](about-distributed-routing-tables.md)
</dt> <dt>

[Tabellen-API Referenz zu verteiltem Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



