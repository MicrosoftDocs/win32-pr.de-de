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
# <a name="comadmincatalogobject-class"></a>COMAdminCatalogObject-Klasse

Stellt Elemente in Auflistungen im com+-Katalog dar. Verwenden Sie es zum Abrufen und Ändern von Eigenschaften, die von einem Element in einer Sammlung verfügbar gemacht werden.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|------------------------------------------|
| Schnittstellen | [**Icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie Objekte, die aus der **COMAdminCatalogObject** -Klasse erstellt wurden, um die Eigenschaften von Elementen in Auflistungen im com+-Katalog zu ändern. Diese Elemente entsprechen den Elementen, die in den Ordnern in der Konsolen Struktur des Verwaltungs Tools für Komponenten Dienste angezeigt werden. Ordner im Verwaltungs Tool Komponenten Dienste entsprechen Sammlungen im-Katalog, die Sie mithilfe von Objekten darstellen können, die aus der [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse erstellt wurden.

Nicht alle Auflistungen und Elemente, die über " [**comadmincatalogcollection**](comadmincatalogcollection.md) " und " **COMAdminCatalogObject** " verfügbar gemacht werden, sind im Verwaltungs Tool für Komponenten Dienste verfügbar.

Informationen zu bestimmten Sammlungen und deren Eigenschaften finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).

Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).

## <a name="remarks"></a>Bemerkungen

Ein **COMAdminCatalogObject** -Objekt kann nicht direkt erstellt werden. Um die Methoden dieses Objekts verwenden zu können, müssen Sie ein [**comadmincatalog**](comadmincatalog.md) -Objekt erstellen, einen Verweis auf [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)abrufen und dann [**icomadmincatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) verwenden, um einen Verweis auf eine [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle zu erhalten, die eine Auflistung der obersten Ebene darstellt, oder [**icatalogcollection:**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)

Nachdem Sie einen Verweis auf die [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle der Sammlung haben, für die Sie sich interessieren, nennen Sie [**icatalogcollection::P opate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) , um die Auflistung mit allen Elementen aufzufüllen. Durchlaufen Sie alle Elemente in der Auflistung, indem Sie [**icatalogcollection:: get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) aufrufen, um einen Verweis auf jede [**icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) -Schnittstelle zu erhalten. Wenn Sie das gewünschte Element finden, können Sie die Eigenschaften des Elements ändern und die Iterationen beenden. Wenn Sie Änderungen an Elementen in einer Auflistung vornehmen, müssen Sie [**icatalogcollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) zum Speichern der Änderungen im com+-Katalog abrufen.

Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss. "ItemName" muss durch den Namen des Elements ersetzt werden, an dem Sie interessiert sind. "PropertyName" muss durch den Namen der Eigenschaft ersetzt werden, die Sie im Element ändern. und varnewprop müssen durch eine Variante ersetzt werden, die den neuen Wert für die Eigenschaft enthält.


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



Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu. Ein comadmincatalogcollection-Objekt kann erstellt werden, indem [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für ein [**comadmincatalog**](comadmincatalog.md) -oder [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aufgerufen wird.

Rufen Sie die [**Auffüllen**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts auf, um die Auflistung mit allen Elementen aufzufüllen. Iterieren Sie alle Elemente in der Auflistung. Wenn Sie das gewünschte Element finden, können Sie die Eigenschaften des Elements ändern und die Iterationen beenden. Wenn Sie Änderungen an Elementen in einer Auflistung vornehmen, müssen Sie die [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode des **comadmincatalogcollection** -Objekts anrufen, um die Änderungen im com+-Katalog zu speichern.

Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss. "ItemName" muss durch den Namen des Elements ersetzt werden, an dem Sie interessiert sind. "PropertyName" muss durch den Namen der Eigenschaft ersetzt werden, die Sie im Element ändern. und newpropvalue müssen durch den neuen Wert für die-Eigenschaft ersetzt werden.


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
| Header<br/>                   | <dl> <dt>"COMAdmin. h"</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Comadmincatalog**](comadmincatalog.md)
</dt> <dt>

[**Comadmincatalogcollection**](comadmincatalogcollection.md)
</dt> <dt>

[**Icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




