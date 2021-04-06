---
title: Der Standard Handler und benutzerdefinierte Handler
description: Der Standard Handler und benutzerdefinierte Handler
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947539"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="040f9-103">Der Standard Handler und benutzerdefinierte Handler</span><span class="sxs-lookup"><span data-stu-id="040f9-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="040f9-104">Der Standard Handler, eine von OLE bereitgestellte Implementierung, wird von den meisten Anwendungen als Handler verwendet.</span><span class="sxs-lookup"><span data-stu-id="040f9-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="040f9-105">Eine Anwendung implementiert einen benutzerdefinierten Handler, wenn die Funktionen des Standard Handlers nicht ausreichen.</span><span class="sxs-lookup"><span data-stu-id="040f9-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="040f9-106">Ein benutzerdefinierter Handler kann entweder den Standard Handler vollständig ersetzen oder Teile der Funktionalität verwenden, die er ggf. bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="040f9-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="040f9-107">Im letzteren Fall wird der Anwendungs Handler als Aggregat Objekt implementiert, das aus einem neuen Steuerelement Objekt und dem Standard Handler besteht.</span><span class="sxs-lookup"><span data-stu-id="040f9-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="040f9-108">Kombinationen von Anwendungs-/standardhandlern werden auch als *Prozess interne Handler* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="040f9-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="040f9-109">Der *Remoting-Handler* wird für Objekte verwendet, denen keine CLSID in der Systemregistrierung zugewiesen ist oder für die kein Handler festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="040f9-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="040f9-110">Für diese Objekttypen müssen lediglich Informationen über die Prozess Grenze hinweg übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="040f9-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="040f9-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="040f9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="040f9-112">Objekt Handler</span><span class="sxs-lookup"><span data-stu-id="040f9-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




