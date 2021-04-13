---
title: Zeigermoniker
description: Ein zeigermoniker identifiziert ein Objekt, das nur im aktiven oder aktiven Zustand vorhanden sein kann. Dies unterscheidet sich von anderen Klassen von Monikern, die Objekte identifizieren, die im passiven oder aktiven Zustand vorhanden sein können.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104389745"
---
# <a name="pointer-monikers"></a><span data-ttu-id="dbdda-104">Zeigermoniker</span><span class="sxs-lookup"><span data-stu-id="dbdda-104">Pointer Monikers</span></span>

<span data-ttu-id="dbdda-105">Ein *zeigermoniker* identifiziert ein Objekt, das nur im aktiven oder aktiven Zustand vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="dbdda-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="dbdda-106">Dies unterscheidet sich von anderen Klassen von Monikern, die Objekte identifizieren, die im passiven oder aktiven Zustand vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="dbdda-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="dbdda-107">Angenommen, eine Anwendung verfügt über ein Objekt, das über keine permanente Darstellung verfügt.</span><span class="sxs-lookup"><span data-stu-id="dbdda-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="dbdda-108">Wenn ein Client der Anwendung Zugriff auf dieses Objekt benötigt, können Sie den Client in der Regel einfach einem Zeiger auf das-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="dbdda-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="dbdda-109">Angenommen, der Client erwartet einen Moniker.</span><span class="sxs-lookup"><span data-stu-id="dbdda-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="dbdda-110">Das Objekt kann nicht mit einem dateimoniker identifiziert werden, weil es nicht in einer Datei gespeichert ist, und nicht mit einem elementmoniker, weil es nicht in einem anderen Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dbdda-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="dbdda-111">Stattdessen kann die Anwendung einen zeigermoniker erstellen, bei dem es sich um einen Moniker handelt, der intern einen Zeiger enthält, und diesen an den Client übergibt.</span><span class="sxs-lookup"><span data-stu-id="dbdda-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="dbdda-112">Dieser Moniker kann vom Client wie jeder andere behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="dbdda-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="dbdda-113">Wenn der Client jedoch [**IMoniker:: bindungobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für den zeigermoniker aufruft, überprüft der monikercode nicht die laufende Objekttabelle (rot) oder lädt nichts aus dem Speicher.</span><span class="sxs-lookup"><span data-stu-id="dbdda-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="dbdda-114">Stattdessen ruft der monikercode einfach [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den im Moniker gespeicherten Zeiger auf.</span><span class="sxs-lookup"><span data-stu-id="dbdda-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="dbdda-115">Zeiger Moniker erlauben, dass Objekte, die nur im Status aktiv oder wird ausgeführt werden, an monikervorgängen teilnehmen und von monikerclients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbdda-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="dbdda-116">Ein wichtiger Unterschied zwischen Zeiger Monikern und anderen Klassen von Monikern besteht darin, dass Zeiger Moniker nicht im persistenten Speicher gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="dbdda-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="dbdda-117">Wenn Sie dies tun, gibt der Aufruf der [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) -Methode einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="dbdda-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="dbdda-118">Dies bedeutet, dass Zeiger Moniker nur in speziellen Situationen nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="dbdda-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="dbdda-119">Sie können die Funktion " [**kreatepointermoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) " verwenden, wenn Sie einen zeigermoniker verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="dbdda-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbdda-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dbdda-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbdda-121">Anti-Moniker</span><span class="sxs-lookup"><span data-stu-id="dbdda-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="dbdda-122">Klassenmoniker</span><span class="sxs-lookup"><span data-stu-id="dbdda-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="dbdda-123">Zusammengesetzte Moniker</span><span class="sxs-lookup"><span data-stu-id="dbdda-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="dbdda-124">Dateimoniker</span><span class="sxs-lookup"><span data-stu-id="dbdda-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="dbdda-125">Elementmoniker</span><span class="sxs-lookup"><span data-stu-id="dbdda-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




