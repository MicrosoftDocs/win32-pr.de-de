---
description: Nachdem Sie eine DLL erstellt haben, können Sie die Funktionen verwenden, die in einer Anwendung definiert sind. Im folgenden finden Sie eine einfache Konsolenanwendung, die die Funktion "myputs" verwendet, die aus Myputs.dll exportiert wird (siehe Erstellen einer einfachen Dynamic-Link Bibliothek).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Verwenden Load-Time dynamischen Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345856"
---
# <a name="using-load-time-dynamic-linking"></a>Verwenden Load-Time dynamischen Verknüpfungen

Nachdem Sie eine DLL erstellt haben, können Sie die Funktionen verwenden, die in einer Anwendung definiert sind. Im folgenden finden Sie eine einfache Konsolenanwendung, die die Funktion "myputs" verwendet, die aus Myputs.dll exportiert wird (siehe [Erstellen einer einfachen Dynamic-Link Bibliothek](creating-a-simple-dynamic-link-library.md)).

Da in diesem Beispiel die DLL-Funktion explizit aufgerufen wird, muss das Modul für die Anwendung mit der Import Bibliothek myputs. lib verknüpft werden. Weitere Informationen zum Entwickeln von DLLs finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.


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

[Dynamische Verknüpfung der Ladezeit](load-time-dynamic-linking.md)
</dt> </dl>

 

 



