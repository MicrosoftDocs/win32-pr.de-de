---
title: Initialisieren der com-Bibliothek
description: Initialisieren der com-Bibliothek
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340267"
---
# <a name="initializing-the-com-library"></a>Initialisieren der com-Bibliothek

Jedes Windows-Programm, das com verwendet, muss die com-Bibliothek initialisieren, indem die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion aufgerufen wird. Jeder Thread, der eine COM-Schnittstelle verwendet, muss einen separaten Rückruf für diese Funktion durchführen. **CoInitializeEx** hat die folgende Signatur:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



Der erste Parameter ist reserviert und muss **null** sein. Der zweite Parameter gibt das Threading Modell an, das von Ihrem Programm verwendet wird. COM unterstützt zwei verschiedene Threading Modelle, *Apartment Thread* und *Multithread*. Wenn Sie Apartment Threading angeben, haben Sie folgende Garantien:

-   Sie greifen auf jedes COM-Objekt von einem einzelnen Thread aus zu. COM-Schnittstellen Zeiger werden nicht zwischen mehreren Threads gemeinsam verwendet.
-   Der Thread verfügt über eine Nachrichten Schleife. (Siehe [Fenster Meldungen](window-messages.md) in Modul 1.)

Wenn eine dieser Einschränkungen nicht zutrifft, verwenden Sie das Multithread-Modell. Legen Sie zum Angeben des Threading Modells eines der folgenden Flags im *dwcoinit* -Parameter fest.



| Flag                          | Beschreibung         |
|-------------------------------|---------------------|
| **coinit \_ Apartmentthreaded** | Apartment Thread. |
| **coinit- \_ Multithread**     | Multithread.      |



 

Sie müssen genau eines dieser Flags festlegen. Im Allgemeinen sollte ein Thread, der ein Fenster erstellt, das **coinit \_ Apartmentthreaded** -Flag verwenden, und andere Threads sollten **coinit \_ Multithreaded** verwenden. Einige COM-Komponenten erfordern jedoch ein bestimmtes Threading Modell. In der MSDN-Dokumentation sollten Sie wissen, wann dies der Fall ist.

> [!Note]  
> Selbst wenn Sie das Apartment Threading angeben, ist es weiterhin möglich, Schnittstellen zwischen Threads mithilfe einer *Methode namens* Marshalling gemeinsam zu nutzen. Das Marshalling geht über den Rahmen dieses Moduls hinaus. Wichtig ist, dass Sie beim Apartment Threading nie einfach einen Schnittstellen Zeiger auf einen anderen Thread kopieren müssen. Weitere Informationen zu den COM-Threading Modellen finden Sie unter [Prozesse, Threads und Apartments](/windows/desktop/com/processes--threads--and-apartments).

 

Zusätzlich zu den bereits erwähnten Flags empfiehlt es sich, das kennflag " **coinit \_ deaktivierte \_ OLE1DDE** " im Parameter " *dwcoinit* " festzulegen. Wenn dieses Flag festgelegt wird, wird ein zusätzlicher Aufwand vermieden, der mit dem Objekt Verknüpfungs-und Einbettungs-und Einbettungs-1,0 (

Im folgenden wird erläutert, wie Sie com für Apartment Threading initialisieren:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



Der **HRESULT** -Rückgabetyp enthält einen Fehler-oder Erfolgs Code. Im nächsten Abschnitt sehen wir uns die com-Fehlerbehandlung an.

## <a name="uninitializing-the-com-library"></a>Aufheben der Initialisierung der com-Bibliothek

Bei jedem erfolgreichen Aufrufen von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)müssen Sie " [**zählinitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) " aufrufen, bevor der Thread beendet wird. Diese Funktion nimmt keine Parameter an und weist keinen Rückgabewert auf.


```C++
CoUninitialize();
```



## <a name="next"></a>Nächste

[Fehler Codes in com](error-codes-in-com.md)

 

 