---
description: Hinweise zur Fehlerbehebung
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Hinweise zur Fehlerbehebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358968"
---
# <a name="troubleshooting-tips"></a>Hinweise zur Fehlerbehebung

Die folgenden Tipps helfen Ihnen, Deadlocks oder Abstürze in ihrer DirectShow-Anwendung zu vermeiden.

**Globale Objekte**

Ein globales C++-Objekt sollte keine DirectShow-Objekte in seiner Konstruktormethode erstellen oder in seiner dededemethode freigeben. Dies kann aus folgendem Grund bewirken, dass die Anwendung unbegrenzt blockiert wird:

Threads können nicht innerhalb einer DLL-Einstiegspunkt Funktion beendet werden. Kernel 32 enthält eine globale Prozess Sperre während der Einstiegspunkt Funktion, und die Sperre verhindert, dass der Thread beendet wird. Da einige DirectShow-Objekte über Threads verfügen, können Sie blockieren, wenn Sie von innerhalb einer DLL-Einstiegspunkt Funktion freigegeben werden. Wenn eine Anwendung über ein globales C++-Objekt verfügt, ruft die C-Lauf Zeit-dll den Dekonstruktor des Objekts auf, wenn die DLL entladen wird. Wenn der Dekonstruktor DirectShow-Objekte freigibt, kann dies als Ergebnis blockiert werden.

Aus ähnlichen Gründen sollte eine DLL DirectShow-Objekte nicht in der Einstiegspunkt Routine erstellen oder freigeben.

**Freigeben von Schnittstellen**

Sie sollten alle DirectShow-Schnittstellen Zeiger freigeben, während die Anwendung weiterhin Nachrichten verarbeitet, bevor die Nachrichten Schleife beendet wird. Andernfalls werden möglicherweise verschiedene Bestätigungen angezeigt, da einige DirectShow-Objekte Nachrichten während ihrer Bereinigungs Routinen senden.

(Wenn Sie die ATL **CWindowImpl** -Klasse verwenden, sollten Sie nicht warten, bis **onfinalmessage** die Schnittstellen freigibt. Verwenden Sie Sie stattdessen, wenn Sie die Meldung zum Schließen der WM verarbeiten \_ .)

**Verweis Zähler**

Wenn die Debugversion von Quartz.dll entladen wird, wird überprüft, ob DirectShow-Objekte über Verweis Zähler verfügen, die nicht freigegeben wurden. Wenn dies der Fall ist, wird eine-Behauptung ausgelöst:


```C++
g_cFGObjects == 0 
```



Wenn diese Aussage fehlschlägt, bedeutet dies, dass Ihre Anwendung einen Verweis Zähler kompromittiert hat. Überprüfen Sie den Code, und stellen Sie sicher, dass alle Schnittstellen Zeiger freigegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



