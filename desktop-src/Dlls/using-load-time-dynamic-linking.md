---
description: Nachdem Sie eine DLL erstellt haben, können Sie die Funktionen verwenden, die sie in einer Anwendung definiert. Im Folgenden finden Sie eine einfache Konsolenanwendung, die die aus Myputs.dll exportierte myPuts-Funktion verwendet (siehe Erstellen einer einfachen Dynamic-Link Library).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Verwenden Load-Time dynamischen Verknüpfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106d9d73808b56c664e44d8dcd71b74a65431316fd3daf47dd0736596c5aa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902370"
---
# <a name="using-load-time-dynamic-linking"></a>Verwenden Load-Time dynamischen Verknüpfung

Nachdem Sie eine DLL erstellt haben, können Sie die Funktionen verwenden, die sie in einer Anwendung definiert. Im Folgenden finden Sie eine einfache Konsolenanwendung, die die aus Myputs.dll exportierte myPuts-Funktion verwendet (siehe [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).

Da in diesem Beispiel die DLL-Funktion explizit aufruft, muss das Modul für die Anwendung mit der Importbibliothek Myputs.lib verknüpft werden. Weitere Informationen zum Erstellen von DLLs finden Sie in der Dokumentation zu Ihren Entwicklungstools.


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamische Verknüpfung zur Ladezeit](load-time-dynamic-linking.md)
</dt> </dl>

 

 



