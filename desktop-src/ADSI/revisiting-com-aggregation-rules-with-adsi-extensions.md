---
title: Rebesuchen von com-Aggregations Regeln mit ADSI-Erweiterungen
description: Im folgenden finden Sie eine kurze Überprüfung der com-Aggregations-und ADSI-Erweiterungs Regeln.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, com-Aggregations Regeln
- COM-Aggregations-ADSI
- Rebesuchen von com-Aggregations Regeln mit ADSI Extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730257"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="27155-106">Rebesuchen von com-Aggregations Regeln mit ADSI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="27155-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="27155-107">Im folgenden finden Sie eine kurze Überprüfung der com-Aggregations-und ADSI-Erweiterungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="27155-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="27155-108">Die Methode " **kreatanstance** " gibt wie folgt einen Zeiger auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle zurück, die keine Funktionsaufrufe an den Aggregator delegiert.</span><span class="sxs-lookup"><span data-stu-id="27155-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="27155-109">Die [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode gibt Zeiger auf die unterstützten Schnittstellen und Fehler für Schnittstellen zurück, die Sie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27155-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="27155-110">Die [**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode erhöht den Verweis Zähler für das aggregierte Erweiterungs Objekt selbst.</span><span class="sxs-lookup"><span data-stu-id="27155-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="27155-111">Die [**iunkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode Dekremente den Verweis Zähler für das aggregierte Erweiterungs Objekt selbst und zerstört sich selbst, wenn der Verweis Zähler 0 ist.</span><span class="sxs-lookup"><span data-stu-id="27155-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="27155-112">Das Erweiterungs Objekt sollte den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger des Aggregators (z. b. m \_ pouterunknown) während der Implementierung der Methode " **kreateinstance** " speichern.</span><span class="sxs-lookup"><span data-stu-id="27155-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="27155-113">Alle Schnittstellen, die das Erweiterungs Objekt unterstützt (einschließlich [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)), sollten von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)erben, das alle Funktionsaufrufe an den Aggregator zurück delegiert.</span><span class="sxs-lookup"><span data-stu-id="27155-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="27155-114">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ruft "m \_ pouterunknown->QueryInterface" auf</span><span class="sxs-lookup"><span data-stu-id="27155-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="27155-115">[**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ruft "m \_ pouterunknown->adressf" auf</span><span class="sxs-lookup"><span data-stu-id="27155-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="27155-116">[**Iunkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ruft "m \_ pouterunknown->Release" auf</span><span class="sxs-lookup"><span data-stu-id="27155-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="27155-117">Erweiterungs Schreiber können eine beliebige interne Implementierung auswählen, die Sie bevorzugen, sofern Sie den standardmäßigen com-Aggregations Regeln folgen.</span><span class="sxs-lookup"><span data-stu-id="27155-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="27155-118">Beachten Sie, dass ein Erweiterungs Objekt nicht als eigenständiges Objekt funktionieren muss.</span><span class="sxs-lookup"><span data-stu-id="27155-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="27155-119">Erweiterungen sind so konzipiert, dass Sie als Aggregate funktionieren.</span><span class="sxs-lookup"><span data-stu-id="27155-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="27155-120">Eine Erweiterung kann jedoch so geschrieben werden, dass Sie sowohl als eigenständiges Objekt als auch als Aggregat funktioniert.</span><span class="sxs-lookup"><span data-stu-id="27155-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="27155-121">Zusätzlich zur Standard-com-Aggregations Unterstützung unterstützt ein Erweiterungs Objekt [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) für erweiterte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="27155-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="27155-122">Wenn die späte Bindung unterstützt wird, sollte die Erweiterung wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="27155-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="27155-123">Delegieren Sie Funktionen für [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück an den Aggregator.</span><span class="sxs-lookup"><span data-stu-id="27155-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="27155-124">Implementieren Sie die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle in [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="27155-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 