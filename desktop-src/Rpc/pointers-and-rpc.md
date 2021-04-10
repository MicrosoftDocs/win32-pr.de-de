---
title: Zeiger und RPC
description: Es ist sehr effizient, Zeiger als C-Funktionsparameter zu verwenden.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856636"
---
# <a name="pointers-and-rpc"></a>Zeiger und RPC

Es ist sehr effizient, Zeiger als C-Funktionsparameter zu verwenden. Der Zeiger kostet nur einige Bytes und kann verwendet werden, um auf eine große Menge an Arbeitsspeicher zuzugreifen. In einer verteilten Anwendung befinden sich die Client-und Server Prozeduren jedoch in unterschiedlichen Adressräumen – Sie können sich auf unterschiedlichen Computern befinden. Daher haben der Client und der Server in der Regel keinen Zugriff auf denselben Speicherplatz.

Wenn einer der Parameter der Remote Prozedur ein Zeiger auf ein Objekt ist, muss der Client eine Kopie des Objekts und dessen Zeiger auf den Server übertragen. Wenn das Objekt durch die Remote Prozedur über seinen Zeiger geändert wird, gibt der Server den Zeiger und seine geänderte Kopie zurück.

In der mittleren l werden Zeiger Attribute angeboten, um den erforderlichen mehr Aufwand und die Größe der Anwendung zu minimieren. In diesem Abschnitt werden der Zweck und die Verwendung von-Mittell-Zeiger Attributen erläutert. Außerdem werden Informationen zur Zeiger Behandlung in RPC-Anwendungen angezeigt. Es ist in die folgenden Themen unterteilt:

-   [Arten von Zeigern](kinds-of-pointers.md)
-   [Zeiger und Speicher Belegung](pointers-and-memory-allocation.md)
-   [Standard Zeiger Typen](default-pointer-types.md)
-   [Vererbung von Attributtypen](pointer-attribute-type-inheritance.md)

 

 




