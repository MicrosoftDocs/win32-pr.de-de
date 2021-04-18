---
description: Der Wert der Eigenschaft "betreffzusammenfassung" überträgt den Namen des Produkts, der Transformation oder des Patches, das vom Paket installiert wird.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Subject Summary-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364920"
---
# <a name="subject-summary-property"></a><span data-ttu-id="5ab90-103">Subject Summary-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5ab90-103">Subject Summary property</span></span>

<span data-ttu-id="5ab90-104">Der Wert der Eigenschaft " **betreffzusammenfassung** " überträgt den Namen des Produkts, der Transformation oder des Patches, das vom Paket installiert wird.</span><span class="sxs-lookup"><span data-stu-id="5ab90-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="5ab90-105">Es liegt an der Erstellung einer Installations Datenbank, einer Transformation oder eines Patchpakets, um den Wert dieser Eigenschaft in den Zusammenfassungs Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5ab90-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="5ab90-106">Autoren sollten die folgenden Schritte ausführen, um den richtigen Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5ab90-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="5ab90-107">Legen Sie die Eigenschaft für die **betreffzusammenfassung** in einem Installationspaket auf denselben Wert fest wie die [**ProductName**](productname.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5ab90-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="5ab90-108">Legen Sie die Eigenschaft für die **betreffzusammenfassung** in einer Transformation auf denselben Wert wie die Eigenschaft für die **betreffzusammenfassung** im ursprünglichen Installationspaket fest.</span><span class="sxs-lookup"><span data-stu-id="5ab90-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="5ab90-109">Legen Sie die Eigenschaft für die **betreffzusammenfassung** in den Zusammenfassungs Informationen eines Patchpakets auf eine kurze Beschreibung des Patches fest, der den Namen des Produkts enthält.</span><span class="sxs-lookup"><span data-stu-id="5ab90-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab90-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ab90-110">Requirements</span></span>



| <span data-ttu-id="5ab90-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ab90-111">Requirement</span></span> | <span data-ttu-id="5ab90-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab90-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab90-113">Version</span><span class="sxs-lookup"><span data-stu-id="5ab90-113">Version</span></span><br/> | <span data-ttu-id="5ab90-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ab90-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ab90-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ab90-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ab90-116">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="5ab90-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ab90-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ab90-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab90-118">**Patchnewsummarysubject**</span><span class="sxs-lookup"><span data-stu-id="5ab90-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="5ab90-119">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ab90-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




