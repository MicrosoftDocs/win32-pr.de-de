---
description: Bevor eine Anwendung die Verteilte Routingtabelle (Distributed Routing Table, DRT) durchsuchen kann, muss eine Suchabfrage erstellt werden.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Durchsuchen einer verteilten Routingtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9016c351412d80b7adb97bc4325dae546e24db68e5737badc311e7c068f1a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034240"
---
# <a name="searching-a-distributed-routing-table"></a>Durchsuchen einer verteilten Routingtabelle

Bevor eine Anwendung die Verteilte Routingtabelle (Distributed Routing Table, DRT) durchsuchen kann, muss eine Suchabfrage erstellt werden. Der gewünschte Schlüsselwert wird von der Anwendung angegeben, wenn die [**DrtStartSearch-Funktion**](/windows/desktop/api/drt/nf-drt-drtstartsearch) aufgerufen wird. Das Verhalten der Suche wird durch Informationen bestimmt, die von der Anwendung in der [**DRT \_ SEARCH \_ INFO-Struktur**](/windows/desktop/api/drt/ns-drt-drt_search_info) angegeben werden.

In der Regel wird ein Anwendungsereignis signalisiert, wenn die Suche Ergebnisse und ein anderes am Ende der Suche ermittelt. Wenn **fIterative** jedoch in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info)festgelegt ist, kann ein Anwendungsereignis signalisiert werden, wenn ein Kontakt mit jedem Knoten hergestellt wird.

Nachdem ein Ereignis signalisiert wurde, ruft die Anwendung dann die [**DrtGetSearchResult-Funktion**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) für die Ergebnisse auf. Wenn der zurückgegebene Code **S \_ OK** ist, werden die Ergebnisse in der von der API zurückgegebenen [**DRT \_ SEARCH \_ RESULT-Struktur**](/windows/desktop/api/drt/ns-drt-drt_search_result) angezeigt. Die zurückgegebenen Ergebnisse fallen in den In [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info)angegebenen Wertebereich. Wenn die Suche keine Übereinstimmungen findet, wird nur der **WERT DRT \_ E NO \_ \_ MORE** am Ende der Ergebnisrücksendung zurückgegeben.

In den folgenden Informationen wird erläutert, wie die in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) enthaltenen Elemente einer Anwendung ermöglichen, das Suchverhalten der DRT-Infrastruktur explizit vorzuschreiben:

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

Standardmäßig enthalten DRT-Suchergebnisse nur Übereinstimmungen, die außerhalb des lokalen Knotens gefunden wurden. Durch festlegen von **fAllowCurrentInstanceMatch** wird angegeben, dass die Suchergebnisse auch Übereinstimmungen enthalten, die in der lokalen DRT-Instanz gefunden wurden.

## <a name="cmaxendpoints"></a>cMaxEndpoints

Die Menge und der Bereich der von der Suche zurückgegebenen Ergebnisse werden von der Anwendung mit den Werten **cMaxEndpoints** (quantity) und **pMinimumKey** und **pMaximumKey** (Bereich) angegeben und von [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info)referenziert.

Wenn **cMaxEndpoints = 1** ist, sucht die DRT-Infrastruktur nach einem Schlüssel und gibt eine Übereinstimmung innerhalb des Bereichs zurück, der durch die Werte **pMinimumKey** und **pMaximumKey** in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info)angegeben wird. Diese Übereinstimmung kann entweder eine genaue Übereinstimmung oder die nächste Übereinstimmung innerhalb des Bereichs sein. Wenn keine Übereinstimmung gefunden wird, wird **DRT \_ E NO \_ \_ MORE** zurückgegeben.

Wenn **cMaxEndpoints > 1** ist, gibt die DRT-Infrastruktur Übereinstimmungen innerhalb des Bereichs bis zum Wert von **cMaxEndpoints** zurück. Die zurückgegebenen Übereinstimmungen können eine genaue Übereinstimmung oder die nächsten Übereinstimmungsergebnisse innerhalb des Bereichs enthalten. Wenn **pMinimumKey** und **pMaximumKey** auf denselben Wert festgelegt sind, wird eine Suche nur für diesen Wert durchgeführt, und es wird **DRT \_ E NO \_ \_ MORE** zurückgegeben, wenn er nicht gefunden wird.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

Das **fAnyMatchInRange-Element** gibt an, ob die Suche beendet wird, nachdem die erste Übereinstimmung innerhalb des angegebenen Bereichs gefunden wurde, oder ob die Suche nach der nächsten Übereinstimmung mit dem in der [**DrtStartSearch-API**](/windows/desktop/api/drt/nf-drt-drtstartsearch) angegebenen Schlüssel fortgesetzt wird. Wenn **fAnyMatchInRange** festgelegt ist, wird die Suche mit **cMaxEndpoints = 1** ausgeführt, unabhängig vom angegebenen Wert von **cMaxEndpoints** in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

Der **fIterative-Member** gibt an, ob jedem Knoten, der während der Suche von der DRT-Infrastruktur kontaktiert wird, die Schlüssel-/Endpunktdaten zugeordnet sind, die der Anwendung über [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result)zur Verfügung gestellt werden. Durch Festlegen von **fIterative** auf **TRUE** wird der Wert von **cMaxEndpoints = 1** erzwungen. Wenn **fIterative** in einer Suchabfrage für das DRT auf **TRUE** festgelegt ist, wird die Anwendung nach dem Kontakt mit jedem Knoten oder "Hop" zurückgerufen. Jedes Hopergebnis enthält einen Schlüssel, der angibt, welcher Knoten vom DRT als Nächstes durchsucht wird. Ein Hopergebnis wird über [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) als **DRT \_ MATCH \_ INTERMEDIATE-Ergebnis** zurückgegeben.

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey und pMaximumKey

Die Member **pMinimumKey** und **pMaximumKey** können verwendet werden, um nach Schlüsseln zu suchen, die innerhalb eines Bereichs liegen. Wenn der **fAnyMatchInRange-Member** auf **FALSE** festgelegt ist, gibt das DRT die nächstgelegenen Schlüssel an das Suchziel zurück (angegeben mithilfe des pKey-Arguments, das in der [**DrtStartSearch-Funktion**](/windows/desktop/api/drt/nf-drt-drtstartsearch) übergeben wird), die innerhalb des Bereichs liegen. Beachten Sie, dass das an **DrtStartSearch** übergebene *pKey-Argument* innerhalb des durch **pMinimumKey** und **pMaximumKey** definierten Bereichs liegen muss. Um nach einem präzisen Schlüssel zu suchen, legen Sie **pMinimumKey,** **pMaximumKey** und *pKey* auf den gleichen Wert fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren und Aufheben der Registrierung von Schlüsseln](registering-and-deregistering-keys.md)
</dt> <dt>

[Informationen zu verteilten Routingtabellen](about-distributed-routing-tables.md)
</dt> <dt>

[Tabellen-API-Referenz für verteiltes Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



