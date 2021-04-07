---
title: Fehler Codes in com
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725385"
---
# <a name="error-codes-in-com"></a>Fehler Codes in com

Um den Erfolg oder Misserfolg anzuzeigen, geben com-Methoden und-Funktionen einen Wert vom Typ **HRESULT** zurück. Ein **HRESULT** ist eine 32-Bit-Ganzzahl. Das höchst wertige Bit des **HRESULT** signalisiert Erfolg oder Fehler. NULL (0) gibt den Erfolg an, und 1 gibt einen Fehler an.

Dies erzeugt die folgenden numerischen Bereiche:

-   Erfolgs Codes: 0x0 – 0x7FFFFFFF.
-   Fehlercodes: 0x80000000 – 0xFFFFFFFF.

Eine kleine Anzahl von com-Methoden gibt keinen **HRESULT** -Wert zurück. Beispielsweise geben die Methoden " [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) " und " [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) " nicht signierte Long-Werte zurück. Jede com-Methode, die einen Fehlercode zurückgibt, bewirkt jedoch, dass ein **HRESULT** -Wert zurückgegeben wird.

Um zu überprüfen, ob eine com-Methode erfolgreich ist, überprüfen Sie das höchst wertige Bit des zurückgegebenen **HRESULT**. Die Windows SDK-Header bieten zwei Makros, die dies vereinfachen: das Makro " [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) " und das [**fehlgeschlagene**](/windows/desktop/api/winerror/nf-winerror-failed) Makro. Das Makro " **erfolgreich** " gibt **true** zurück, wenn ein **HRESULT** ein Erfolgs Code ist, und **false** , wenn es sich um einen Fehlercode handelt. Im folgenden Beispiel wird überprüft, ob [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) erfolgreich ist.


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



Manchmal ist es bequemer, die umgekehrte Bedingung zu testen. Das [**fehlgeschlagene**](/windows/desktop/api/winerror/nf-winerror-failed) Makro bewirkt, dass das Gegenteil von [**erfolgreich war**](/windows/desktop/api/winerror/nf-winerror-succeeded). Sie gibt **true** für einen Fehlercode und **false** für einen Erfolgs Code zurück.


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



Später in diesem Modul betrachten wir einige praktische Ratschläge, wie Sie Ihren Code für die Behandlung von com-Fehlern strukturieren. (Siehe [Fehlerbehandlung in com](error-handling-in-com.md).)

## <a name="next"></a>Nächste

[Erstellen eines Objekts in com](creating-an-object-in-com.md)

 

 