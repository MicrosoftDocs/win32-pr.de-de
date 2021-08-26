---
title: Initialisieren der COM-Bibliothek
description: Initialisieren der COM-Bibliothek
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1bc9536c186c2af3b604f7eb5666a6a31e7a845cf3b20f64a132119d16cb1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979990"
---
# <a name="initializing-the-com-library"></a>Initialisieren der COM-Bibliothek

Jedes Windows Programms, das COM verwendet, muss die COM-Bibliothek durch Aufrufen der [**CoInitializeEx-Funktion initialisieren.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Jeder Thread, der eine COM-Schnittstelle verwendet, muss einen separaten Aufruf dieser Funktion vornehmen. **CoInitializeEx** verfügt über die folgende Signatur:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



Der erste Parameter ist reserviert und muss **NULL** sein. Der zweite Parameter gibt das Threadingmodell an, das vom Programm verwendet wird. COM unterstützt zwei verschiedene Threadingmodelle: *Apartmentthreading* und *Multithreading.* Wenn Sie Apartmentthreading angeben, stellen Sie die folgenden Garantien sicher:

-   Sie greifen über einen einzelnen Thread auf jedes COM-Objekt zu. Com-Schnittstellenzeiger werden nicht zwischen mehreren Threads gemeinsam verwendet.
-   Der Thread hat eine Meldungsschleife. (Siehe [Fenstermeldungen](window-messages.md) in Modul 1.)

Wenn eine dieser Einschränkungen nicht zutrifft, verwenden Sie das Multithreadmodell. Um das Threadingmodell anzugeben, legen Sie eines der folgenden Flags im *dwCoInit-Parameter* fest.



| Flag                          | Beschreibung         |
|-------------------------------|---------------------|
| **COINIT \_ APARTMENTTHREADED** | Apartmentthreading. |
| **COINIT \_ MULTITHREADED**     | Multithreaded.      |



 

Sie müssen genau eines dieser Flags festlegen. Im Allgemeinen sollte ein Thread, der ein Fenster erstellt, das **FLAG COINIT \_ APARTMENTTHREADED** verwenden, und andere Threads sollten **COINIT \_ MULTITHREADED** verwenden. Einige COM-Komponenten erfordern jedoch ein bestimmtes Threadingmodell. Die MSDN-Dokumentation sollte Ihnen mitteilen, wann dies der Fall ist.

> [!Note]  
> Selbst wenn Sie Apartmentthreading angeben, ist es dennoch möglich, Schnittstellen zwischen Threads mithilfe einer Technik namens *Marshalling* zu teilen. Das Marshalling geht über den Rahmen dieses Moduls hinaus. Wichtig ist, dass Sie beim Apartmentthreading niemals einfach einen Schnittstellenzeiger auf einen anderen Thread kopieren dürfen. Weitere Informationen zu den COM-Threadingmodellen finden Sie unter [Prozesse, Threads und Apartment.](/windows/desktop/com/processes--threads--and-apartments)

 

Zusätzlich zu den bereits erwähnten Flags empfiehlt es sich, das **FLAG COINIT \_ DISABLE \_ OLE1DDE** im *dwCoInit-Parameter* festzulegen. Durch Das Festlegen dieses Flags wird ein zusätzlicher Aufwand vermieden, der mit ole 1.0 (Object Linking and Embedding, Objektverknüpfung und Einbettung) verbunden ist, einer veralteten Technologie.

So initialisieren Sie COM für Apartmentthreading:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



Der **HRESULT-Rückgabetyp** enthält einen Fehler- oder Erfolgscode. Wir sehen uns die COM-Fehlerbehandlung im nächsten Abschnitt an.

## <a name="uninitializing-the-com-library"></a>Aufheben der Initialisierung der COM-Bibliothek

Für jeden erfolgreichen Aufruf von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)müssen Sie [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) aufrufen, bevor der Thread beendet wird. Diese Funktion nimmt keine Parameter entgegen und hat keinen Rückgabewert.


```C++
CoUninitialize();
```



## <a name="next"></a>Nächste

[Fehlercodes in COM](error-codes-in-com.md)

 

 