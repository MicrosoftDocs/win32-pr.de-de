---
description: Stellt Elemente in Auflistungen im com+-Katalog dar. Verwenden Sie es zum Abrufen und Ändern von Eigenschaften, die von einem Element in einer Sammlung verfügbar gemacht werden.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: COMAdminCatalogObject-Klasse (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126716"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="ce3ba-104">COMAdminCatalogObject-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce3ba-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="ce3ba-105">Stellt Elemente in Auflistungen im com+-Katalog dar.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="ce3ba-106">Verwenden Sie es zum Abrufen und Ändern von Eigenschaften, die von einem Element in einer Sammlung verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ce3ba-107">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="ce3ba-107">When to implement</span></span>

<span data-ttu-id="ce3ba-108">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="ce3ba-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce3ba-109">Requirement</span></span> | <span data-ttu-id="ce3ba-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ce3ba-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="ce3ba-111">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ce3ba-111">Interfaces</span></span> | [<span data-ttu-id="ce3ba-112">**Icatalogobject**</span><span class="sxs-lookup"><span data-stu-id="ce3ba-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="ce3ba-113">Verwendung</span><span class="sxs-lookup"><span data-stu-id="ce3ba-113">When to use</span></span>

<span data-ttu-id="ce3ba-114">Verwenden Sie Objekte, die aus der **COMAdminCatalogObject** -Klasse erstellt wurden, um die Eigenschaften von Elementen in Auflistungen im com+-Katalog zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="ce3ba-115">Diese Elemente entsprechen den Elementen, die in den Ordnern in der Konsolen Struktur des Verwaltungs Tools für Komponenten Dienste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="ce3ba-116">Ordner im Verwaltungs Tool Komponenten Dienste entsprechen Sammlungen im-Katalog, die Sie mithilfe von Objekten darstellen können, die aus der [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="ce3ba-117">Nicht alle Auflistungen und Elemente, die über " [**comadmincatalogcollection**](comadmincatalogcollection.md) " und " **COMAdminCatalogObject** " verfügbar gemacht werden, sind im Verwaltungs Tool für Komponenten Dienste verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="ce3ba-118">Informationen zu bestimmten Sammlungen und deren Eigenschaften finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="ce3ba-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="ce3ba-119">Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="ce3ba-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce3ba-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce3ba-120">Remarks</span></span>

<span data-ttu-id="ce3ba-121">Ein **COMAdminCatalogObject** -Objekt kann nicht direkt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="ce3ba-122">Um die Methoden dieses Objekts verwenden zu können, müssen Sie ein [**comadmincatalog**](comadmincatalog.md) -Objekt erstellen, einen Verweis auf [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)abrufen und dann [**icomadmincatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) verwenden, um einen Verweis auf eine [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle zu erhalten, die eine Auflistung der obersten Ebene darstellt, oder [**icatalogcollection:**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)</span><span class="sxs-lookup"><span data-stu-id="ce3ba-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="ce3ba-123">Nachdem Sie einen Verweis auf die [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle der Sammlung haben, für die Sie sich interessieren, nennen Sie [**icatalogcollection::P opate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) , um die Auflistung mit allen Elementen aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="ce3ba-124">Durchlaufen Sie alle Elemente in der Auflistung, indem Sie [**icatalogcollection:: get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) aufrufen, um einen Verweis auf jede [**icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="ce3ba-125">Wenn Sie das gewünschte Element finden, können Sie die Eigenschaften des Elements ändern und die Iterationen beenden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="ce3ba-126">Wenn Sie Änderungen an Elementen in einer Auflistung vornehmen, müssen Sie [**icatalogcollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) zum Speichern der Änderungen im com+-Katalog abrufen.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="ce3ba-127">Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss. "ItemName" muss durch den Namen des Elements ersetzt werden, an dem Sie interessiert sind. "PropertyName" muss durch den Namen der Eigenschaft ersetzt werden, die Sie im Element ändern. und varnewprop müssen durch eine Variante ersetzt werden, die den neuen Wert für die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



<span data-ttu-id="ce3ba-128">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="ce3ba-129">Ein comadmincatalogcollection-Objekt kann erstellt werden, indem [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für ein [**comadmincatalog**](comadmincatalog.md) -oder [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="ce3ba-130">Rufen Sie die [**Auffüllen**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts auf, um die Auflistung mit allen Elementen aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="ce3ba-131">Iterieren Sie alle Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="ce3ba-132">Wenn Sie das gewünschte Element finden, können Sie die Eigenschaften des Elements ändern und die Iterationen beenden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="ce3ba-133">Wenn Sie Änderungen an Elementen in einer Auflistung vornehmen, müssen Sie die [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode des **comadmincatalogcollection** -Objekts anrufen, um die Änderungen im com+-Katalog zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="ce3ba-134">Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss. "ItemName" muss durch den Namen des Elements ersetzt werden, an dem Sie interessiert sind. "PropertyName" muss durch den Namen der Eigenschaft ersetzt werden, die Sie im Element ändern. und newpropvalue müssen durch den neuen Wert für die-Eigenschaft ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ce3ba-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a><span data-ttu-id="ce3ba-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce3ba-135">Requirements</span></span>



| <span data-ttu-id="ce3ba-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce3ba-136">Requirement</span></span> | <span data-ttu-id="ce3ba-137">Wert</span><span class="sxs-lookup"><span data-stu-id="ce3ba-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3ba-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce3ba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3ba-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce3ba-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce3ba-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce3ba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3ba-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce3ba-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce3ba-142">Header</span><span class="sxs-lookup"><span data-stu-id="ce3ba-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce3ba-143"><dt>"COMAdmin. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ce3ba-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce3ba-144">IDL</span><span class="sxs-lookup"><span data-stu-id="ce3ba-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ce3ba-145"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ce3ba-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce3ba-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce3ba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3ba-147">**Comadmincatalog**</span><span class="sxs-lookup"><span data-stu-id="ce3ba-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="ce3ba-148">**Comadmincatalogcollection**</span><span class="sxs-lookup"><span data-stu-id="ce3ba-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="ce3ba-149">**Icatalogobject**</span><span class="sxs-lookup"><span data-stu-id="ce3ba-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




