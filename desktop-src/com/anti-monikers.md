---
title: Anti-Moniker
description: OLE stellt eine Implementierung eines besonderen Typs von Moniker bereit, der als Anti-Moniker bezeichnet wird.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037101"
---
# <a name="anti-monikers"></a><span data-ttu-id="fe048-103">Anti-Moniker</span><span class="sxs-lookup"><span data-stu-id="fe048-103">Anti-Monikers</span></span>

<span data-ttu-id="fe048-104">OLE stellt eine Implementierung eines besonderen Typs von Moniker bereit, der als *Anti-Moniker* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="fe048-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="fe048-105">Dieser Moniker wird bei der Erstellung neuer Monikerklassen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe048-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="fe048-106">Sie verwenden Sie als Umkehrung des Monikers, auf dem Sie erstellt wurde, und den Moniker effektiv abbrechen, ähnlich wie der Operator ".." in einem Dateisystem Befehl eine Verzeichnisebene verschiebt.</span><span class="sxs-lookup"><span data-stu-id="fe048-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="fe048-107">Es muss ein-antimoniker verfügbar sein, da nach dem Erstellen eines zusammengesetzten Monikers keine Teile des Monikers gelöscht werden können, wenn z. b. ein-Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="fe048-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="fe048-108">Stattdessen verwenden Sie einen-antimoniker, um einen oder mehrere Einträge aus einem zusammengesetzten Moniker zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fe048-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="fe048-109">Anti-Moniker sind eine Monikerklasse, die explizit für die Verwendung als Umkehrung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="fe048-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="fe048-110">COM definiert die benannte Funktion " [**comateantimoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) ", die einen Anti-Moniker zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fe048-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="fe048-111">Im Allgemeinen verwenden Sie diese Funktion, um die [**IMoniker:: inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) -Methode zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="fe048-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="fe048-112">Ein Anti-Moniker ist nur eine Umkehrung für die Typen von Monikern, die implementiert werden, um antimoniker als Umkehrung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="fe048-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="fe048-113">Wenn Sie z. b. den letzten Teil eines zusammengesetzten Monikers entfernen möchten, sollten Sie keinen antimoniker erstellen und ihn am Ende der zusammengesetzten zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="fe048-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="fe048-114">Sie können nicht sicher sein, dass der letzte Teil des zusammengesetzten einen antimoniker als Umkehrung ansieht.</span><span class="sxs-lookup"><span data-stu-id="fe048-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="fe048-115">Stattdessen sollten Sie [**IMoniker:: Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) für den zusammengesetzten Moniker aufrufen und dabei **false** als ersten Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="fe048-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="fe048-116">Dadurch wird ein Enumerator erstellt, der die komponentenmoniker in umgekehrter Reihenfolge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fe048-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="fe048-117">Verwenden Sie den Enumerator, um den letzten Teil des zusammengesetzten abzurufen, und rufen Sie [**inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) für diesen Moniker auf.</span><span class="sxs-lookup"><span data-stu-id="fe048-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="fe048-118">Der von **inverse** zurückgegebene Moniker ist das, was Sie benötigen, um den letzten Teil des zusammengesetzten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fe048-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe048-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe048-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe048-120">Klassenmoniker</span><span class="sxs-lookup"><span data-stu-id="fe048-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="fe048-121">Zusammengesetzte Moniker</span><span class="sxs-lookup"><span data-stu-id="fe048-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="fe048-122">Dateimoniker</span><span class="sxs-lookup"><span data-stu-id="fe048-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="fe048-123">Elementmoniker</span><span class="sxs-lookup"><span data-stu-id="fe048-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="fe048-124">Zeigermoniker</span><span class="sxs-lookup"><span data-stu-id="fe048-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




