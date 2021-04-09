---
title: Verschieben von Objekten
description: Verschieben von Objekten
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Verschieben von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038747"
---
# <a name="moving-objects"></a><span data-ttu-id="a9543-104">Verschieben von Objekten</span><span class="sxs-lookup"><span data-stu-id="a9543-104">Moving Objects</span></span>

<span data-ttu-id="a9543-105">Verwenden Sie die [**IADsContainer. movehere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) -Methode, um ein Objekt innerhalb einer Domäne zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="a9543-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="a9543-106">**So verschieben Sie ein Objekt innerhalb einer Domäne**</span><span class="sxs-lookup"><span data-stu-id="a9543-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="a9543-107">Binden an die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle des zu verschiebenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9543-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="a9543-108">Ruft den ADsPath des Objekts ab, das aus der [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9543-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="a9543-109">Binden Sie an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle des Containers, in den das Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a9543-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="a9543-110">Verschieben Sie das Objekt mit der [**IADsContainer. movehere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a9543-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="a9543-111">Wenn eine Schnittstelle für das Objekt vorhanden ist, das verschoben wurde, ist die Schnittstelle nach dem Verschieben des Objekts ungültig, da das Verzeichnis Objekt, das die Schnittstelle darstellt, nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a9543-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="a9543-112">Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Objekt verschoben wird, finden Sie unter [Beispielcode zum Verschieben eines Objekts](example-code-for-moving-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="a9543-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 