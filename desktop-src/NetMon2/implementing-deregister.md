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
# <a name="implementing-deregister"></a><span data-ttu-id="17ac0-104">Implementieren von deregistern</span><span class="sxs-lookup"><span data-stu-id="17ac0-104">Implementing Deregister</span></span>

<span data-ttu-id="17ac0-105">Netzwerkmonitor übergibt alle Frames einer Erfassung an die Parser und beginnt dann mit dem Aufruf der [**deregisterfunktion**](deregister.md) für alle identifizierten Protokolle.</span><span class="sxs-lookup"><span data-stu-id="17ac0-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="17ac0-106">Jede Parser-DLL muss eine **deregiester** -Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17ac0-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="17ac0-107">Jede Implementierung der [**deregiester**](deregister.md) -Funktion muss die Funktion [**destroyprotocoldatabase**](destroypropertydatabase.md) zum Freigeben der Ressourcen, die zum Erstellen der Datenbank verwendet werden, aufruft.</span><span class="sxs-lookup"><span data-stu-id="17ac0-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="17ac0-108">Das folgende Verfahren identifiziert den einen Schritt, der zum [**Implementieren der**](deregister.md)Registrierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="17ac0-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="17ac0-109">**So implementieren Sie deregiester für ein Protokoll**</span><span class="sxs-lookup"><span data-stu-id="17ac0-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="17ac0-110">Wenden Sie [**destroyprotocoldatabase**](destroypropertydatabase.md) an, um die Datenbankressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="17ac0-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="17ac0-111">Im folgenden finden Sie eine grundlegende Implementierung von [**deregistern**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="17ac0-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="17ac0-112">Beachten Sie, dass das Codebeispiel die Freigabe von Ressourcen veranschaulicht, die zum Erstellen einer Eigenschaften Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ac0-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



