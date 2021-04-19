---
title: Explizite Bindungs Handles
description: Um die maximale Kontrolle über den Bindungsprozess zu erhalten, verwenden Client/Server-Anwendungen möglicherweise explizite Bindungs Handles.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341862"
---
# <a name="explicit-binding-handles"></a>Explizite Bindungs Handles

Um die maximale Kontrolle über den Bindungsprozess zu erhalten, verwenden Client/Server-Anwendungen möglicherweise explizite Bindungs Handles. Wie implizite Handles ermöglichen explizite Bindungs Handles Ihrer Client Anwendung, einen Server für die Ausführung ihrer Aufrufe auszuwählen. Außerdem ermöglichen explizite Bindungs Handles Ihrer Client/Server-Anwendung das Erstellen einer authentifizierten RPC-Kommunikationssitzung. Mit expliziten Handles kann der Client eine Verbindung mit mehr als einem Server herstellen und Remote Prozeduren auf mehreren Servern ausführen. Multithread-und asynchrone Client Anwendungen können sogar eine Verbindung mit mehreren Servern herstellen und gleichzeitig mehrere Remote Prozeduren ausführen.

Die Client Anwendung muss das explizite Handle als Parameter an jeden Remote Prozedur aufzurufen übergeben. Um dem OSF-Standard zu entsprechen, sollte das Handle für jede Remote Prozedur als erster Parameter angegeben werden. Die Microsoft-Erweiterungen für RPC ermöglichen es Ihnen jedoch, das Bindungs Handle an anderen Positionen anzugeben. Weitere Informationen finden Sie unter [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).

Zum Erstellen eines expliziten Handles deklarieren Sie das Handle als Parameter für die Remote Vorgänge in der IDL-Datei. Das [Hello, World-Beispiel](tutorial.md) kann so neu definiert werden, dass ein explizites handle wie gezeigt verwendet wird:

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

Sie können explizite und implizite Handles in einer einzelnen Schnittstelle kombinieren. Wenn eine Funktion einen expliziten Handle in der Parameterliste aufweist, wird dieses Handle verwendet. Wenn eine Funktion in einer Schnittstelle, die implizite Handles verwendet, kein explizites Handle angibt, wird das implizite Standard Handle verwendet.

 

 




