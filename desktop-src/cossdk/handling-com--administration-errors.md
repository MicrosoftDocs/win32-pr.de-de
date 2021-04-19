---
description: Behandeln von com+-Verwaltungsfehlern
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Behandeln von com+-Verwaltungsfehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346444"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="3c5c1-103">Behandeln von com+-Verwaltungsfehlern</span><span class="sxs-lookup"><span data-stu-id="3c5c1-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="3c5c1-104">Fehler, die bei der Verwendung der COMAdmin-Objekte generiert werden, werden auf zwei Arten wie folgt gemeldet:</span><span class="sxs-lookup"><span data-stu-id="3c5c1-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="3c5c1-105">Verwendung von für die COMAdmin-Bibliothek spezifischen Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="3c5c1-106">Verwendung erweiterter Fehlerinformationen, die in einer speziellen [**errorInfo**](errorinfo.md) -Sammlung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c5c1-107">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3c5c1-107">Error Codes</span></span>

<span data-ttu-id="3c5c1-108">Sie behandeln Verwaltungsfehler Codes wie jede beliebige com-Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="3c5c1-109">In Microsoft Visual C++ werden diese Codes als **HRESULT** -Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="3c5c1-110">In Microsoft Visual Basic werden Sie als Ausnahmen ausgelöst, die Sie erfassen können.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="3c5c1-111">Für C++-Programmierer sind die com+-Verwaltungsfehler Codes in WinError. h definiert.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="3c5c1-112">Für Visual Basic Programmierer sind Sie über die Visual Basic IDE verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="3c5c1-113">ErrorInfo-Sammlung</span><span class="sxs-lookup"><span data-stu-id="3c5c1-113">ErrorInfo Collection</span></span>

<span data-ttu-id="3c5c1-114">Wenn ein Fehler auftritt, der durch eine Art von Fehlercode signalisiert wird, sind möglicherweise ausführlichere Informationen verfügbar, abhängig von der Art des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="3c5c1-115">Die COMAdmin-Objekte bieten erweiterte Informationen in Situationen, in denen die genaue Ursache des Fehlers ohne einen detaillierten Bericht, z. b. mit mehreren Lese-und Schreibvorgängen, schwer zu bestimmen ist.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="3c5c1-116">Wenn Sie z. b. [**Methoden wie "auffüllen" und "**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) " für ein [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt verwenden, können Sie Daten für jedes Element in der Sammlung lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="3c5c1-117">Komplizierte Fehler können auftreten, und Sie können auf Grundlage eines einzelnen numerischen Fehlercodes schwierig zu diagnostizieren sein.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="3c5c1-118">Aus diesem Grund werden durch die COMAdmin-Bibliothek Erweiterte Fehlerinformationen über eine spezielle Sammlung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="3c5c1-119">Wenn erweiterte Fehlerinformationen verfügbar sind, werden Sie in der [**errorInfo**](errorinfo.md) -Auflistung platziert, die mit der ursprünglichen Auflistung verknüpft ist, in der der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="3c5c1-120">Um den Fehlerbericht abzurufen, rufen Sie die **errorInfo** -Auflistung ab, die mit der ursprünglichen Auflistung verknüpft ist, und untersuchen Sie die darin enthaltenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="3c5c1-121">Sie können die **errorInfo** -Auflistung mithilfe von [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in [**comadmincatalogcollection**](comadmincatalogcollection.md)abrufen und den zweiten Parameter leer lassen, wo Sie normalerweise die Schlüsseleigenschaft eines übergeordneten Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="3c5c1-122">Wenn Sie eine Fehlermeldung erhalten, müssen Sie die [**errorInfo**](errorinfo.md) -Auflistung sofort für die Auflistung, bei der ein Fehler aufgetreten ist, erhalten und Auffüllen, ohne weitere Vorgänge für diese Sammlung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="3c5c1-123">Andernfalls wird die **errorInfo** -Auflistung zurückgesetzt, und der Fehler wird nicht ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="3c5c1-124">Die Elemente in der [**errorInfo**](errorinfo.md) -Auflistung machen die speziellen Fehler Berichterstattungs Eigenschaften majorref und MinorRef verfügbar, die die jeweilige Ursache des Fehlers detailliert beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="3c5c1-125">Weitere Informationen finden Sie unter **errorInfo**.</span><span class="sxs-lookup"><span data-stu-id="3c5c1-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c5c1-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c5c1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c5c1-127">Com+-Verwaltungsvorgänge in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="3c5c1-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="3c5c1-128">Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog</span><span class="sxs-lookup"><span data-stu-id="3c5c1-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="3c5c1-129">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="3c5c1-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="3c5c1-130">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="3c5c1-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="3c5c1-131">Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="3c5c1-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



