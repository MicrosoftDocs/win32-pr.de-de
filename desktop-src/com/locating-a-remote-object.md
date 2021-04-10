---
title: Suchen eines Remote Objekts
description: Suchen eines Remote Objekts
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858511"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="bd669-103">Suchen eines Remote Objekts</span><span class="sxs-lookup"><span data-stu-id="bd669-103">Locating a Remote Object</span></span>

<span data-ttu-id="bd669-104">Mit der Einführung von com für verteilte Systeme verwendet com das grundlegende Modell für die Objekt Erstellung, das in [com-Klassen Objekten und CLSIDs](com-class-objects-and-clsids.md) beschrieben ist, und bietet mehr als eine Möglichkeit, ein Objekt zu finden, das sich auf einem anderen System in einem Netzwerk befinden kann, ohne die Client Anwendung zu überlasten.</span><span class="sxs-lookup"><span data-stu-id="bd669-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="bd669-105">COM hat Registrierungsschlüssel hinzugefügt, mit denen ein Server den Namen des Computers, auf dem er sich befindet, oder den Computer, auf dem sich ein vorhandener Speicher befindet, registrieren kann.</span><span class="sxs-lookup"><span data-stu-id="bd669-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="bd669-106">Daher müssen Client Anwendungen nur die CLSID des Servers kennen.</span><span class="sxs-lookup"><span data-stu-id="bd669-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="bd669-107">In Fällen, in denen es gewünscht ist, hat com jedoch einen zuvor reservierten Parameter von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) durch eine [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur ersetzt, mit der ein Client den Speicherort eines Servers angeben kann.</span><span class="sxs-lookup"><span data-stu-id="bd669-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="bd669-108">Ein weiterer wichtiger Wert in der **CoGetClassObject** -Funktion ist die [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) -Enumeration, die angibt, ob das erwartete Objekt Prozess interne, Prozess interne oder out-of-Process-Remote Vorgänge ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd669-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="bd669-109">Diese beiden Werte und die Werte in der Registrierung legen fest, wie und wo das Objekt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd669-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="bd669-110">Beim Erstellen von Instanzen kann eine Registrierungs Einstellung überschrieben werden, wenn Sie einen Server Speicherort angeben.</span><span class="sxs-lookup"><span data-stu-id="bd669-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="bd669-111">Der Algorithmus, den com hierfür verwendet, wird in der Referenz für die [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) -Enumeration beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd669-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="bd669-112">Die Remote Aktivierung hängt von der Sicherheits Beziehung zwischen Client und Server ab.</span><span class="sxs-lookup"><span data-stu-id="bd669-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="bd669-113">Weitere Informationen finden Sie unter [Sicherheit in com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="bd669-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd669-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd669-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd669-115">COM-Klassen Objekte und CLSIDs</span><span class="sxs-lookup"><span data-stu-id="bd669-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="bd669-116">Erstellen eines Objekts über ein Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="bd669-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 