---
description: Hinweise zur Fehlerbehebung
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Hinweise zur Fehlerbehebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fe361af291c29f8784235066f341d940ab38205cd3b8238896011f85021a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651242"
---
# <a name="troubleshooting-tips"></a>Hinweise zur Fehlerbehebung

Die folgenden Tipps helfen Ihnen, Deadlocks oder Abstürze in Ihrer DirectShow-Anwendung zu vermeiden.

**Globale Objekte**

Ein globales C++-Objekt sollte keine DirectShow-Objekte in seiner Konstruktormethode erstellen oder in seiner Destruktormethode veröffentlichen. Dies kann dazu führen, dass die Anwendung aus folgendem Grund unbegrenzt blockiert wird:

Threads können innerhalb der Einstiegspunktfunktion einer DLL nicht beendet werden. Kernel 32 enthält eine globale Prozesssperre während der Einstiegspunktfunktion, und die Sperre verhindert, dass der Thread beendet wird. Da einige DirectShow-Objekte Threads besitzen, können sie blockiert werden, wenn sie innerhalb einer DLL-Einstiegspunktfunktion freigegeben werden. Wenn eine Anwendung über ein globales C++-Objekt verfügt, ruft die C-Laufzeit-DLL den Destruktor des Objekts auf, wenn die DLL entladen wird. Wenn der Destruktor DirectShow-Objekte frei gibt, kann er als Ergebnis blockieren.

Aus ähnlichen Gründen sollte eine DLL keine DirectShow-Objekte in ihrer Einstiegspunktroutine erstellen oder veröffentlichen.

**Freigeben von Schnittstellen**

Sie sollten alle DirectShow-Schnittstellenzeker frei geben, während Ihre Anwendung noch Nachrichten verarbeitet, bevor die Nachrichtenschleife beendet wird. Andernfalls werden möglicherweise verschiedene Asserts angezeigt, da einige DirectShow-Objekte während ihrer Bereinigungsroutinen Nachrichten senden.

(Wenn Sie die ATL **CWindowImpl-Klasse** verwenden, warten Sie nicht, bis **OnFinalMessage** die Schnittstellen frei gibt. Geben Sie sie stattdessen frei, wenn Sie die WM \_ CLOSE-Nachricht behandeln.)

**Verweisanzahl**

Wenn die Debugversion von Quartz.dll wird überprüft, ob DirectShow-Objekte Verweiszähler haben, die nicht freigegeben wurden. Wenn dies der Fall ist, wird eine Assertion auslösen:


```C++
g_cFGObjects == 0 
```



Wenn bei dieser Assertion ein Fehler auftritt, bedeutet dies, dass ihre Anwendung eine Verweisanzahl verfleckt hat. Überprüfen Sie Ihren Code, und stellen Sie sicher, dass Sie alle Schnittstellenzeker frei geben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



