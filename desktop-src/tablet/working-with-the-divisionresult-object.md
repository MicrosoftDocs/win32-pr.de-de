---
description: Das DivisionResult-Objekt stellt eine Momentaufnahme der Layoutanalyse der Striche dar, die im Divider-Objekt enthalten sind. Sie enthält die Informationen zur Strich Klassifizierung und-Gruppierung aus der Layoutanalyse.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Arbeiten mit dem DivisionResult-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526888"
---
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="ce4db-104">Arbeiten mit dem DivisionResult-Objekt</span><span class="sxs-lookup"><span data-stu-id="ce4db-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="ce4db-105">Das **DivisionResult** -Objekt stellt eine Momentaufnahme der Layoutanalyse der Striche dar, die im **Divider** -Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ce4db-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="ce4db-106">Sie enthält die Informationen zur Strich Klassifizierung und-Gruppierung aus der Layoutanalyse.</span><span class="sxs-lookup"><span data-stu-id="ce4db-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="ce4db-107">Sie können Informationen aus dem **DivisionResult** -Objekt nach Struktur Elementtyp (z. b. zeichnen oder Zeilen der Handschrift) erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce4db-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="ce4db-108">Das **DivisionResult** -Objekt kann beibehalten werden, nachdem das **Divider** -Objekt zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="ce4db-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="ce4db-109">In Automation wird dieses Objekt als [**iinkdivisionresult-Schnittstellen**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) Objekt bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ce4db-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="ce4db-110">Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft des **DivisionResult** -Objekts enthält eine Kopie der **Striche** -Auflistung im **Divider** -Objekt zum Zeitpunkt der Erstellung des **DivisionResult** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ce4db-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="ce4db-111">Die [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) -Enumeration definiert die Strukturelement Typen, die von der Layoutanalyse erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="ce4db-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="ce4db-112">Die [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) -Methode des **DivisionResult** -Objekts gibt eine **DivisionUnits** -Auflistung zurück, die alle strukturellen Elemente eines bestimmten Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="ce4db-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="ce4db-113">Ein einzelnes Strukturelement wird durch ein **DivisionUnit** -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce4db-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="ce4db-114">Jedes Mal, wenn Sie die Methode " **ResultByType** " aufzurufen, erstellt das **DivisionResult** -Objekt eine **DivisionUnits** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ce4db-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="ce4db-115">Weitere Informationen zum **DivisionUnit** -Objekt finden Sie unter [Arbeiten mit dem DivisionUnit-Objekt](working-with-the-divisionunit-object.md).</span><span class="sxs-lookup"><span data-stu-id="ce4db-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
