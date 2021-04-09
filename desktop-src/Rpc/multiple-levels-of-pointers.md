---
title: Mehrere Ebenen von Zeigern
description: Verwenden mehrerer Zeiger Ebenen in Remote Prozedur Aufruf (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948958"
---
# <a name="multiple-levels-of-pointers"></a>Mehrere Ebenen von Zeigern

Wenn mehrere Zeiger Ebenen vorhanden sind, werden die Attribute mit dem Zeiger verknüpft, der dem Variablennamen am nächsten liegt. Der Client ist nach wie vor für die Zuordnung von Arbeitsspeicher verantwortlich, der der Antwort zugeordnet ist.

Im folgenden Beispiel kann der Stub den Server anrufen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden:

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

In diesem Beispiel übergibt der Stub dem Server einen eindeutigen Zeiger, der vom Server mit **null** initialisiert wird. Der Server ordnet dann einen Block von Balken zu, legt den Zeiger fest, legt das Größen Argument fest und gibt zurück. Beachten Sie, dass Sie einen Verweis \[ \] Zeiger an einen \[ [**eindeutigen**](/windows/desktop/Midl/unique) \] Zeiger auf Ihre Daten übergeben müssen, damit der Server Auswirkungen auf den Aufrufer hat. Beachten Sie auch, dass das Komma in \[ [**size (, \_**](/windows/desktop/Midl/size-is) \* Psize) ist \] , das angibt, dass der Zeiger der obersten Ebene kein Größen Zeiger ist, aber dass der Zeiger auf der unteren Ebene ist.

Auf der Clientseite legt der Stub \* ppbar auf **null** fest, bevor die Remote Prozedur aufgerufen wird. Der Stub ordnet dann die Arrays von Bar-Objekten zu und löscht diese. Das size-Argument gibt die Größe des Blocks an (und die Anzahl der nicht gemarshallten Balken). Der Client muss das zurückgegebene Array von Balken Objekten freigeben, wenn es nicht mehr benötigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Größe \_ :**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 