---
title: Zeiger und RPC
description: Es ist sehr effizient, Zeiger als C-Funktionsparameter zu verwenden.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2ce934ed1440bc070fab1b59b76f87182419aada06acaf7699533ef9989697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019182"
---
# <a name="pointers-and-rpc"></a>Zeiger und RPC

Es ist sehr effizient, Zeiger als C-Funktionsparameter zu verwenden. Der Zeiger kostet nur wenige Bytes und kann für den Zugriff auf eine große Menge an Arbeitsspeicher verwendet werden. In einer verteilten Anwendung befinden sich die Client- und Serververfahren jedoch in unterschiedlichen Adressräumen– sie können sich auf unterschiedlichen Computern befinden. Aus diesem Grund haben Client und Server in der Regel keinen Zugriff auf denselben Speicherplatz.

Wenn einer der Parameter der Remoteprozedur ein Zeiger auf ein Objekt ist, muss der Client eine Kopie dieses Objekts und seines Zeigers auf den Server übertragen. Wenn die Remoteprozedur das Objekt über seinen Zeiger ändert, gibt der Server den Zeiger und die geänderte Kopie zurück.

MIDL bietet Zeigerattribute, um den erforderlichen Mehraufwand und die Größe Ihrer Anwendung zu minimieren. In diesem Abschnitt werden der Zweck und die Verwendung von MIDL-Zeigerattributen erläutert. Außerdem werden Informationen zur Zeigerbehandlung in RPC-Anwendungen präsentiert. Sie ist in die folgenden Themen unterteilt:

-   [Arten von Zeigern](kinds-of-pointers.md)
-   [Zeiger und Speicherzuweisung](pointers-and-memory-allocation.md)
-   [Standardzeigertypen](default-pointer-types.md)
-   [Zeigerattributtypvererbung](pointer-attribute-type-inheritance.md)

 

 




