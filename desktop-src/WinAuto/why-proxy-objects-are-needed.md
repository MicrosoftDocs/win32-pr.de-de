---
title: Warum Proxy Objekte erforderlich sind
description: Bei zugänglichen Objekten wird die dll, in der die Hook-Funktion des Clients implementiert ist, in den Adressbereich des Servers geladen, wenn ein Client eine kontextbasierte Hook-Funktion festlegt.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309999"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="3b3f1-103">Warum Proxy Objekte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="3b3f1-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="3b3f1-104">Bei zugänglichen Objekten wird die dll, in der die Hook-Funktion des Clients implementiert ist, in den Adressbereich des Servers geladen, wenn ein Client eine [kontextbasierte Hook-Funktion](in-context-and-out-of-context-hook-functions.md)festlegt.</span><span class="sxs-lookup"><span data-stu-id="3b3f1-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="3b3f1-105">Wenn der Client in diesem Fall [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) von der Hook-Funktion aus aufruft, zeigt der Schnittstellen Zeiger, der zurückgegeben wird, direkt auf den Code im Adressbereich des Servers.</span><span class="sxs-lookup"><span data-stu-id="3b3f1-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="3b3f1-106">Wenn der Client eine Schnittstellen Eigenschaft mithilfe dieses Zeigers aufruft, ist die Component Object Model (com)-Bibliothek nicht an Marshalling oder Unmarshalling beteiligt und kann nicht erkennen, ob ein Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="3b3f1-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="3b3f1-107">Daher muss der Server diese Situation erkennen und einen Fehlercode an den Client zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3b3f1-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




