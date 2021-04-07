---
description: Stellt eine beliebige Auflistung im com+-Katalog dar. Verwenden Sie diese Option, um Elemente in einer Auflistung aufzulisten, hinzuzufügen, zu entfernen und abzurufen und um auf verwandte Auflistungen zuzugreifen.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Comadmincatalogcollection-Klasse (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748664"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="c6b72-104">Comadmincatalogcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6b72-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="c6b72-105">Stellt eine beliebige Auflistung im com+-Katalog dar.</span><span class="sxs-lookup"><span data-stu-id="c6b72-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="c6b72-106">Verwenden Sie diese Option, um Elemente in einer Auflistung aufzulisten, hinzuzufügen, zu entfernen und abzurufen und um auf verwandte Auflistungen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c6b72-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c6b72-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="c6b72-107">When to implement</span></span>

<span data-ttu-id="c6b72-108">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6b72-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="c6b72-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6b72-109">Requirement</span></span> | <span data-ttu-id="c6b72-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c6b72-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="c6b72-111">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c6b72-111">Interfaces</span></span> | [<span data-ttu-id="c6b72-112">**Icatalogcollection**</span><span class="sxs-lookup"><span data-stu-id="c6b72-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="c6b72-113">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c6b72-113">When to use</span></span>

<span data-ttu-id="c6b72-114">Verwenden Sie Objekte, die aus der **comadmincatalogcollection** -Klasse erstellt wurden, wenn Sie eine Auflistung im com+-Katalog Programm gesteuert bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="c6b72-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="c6b72-115">Diese Sammlungen entsprechen Ordnern im Verwaltungs Tool Komponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="c6b72-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="c6b72-116">Elemente in den Ordnern entsprechen Elementen in Auflistungen, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6b72-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="c6b72-117">Informationen zu den Sammlungen im Katalog und deren Eigenschaften finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="c6b72-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="c6b72-118">Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="c6b72-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b72-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6b72-119">Remarks</span></span>

<span data-ttu-id="c6b72-120">Ein **comadmincatalogcollection** -Objekt kann nicht direkt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6b72-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="c6b72-121">Um die Methoden dieses Objekts verwenden zu können, müssen Sie ein [**comadmincatalog**](comadmincatalog.md) -Objekt erstellen, einen Verweis auf [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)abrufen und dann [**icomadmincatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) verwenden, um einen Verweis auf eine [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle abzurufen, die eine Auflistung der obersten Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6b72-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="c6b72-122">Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c6b72-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="c6b72-123">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6b72-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="c6b72-124">Ein comadmincatalogcollection-Objekt kann durch Aufrufen von [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für ein [**comadmincatalog**](comadmincatalog.md) -Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6b72-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="c6b72-125">Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c6b72-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="c6b72-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6b72-126">Requirements</span></span>



| <span data-ttu-id="c6b72-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6b72-127">Requirement</span></span> | <span data-ttu-id="c6b72-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c6b72-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b72-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6b72-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b72-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6b72-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6b72-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6b72-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b72-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6b72-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6b72-133">Header</span><span class="sxs-lookup"><span data-stu-id="c6b72-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b72-134"><dt>"COMAdmin. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c6b72-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6b72-135">IDL</span><span class="sxs-lookup"><span data-stu-id="c6b72-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6b72-136"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6b72-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b72-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6b72-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b72-138">**Comadmincatalog**</span><span class="sxs-lookup"><span data-stu-id="c6b72-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="c6b72-139">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="c6b72-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="c6b72-140">**Icatalogcollection**</span><span class="sxs-lookup"><span data-stu-id="c6b72-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




