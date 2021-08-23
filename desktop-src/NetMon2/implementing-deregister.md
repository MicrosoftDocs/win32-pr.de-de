---
description: Netzwerkmonitor alle Frames einer Erfassung an die Parser übergeben und dann mit dem Aufrufen der Deregister-Funktion für alle identifizierten Protokolle gestartet. Jede Parser-DLL muss eine Deregister-Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementieren der Registrierung aufheben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444502ba3ab19921a6372d4cda872aed85e879cbbdadc2f0176a7187bfc24491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890480"
---
# <a name="implementing-deregister"></a>Implementieren der Registrierung aufheben

Netzwerkmonitor alle Frames einer Erfassung an die Parser übergeben und dann mit dem Aufrufen der [**Deregister-Funktion**](deregister.md) für alle identifizierten Protokolle gestartet. Jede Parser-DLL muss eine **Deregister-Funktion** für jedes Protokoll implementieren, das die Parser-DLL unterstützt.

Jede Implementierung der [**Deregister-Funktion**](deregister.md) muss die [**DestroyProtocolDatabase-Funktion**](destroypropertydatabase.md) aufrufen, um die Ressourcen frei zu geben, die zum Erstellen der Datenbank verwendet werden.

Im folgenden Verfahren wird der schritt identifiziert, der zum Implementieren der Registrierung aufheben [**erforderlich ist.**](deregister.md)

**So implementieren Sie Die Registrierung aufheben für ein Protokoll**

-   Rufen [**Sie DestroyProtocolDatabase auf,**](destroypropertydatabase.md) um die Datenbankressourcen frei zu geben.

Im Folgenden finden Sie eine grundlegende Implementierung von [**Aufheben der Registrierung**](deregister.md)von . Beachten Sie, dass das Codebeispiel die Freigabe von Ressourcen zeigt, die zum Erstellen einer Eigenschaftendatenbank verwendet werden.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



