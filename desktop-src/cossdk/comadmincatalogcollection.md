---
description: Stellt eine beliebige Auflistung im COM+-Katalog dar. Verwenden Sie es, um Elemente in einer Auflistung aufzuzählen, hinzuzufügen, zu entfernen und abzurufen und auf verwandte Sammlungen zuzugreifen.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: COMAdminCatalogCollection-Klasse (ComAdmin.h)
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
ms.openlocfilehash: 3656e65b89ae02b0cfe8ea3b1dbe9784d679c5eb40e11edbfe2951e08893e1aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029480"
---
# <a name="comadmincatalogcollection-class"></a>COMAdminCatalogCollection-Klasse

Stellt eine beliebige Auflistung im COM+-Katalog dar. Verwenden Sie es, um Elemente in einer Auflistung aufzuzählen, hinzuzufügen, zu entfernen und abzurufen und auf verwandte Sammlungen zuzugreifen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------|
| Schnittstellen | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie Objekte, die aus der **COMAdminCatalogCollection-Klasse** erstellt wurden, wenn Sie eine Sammlung programmgesteuert im COM+-Katalog bearbeiten möchten. Diese Sammlungen entsprechen Ordnern im Verwaltungstool Komponentendienste. Elemente in den Ordnern entsprechen Elementen in Sammlungen, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogObject-Klasse**](comadmincatalogobject.md) erstellt wurden.

Informationen zu den Sammlungen im Katalog und deren Eigenschaften finden Sie unter [COM+ Administration Collections](com--administration-collections.md).

Eine Einführung in die programmgesteuerte Verwaltung von COM+ finden Sie unter [Automatisieren der COM+-Verwaltung.](automating-com--administration.md)

## <a name="remarks"></a>Hinweise

Sie können kein **COMAdminCatalogCollection-Objekt** direkt erstellen. Um die Methoden dieses Objekts zu verwenden, müssen Sie ein [**COMAdminCatalog-Objekt**](comadmincatalog.md) erstellen, einen Verweis auf [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)abrufen und dann [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) verwenden, um einen Verweis auf eine [**ICatalogCollection-Schnittstelle**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) abzurufen, die eine Auflistung der obersten Ebene darstellt. Dies wird im folgenden Beispiel gezeigt, in dem "TopCollection" durch den Namen einer der COM+-Verwaltungssammlungen der obersten Ebene ersetzt werden muss.


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



Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Administratortypbibliothek hinzu. Ein COMAdminCatalogCollection-Objekt kann erstellt werden, indem [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für ein [**COMAdminCatalog-Objekt**](comadmincatalog.md) aufgerufen wird. Dies wird im folgenden Beispiel gezeigt, in dem "TopCollection" durch den Namen einer der COM+-Verwaltungssammlungen der obersten Ebene ersetzt werden muss.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




