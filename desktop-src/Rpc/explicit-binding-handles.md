---
title: Explizite Bindungshandles
description: Für maximale Kontrolle über den Bindungsprozess können Client-/Serveranwendungen explizite Bindungshandles verwenden.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a6e723d8559dc5e72783412eb6250f69431f31d08a92c4984fb2e2a19b761d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930019"
---
# <a name="explicit-binding-handles"></a>Explizite Bindungshandles

Für maximale Kontrolle über den Bindungsprozess können Client-/Serveranwendungen explizite Bindungshandles verwenden. Wie implizite Handles ermöglichen explizite Bindungshandles Ihrer Clientanwendung die Auswahl eines Servers zum Ausführen der Aufrufe. Darüber hinaus ermöglichen explizite Bindungshandles Ihrer Client-/Serveranwendung das Erstellen einer authentifizierten RPC-Kommunikationssitzung. Mit expliziten Handles kann Ihr Client eine Verbindung mit mehreren Servern herstellen und Remoteverfahren auf mehreren Servern ausführen. Multithread- und asynchrone Clientanwendungen können sogar eine Verbindung mit mehreren Servern herstellen und mehrere Remoteverfahren gleichzeitig ausführen.

Ihre Clientanwendung muss das explizite Handle als Parameter an jeden Remoteprozeduraufruf übergeben. Um dem OSF-Standard zu entsprechen, sollte das Handle als erster Parameter für jede Remoteprozedur angegeben werden. Mit den Rpc-Erweiterungen von Microsoft können Sie jedoch das Bindungshand handle an anderen Positionen angeben. Weitere Informationen finden Sie unter [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).

Um ein explizites Handle zu erstellen, deklarieren Sie das Handle als Parameter für die Remotevorgänge in der IDL-Datei. Das [Hello, World-Beispiel](tutorial.md) kann neu definiert werden, um ein explizites Handle wie gezeigt zu verwenden:

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

Sie können explizite und implizite Handles in einer einzelnen Schnittstelle kombinieren. Wenn eine Funktion über ein explizites Handle in der Parameterliste verfügt, wird dieses Handle verwendet. Wenn eine Funktion in einer Schnittstelle, die implizite Handles verwendet, kein explizites Handle an gibt, wird das implizite Standardhandles verwendet.

 

 




