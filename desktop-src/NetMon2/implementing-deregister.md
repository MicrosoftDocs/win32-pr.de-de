---
description: Netzwerkmonitor übergibt alle Frames einer Erfassung an die Parser und beginnt dann mit dem Aufruf der deregisterfunktion für alle identifizierten Protokolle. Jede Parser-DLL muss eine deregiester-Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementieren von deregistern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346096"
---
# <a name="implementing-deregister"></a>Implementieren von deregistern

Netzwerkmonitor übergibt alle Frames einer Erfassung an die Parser und beginnt dann mit dem Aufruf der [**deregisterfunktion**](deregister.md) für alle identifizierten Protokolle. Jede Parser-DLL muss eine **deregiester** -Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.

Jede Implementierung der [**deregiester**](deregister.md) -Funktion muss die Funktion [**destroyprotocoldatabase**](destroypropertydatabase.md) zum Freigeben der Ressourcen, die zum Erstellen der Datenbank verwendet werden, aufruft.

Das folgende Verfahren identifiziert den einen Schritt, der zum [**Implementieren der**](deregister.md)Registrierung erforderlich ist.

**So implementieren Sie deregiester für ein Protokoll**

-   Wenden Sie [**destroyprotocoldatabase**](destroypropertydatabase.md) an, um die Datenbankressourcen freizugeben.

Im folgenden finden Sie eine grundlegende Implementierung von [**deregistern**](deregister.md). Beachten Sie, dass das Codebeispiel die Freigabe von Ressourcen veranschaulicht, die zum Erstellen einer Eigenschaften Datenbank verwendet werden.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



