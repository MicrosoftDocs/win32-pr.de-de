---
title: " in-, out-, size_is-Prototyp"
description: '\ in, out, size \_ ist \ Prototype verwendet ein Array mit nur einem zählenden Zeichen, das vom Client an den Server und vom Server an den Client übermittelt wird.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315374"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, size \_ ist \] Prototype

Der folgende Funktionsprototyp verwendet ein Array mit einzelnen Zeichen, das auf beide Arten übermittelt wird: vom Client zum Server und von Server zu Client:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Als \[ [**in**](/windows/desktop/Midl/in) - \] Parameter muss " *achinout* " auf der Clientseite auf einen gültigen Speicher zeigen. Der Entwickler ordnet dem Array auf der Clientseite Arbeitsspeicher zu, bevor der Remote Prozedur Aufrufe durchführen wird.

Die Stub verwenden die \[ [**Größe \_**](/windows/desktop/Midl/size-is) des \] para  meters "-Parameter", um Arbeitsspeicher auf dem Server zuzuweisen, und verwenden dann die \[ [**Länge \_**](/windows/desktop/Midl/length-is) des \] Parameters " *pcbSize* ", um die Array Elemente in diesen Speicher zu übertragen Der Entwickler muss sicherstellen, dass der Client Code die **\[ Länge \_ ist \]** variabel festlegt, bevor die Remote Prozedur aufgerufen wird.

In einigen Fällen ist die Verwendung von separaten Parametern anstelle einer einzelnen Zeichenfolge für die Eingabe und Ausgabe effizienter und bietet Flexibilität. Dies wird im folgenden Beispiel veranschaulicht:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

Im vorherigen Beispiel wird das Zeichen Array "achinout" auch als out- \[ [](/windows/desktop/Midl/out-idl) \] Parameter verwendet. In C entspricht der Name des Arrays der Verwendung eines Zeigers. Standardmäßig handelt es sich bei allen Zeigern auf oberster Ebene um Verweis Zeiger – Sie ändern nicht den Wert und zeigen auf den gleichen Arbeitsspeicher Bereich auf dem Client vor und nach dem-Rückruf. Der gesamte Arbeitsspeicher, auf den die Remote Prozedur zugreift, muss der Größe entsprechen, die der Client vor dem-Befehl angibt, oder die stubweise generiert eine Ausnahme.

Vor der Rückgabe muss die Funktion "analysieren" auf dem Server den *pcbSize* -Parameter zurücksetzen, um die Anzahl der Elemente anzugeben, die der Server wie dargestellt an den Client übertragen wird:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 