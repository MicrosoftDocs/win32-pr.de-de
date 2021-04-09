---
title: Die midl_user_allocate-Funktion
description: Die Funktion "Mittel l- \_ Benutzer \_ zuweisen" ist ein Verfahren, das von Entwicklern von RPC-Anwendungen bereitgestellt werden muss.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102006"
---
# <a name="the-midl_user_allocate-function"></a>Die Funktion "Mittel l- \_ Benutzer \_ zuweisen"

Die Funktion " **Mittel l- \_ Benutzer \_ zuweisen** " ist ein Verfahren, das von Entwicklern von RPC-Anwendungen bereitgestellt werden muss. Dadurch wird Arbeitsspeicher für die RPC-stubspeicher und Bibliotheks Routinen zugewiesen. Die Funktion " **Mittel l- \_ Benutzer \_ Zuordnung** " muss dem folgenden Prototyp entsprechen:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

Der *cbytes* -Parameter gibt die Anzahl der zuzuordnenden Bytes an. Sowohl Client Anwendungen als auch Server Anwendungen müssen die Funktion " **Mittell- \_ Benutzer \_ zuweisen** " implementieren, es sei denn, Sie kompilieren ihn im OSF-Kompatibilitätsmodus (/OSF). Von Anwendungen und generierten stubjekten wird die **\_ \_ Zuordnung von Benutzer** Zuordnungen direkt oder indirekt zum Verwalten zugewiesener Objekte aufgerufen. Beispiel:

-   Die Client-und Server Anwendungen wenden die Benutzer Zuordnungen für den **\_ Benutzer \_** an, um Arbeitsspeicher für die Anwendung zuzuweisen, z. b. Wenn ein neuer Knoten in einer Struktur oder verknüpften Liste erstellt wird
-   Der Serverstub Ruft beim Marshalling von Daten in den Server Adressraum die **mittlere \_ Benutzer \_** Zuordnungen auf.
-   Der Clientstub Ruft bei der Aufhebung des Marshalling von Daten von dem Server, auf den von einem out-Zeiger verwiesen wird, die Benutzer Zuordnungen für **mittlere \_ Benutzer \_** auf \[ \] Beachten Sie, \[ dass \] \[ \] der Client-Stub bei in-, out-und \[ Unique \] -Zeigern nur dann die **\_ Benutzer \_** Zuordnungen aufruft, wenn der \[ eindeutige \] Zeiger Wert bei Eingabe NULL war und während des Aufrufs zu einem Wert ungleich NULL wechselt. Wenn der \[ eindeutige \] Zeiger bei Eingabe ungleich Null war, schreibt der Clientstub die zugeordneten Daten in den vorhandenen Arbeitsspeicher.

Wenn die Benutzer Zuordnungen von **\_ Benutzer \_** Zuordnungen keinen Arbeitsspeicher zuordnen können, sollte ein NULL-Zeiger zurückgegeben werden.

Die **\_ Benutzer \_** Zuordnungs Funktion "Mittel l" sollte einen 8-Byte-ausgerichteten Zeiger zurückgeben.

Beispielsweise implementieren die Beispiel Programme, die mit dem Platform Software Development Kit (SDK) bereitgestellt werden, eine **mittlere \_ Benutzer \_** Zuordnungen im Hinblick auf die C-Funktion [**malloc**](pointers-and-memory-allocation.md):


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Wenn das RPCSS-Paket aktiviert ist (z. b. als Ergebnis der Verwendung des \[ Attributs " [**\_ zuordnen**](/windows/desktop/Midl/enable-allocate) " \] ), verwenden Sie " [**rpcsmallo"**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) , um Arbeitsspeicher auf der Serverseite zuzuweisen. Weitere Informationen zum Aktivieren von " \[ **\_ zuordnen**" \] finden Sie unter " [Mittel l Reference](/windows/desktop/Midl/midl-language-reference)".

 

 

 