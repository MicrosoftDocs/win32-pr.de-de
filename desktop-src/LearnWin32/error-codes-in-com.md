---
title: Fehlercodes in COM
description: Fehlercodes in COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dd61208c9ae825999ec0dec024a8cc492b81cae426b1cc4143d694034204d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388288"
---
# <a name="error-codes-in-com"></a>Fehlercodes in COM

Com-Methoden und -Funktionen geben einen Wert vom Typ **HRESULT** zurück, um einen Erfolg oder Fehler anzugeben. Ein **HRESULT** ist eine 32-Bit-Ganzzahl. Das hochgeordnete Bit des **HRESULT** signalisiert Erfolg oder Fehler. Null (0) gibt den Erfolg an, und 1 gibt einen Fehler an.

Dadurch werden die folgenden numerischen Bereiche erzeugt:

-   Erfolgscodes: 0x0–0x7FFFFFFF.
-   Fehlercodes: 0x80000000–0xFFFFFFFF.

Eine kleine Anzahl von COM-Methoden gibt keinen **HRESULT-Wert** zurück. Beispielsweise geben die [**Methoden AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) lange Werte ohne Vorzeichen zurück. Jede COM-Methode, die einen Fehlercode zurückgibt, gibt jedoch einen **HRESULT-Wert** zurück.

Um zu überprüfen, ob eine COM-Methode erfolgreich ist, untersuchen Sie das obere Bit des zurückgegebenen **HRESULT.** Die Windows SDK-Header stellen zwei Makros bereit, die dies vereinfachen: das [**SUCCEEDED-Makro**](/windows/desktop/api/winerror/nf-winerror-succeeded) und das [**FAILED-Makro.**](/windows/desktop/api/winerror/nf-winerror-failed) Das **SUCCEEDED-Makro** gibt **TRUE** zurück, wenn ein **HRESULT** ein Erfolgscode ist, und **FALSE,** wenn es sich um einen Fehlercode handelt. Im folgenden Beispiel wird überprüft, ob [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) erfolgreich ist.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



Manchmal ist es praktischer, die umgekehrte Bedingung zu testen. Das [**FAILED-Makro**](/windows/desktop/api/winerror/nf-winerror-failed) führt das Gegenteil von [**SUCCEEDED aus.**](/windows/desktop/api/winerror/nf-winerror-succeeded) Sie gibt **TRUE** für einen Fehlercode und **FALSE** für einen Erfolgscode zurück.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



Später in diesem Modul werden einige praktische Hinweise zum Strukturieren Ihres Codes zur Behandlung von COM-Fehlern behandelt. (Siehe [Fehlerbehandlung in COM](error-handling-in-com.md).)

## <a name="next"></a>Nächste

[Erstellen eines Objekts in COM](creating-an-object-in-com.md)

 

 
