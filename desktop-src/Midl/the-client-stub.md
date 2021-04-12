---
title: Der Clientstub
description: Das Client-Stub-Modul stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Punkte auf dem Client bereit.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- Mittel l und RPC-Mittell, Schnittstellen, Clientstub
- Schnittstellen-Mittell
- Schnittstellen, Mittel l, Mittel l und RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310728"
---
# <a name="the-client-stub"></a><span data-ttu-id="73b5f-106">Der Clientstub</span><span class="sxs-lookup"><span data-stu-id="73b5f-106">The Client Stub</span></span>

<span data-ttu-id="73b5f-107">Das Client-Stub-Modul stellt für jeden Vorgang, der in der Eingabe-IDL-Datei definiert ist, Ersatz Punkte auf dem Client bereit.</span><span class="sxs-lookup"><span data-stu-id="73b5f-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="73b5f-108">Wenn die Client Anwendung eine Remote Prozedur aufruft, wird der zugehörige-Befehl zuerst an die Ersatz Routine in der Client-Stub-Datei weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="73b5f-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="73b5f-109">Die Client-Stub-Routine führt die folgenden Funktionen aus:</span><span class="sxs-lookup"><span data-stu-id="73b5f-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="73b5f-110">Marshalls-Argumente.</span><span class="sxs-lookup"><span data-stu-id="73b5f-110">Marshals arguments.</span></span> <span data-ttu-id="73b5f-111">Der Client-Stub verpackt Eingabeargumente in ein Formular, das an den Server übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="73b5f-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="73b5f-112">Ruft die Client Lauf Zeit Bibliothek auf, um Argumente an den Remote Adressraum zu übertragen, und ruft die Remote Prozedur im Server Adressbereich auf.</span><span class="sxs-lookup"><span data-stu-id="73b5f-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="73b5f-113">Gibt Ausgabe Argumente aus.</span><span class="sxs-lookup"><span data-stu-id="73b5f-113">Unmarshals output arguments.</span></span> <span data-ttu-id="73b5f-114">Der Client-Stub entpackt Ausgabe Argumente und kehrt zum Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="73b5f-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="73b5f-115">Der-Compilerschalter [**/Client**](-client.md), [**/cstub**](-cstub.md)und [**/out**](-out.md) wirkt sich auf die Client-Stub-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="73b5f-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




