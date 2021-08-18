---
description: Stellt Elemente in Auflistungen im COM+-Katalog dar. Verwenden Sie es, um Eigenschaften abzurufen und zu ändern, die von einem Element in einer Auflistung verfügbar gemacht werden.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: COMAdminCatalogObject-Klasse (ComAdmin.h)
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
ms.openlocfilehash: bce57021774b3abc2f69a1120862912452629c3e70d9c8fd0ebcc5d39ce5203d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548587"
---
# <a name="comadmincatalogobject-class"></a>COMAdminCatalogObject-Klasse

Stellt Elemente in Auflistungen im COM+-Katalog dar. Verwenden Sie es, um Eigenschaften abzurufen und zu ändern, die von einem Element in einer Auflistung verfügbar gemacht werden.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|------------------------------------------|
| Schnittstellen | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie Objekte, die aus der **COMAdminCatalogObject-Klasse** erstellt wurden, um die Eigenschaften von Elementen zu ändern, die in Sammlungen im COM+-Katalog enthalten sind. Diese Elemente entsprechen Elementen, die in Ordnern in der Konsolenstruktur des Component Services-Verwaltungstools angezeigt werden. Ordner im Component Services-Verwaltungstool entsprechen Sammlungen im Katalog, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogCollection-Klasse**](comadmincatalogcollection.md) erstellt wurden.

Nicht alle Sammlungen und Elemente, die über [**COMAdminCatalogCollection**](comadmincatalogcollection.md) und **COMAdminCatalogObject** verfügbar gemacht werden, sind im Component Services-Verwaltungstool verfügbar.

Informationen zu bestimmten Sammlungen und deren Eigenschaften finden Sie unter [COM+-Verwaltungssammlungen.](com--administration-collections.md)

Eine Einführung in die programmgesteuerte Verwaltung von COM+ finden Sie unter [Automatisieren der COM+-Verwaltung.](automating-com--administration.md)

## <a name="remarks"></a>Hinweise

Sie können kein **COMAdminCatalogObject-Objekt** direkt erstellen. Um die Methoden dieses Objekts zu verwenden, müssen Sie ein [**COMAdminCatalog-Objekt**](comadmincatalog.md) erstellen, einen Verweis auf [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)abrufen und dann [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) verwenden, um einen Verweis auf eine [**ICatalogCollection-Schnittstelle**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) abzurufen, die eine Auflistung der obersten Ebene darstellt, oder [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) verwenden, um auf Sammlungen zuzugreifen, die nicht der obersten Ebene entsprechen.

Nachdem Sie über einen Verweis auf die [**ICatalogCollection-Schnittstelle**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) der Sammlung verfügen, an der Sie interessiert sind, rufen Sie [**ICatalogCollection::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) auf, um die Sammlung mit allen ihren Elementen aufzufüllen. Durchlaufen Sie jedes der Elemente in der Auflistung, indem [**Sie ICatalogCollection::get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) aufrufen, um einen Verweis auf jede [**ICatalogObject-Schnittstelle**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) abzurufen. Wenn Sie das gewünschte Element finden, können Sie die Eigenschaften des Elements ändern und die Iteration beenden. Wenn Sie Änderungen an Elementen in einer Sammlung vornehmen, müssen Sie [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) aufrufen, um die Änderungen im COM+-Katalog zu speichern.

Dies wird im folgenden Beispiel gezeigt, in dem "TopCollection" durch den Namen einer der COM+-Verwaltungssammlungen der obersten Ebene ersetzt werden muss. "ItemName" muss durch den Namen des Elements ersetzt werden, an dem Sie interessiert sind. "PropertyName" muss durch den Namen der Eigenschaft ersetzt werden, die Sie im Element ändern. und varNewProp müssen durch einen VARIANT ersetzt werden, der den neuen Wert für die Eigenschaft enthält.


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



Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Administratortypbibliothek hinzu. Ein COMAdminCatalogCollection-Objekt kann erstellt werden, indem [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für ein [**COMAdminCatalog-**](comadmincatalog.md) oder [**COMAdminCatalogCollection-Objekt**](comadmincatalogcollection.md) aufgerufen wird.

Rufen Sie die [**Populate-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) des [**COMAdminCatalogCollection-Objekts**](comadmincatalogcollection.md) auf, um die Auflistung mit allen zugehörigen Elementen aufzufüllen. Durchlaufen Sie jedes der Elemente in der Auflistung. Wenn Sie das gewünschte Element finden, können Sie die Eigenschaften des Elements ändern und die Iteration beenden. Wenn Sie Änderungen an Elementen in einer Sammlung vornehmen, müssen Sie die [**SaveChanges-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) des **COMAdminCatalogCollection-Objekts** aufrufen, um die Änderungen im COM+-Katalog zu speichern.

Dies wird im folgenden Beispiel gezeigt, in dem "TopCollection" durch den Namen einer der COM+-Verwaltungssammlungen der obersten Ebene ersetzt werden muss. "ItemName" muss durch den Namen des Elements ersetzt werden, an dem Sie interessiert sind. "PropertyName" muss durch den Namen der Eigenschaft ersetzt werden, die Sie im Element ändern. und NewPropValue müssen durch den neuen Wert für die Eigenschaft ersetzt werden.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




