---
title: " in, out, size_is Prototype"
description: '\ in, out, size is\ prototype verwendet ein Array mit einzel gezählten Zeichen, das vom Client an den Server und vom Server an den \_ Client übergeben wird.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623dc39e9bd18fdd0c7bc02f008ccc1c16919362fd2a52e373abdde762eb726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073640"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, size \_ ist \] Prototype

Der folgende Funktionsprototyp verwendet ein Einzählungszeichenarray, das auf beide Arten übergeben wird: vom Client zum Server und vom Server zum Client:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Als \[ [**in-Parameter**](/windows/desktop/Midl/in) \] muss *"sollenInOut"* auf einen gültigen Speicher auf clientseitiger Seite verweisen. Der Entwickler ordnet dem Array auf Clientseite zugeordneten Arbeitsspeicher zu, bevor er den Remoteprozeduraufruf vorgibt.

Die Stubs verwenden den Parameter size is strsize, um Arbeitsspeicher auf dem Server zu reservieren, und verwenden dann den \[ [**\_**](/windows/desktop/Midl/size-is) \] length  \[ [**\_ is-Parameter**](/windows/desktop/Midl/length-is) \] *"sizeSize",* um die Arrayelemente in diesen Speicher zu übertragen. Der Entwickler muss vor dem Aufrufen der Remoteprozedur sicherstellen, dass der Clientcode die **\[ Länge \_ \]** als variable festgelegt hat.

In einigen Situationen ist die Verwendung separater Parameter anstelle einer einzelnen Zeichenfolge für die Eingabe und Ausgabe effizienter und bietet Flexibilität. Dies wird im nächsten Beispiel gezeigt:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

Im vorherigen Beispiel wird das Zeichenarray "erhaltenInOut" auch als \[ [**out-Parameter**](/windows/desktop/Midl/out-idl) \] verwendet. In C entspricht der Name des Arrays der Verwendung eines Zeigers. Standardmäßig sind alle Zeiger der obersten Ebene Verweiszeler– sie ändern sich nicht im Wert und zeigen auf denselben Speicherbereich auf dem Client vor und nach dem Aufruf. Der Arbeitsspeicher, auf den die Remoteprozedur zutritt, muss der Vom Client vor dem Aufruf angegebenen Größe passen, oder die Stubs generieren eine Ausnahme.

Vor der Rückgabe muss die Analyze-Funktion auf dem Server den *parameter "polarSize"* zurücksetzen, um die Anzahl der Elemente anzugeben, die der Server wie gezeigt an den Client überträgt:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 