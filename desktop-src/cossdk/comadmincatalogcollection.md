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
# <a name="comadmincatalogcollection-class"></a>Comadmincatalogcollection-Klasse

Stellt eine beliebige Auflistung im com+-Katalog dar. Verwenden Sie diese Option, um Elemente in einer Auflistung aufzulisten, hinzuzufügen, zu entfernen und abzurufen und um auf verwandte Auflistungen zuzugreifen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|--------------------------------------------------|
| Schnittstellen | [**Icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie Objekte, die aus der **comadmincatalogcollection** -Klasse erstellt wurden, wenn Sie eine Auflistung im com+-Katalog Programm gesteuert bearbeiten möchten. Diese Sammlungen entsprechen Ordnern im Verwaltungs Tool Komponenten Dienste. Elemente in den Ordnern entsprechen Elementen in Auflistungen, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse erstellt wurden.

Informationen zu den Sammlungen im Katalog und deren Eigenschaften finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).

Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).

## <a name="remarks"></a>Bemerkungen

Ein **comadmincatalogcollection** -Objekt kann nicht direkt erstellt werden. Um die Methoden dieses Objekts verwenden zu können, müssen Sie ein [**comadmincatalog**](comadmincatalog.md) -Objekt erstellen, einen Verweis auf [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)abrufen und dann [**icomadmincatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) verwenden, um einen Verweis auf eine [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle abzurufen, die eine Auflistung der obersten Ebene darstellt. Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss.


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



Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu. Ein comadmincatalogcollection-Objekt kann durch Aufrufen von [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für ein [**comadmincatalog**](comadmincatalog.md) -Objekt erstellt werden. Dies wird im folgenden Beispiel gezeigt, in dem "topcollection" durch den Namen einer der com+-Verwaltungs Sammlungen der obersten Ebene ersetzt werden muss.


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
| Header<br/>                   | <dl> <dt>"COMAdmin. h"</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Comadmincatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**Icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




