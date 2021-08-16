---
description: Die CBasePropertyPage-Klasse ist eine abstrakte Klasse zum Implementieren einer Eigenschaftenseite. Verwenden Sie diese Klasse, wenn Sie einen Filter (oder ein anderes Objekt) schreiben, der Eigenschaftenseiten unterstützt.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: CBasePropertyPage-Klasse (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ca4bf0789488a8601ae24bd4e43e1af8335fdf97a7864cbfba242b9c99eca8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955014"
---
# <a name="cbasepropertypage-class"></a>CBasePropertyPage-Klasse

![cbasepropertypage-Klassenhierarchie](images/cprop01.png)

Die `CBasePropertyPage` -Klasse ist eine abstrakte Klasse zum Implementieren einer Eigenschaftenseite. Verwenden Sie diese Klasse, wenn Sie einen Filter (oder ein anderes Objekt) schreiben, der Eigenschaftenseiten unterstützt.



| Geschützte Membervariablen                                             | Beschreibung                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bDirty**](cbasepropertypage-m-bdirty.md)                        | Gibt an, ob eine der Eigenschaften geändert wurde.                                                                             |
| [**m \_ DialogId**](cbasepropertypage-m-dialogid.md)                    | Ressourcenbezeichner für das Dialogfeld.                                                                                               |
| [**m \_ Dlg**](cbasepropertypage-m-dlg.md)                              | Handle für das Dialogfeld.                                                                                                      |
| [**m \_ hwnd**](cbasepropertypage-m-hwnd.md)                            | Handle für das Dialogfeld.                                                                                                      |
| [**m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)                  | Zeiger auf die **IPropertyPageSite-Schnittstelle** der Eigenschaftenseitenwebsite.                                                         |
| [**m \_ TitleId**](cbasepropertypage-m-titleid.md)                      | Ressourcenbezeichner für eine Zeichenfolge, die den Dialogtitel enthält.                                                                  |
| Öffentliche Methoden                                                         | Beschreibung                                                                                                                       |
| [**CBasePropertyPage**](cbasepropertypage-cbasepropertypage.md)       | Konstruktormethode.                                                                                                               |
| [**~CBasePropertyPage**](cbasepropertypage--cbasepropertypage.md)     | Destruktormethode. Virtuellen.                                                                                                       |
| [**Ondeactivate**](cbasepropertypage-onactivate.md)                     | Wird aufgerufen, wenn die Eigenschaftenseite aktiviert wird. Virtuellen.                                                                              |
| [**OnApplyChanges**](cbasepropertypage-onapplychanges.md)             | Wird aufgerufen, wenn der Benutzer Änderungen auf die Eigenschaftenseite wendet. Virtuellen.                                                               |
| [**OnConnect**](cbasepropertypage-onconnect.md)                       | Stellt einen **IUnknown-Zeiger** auf das Der Eigenschaftenseite zugeordnete -Objekt zur Seite. Virtuellen.                                        |
| [**OnDeactivate**](cbasepropertypage-ondeactivate.md)                 | Wird aufgerufen, wenn das Dialogfeldfenster zerstört wird. Virtuellen.                                                                          |
| [**OnDisconnect**](cbasepropertypage-ondisconnect.md)                 | Wird aufgerufen, wenn die Eigenschaftenseite das zugeordnete Objekt frei geben soll. Virtuellen.                                                      |
| [**OnReceiveMessage**](cbasepropertypage-onreceivemessage.md)         | Wird aufgerufen, wenn das Dialogfeld eine Nachricht empfängt. Virtuellen.                                                                           |
| IPropertyPage-Methoden                                                  | Beschreibung                                                                                                                       |
| [**Aktivieren**](cbasepropertypage-activate.md)                         | Erstellt das Dialogfeldfenster.                                                                                                    |
| [**Anwenden**](cbasepropertypage-apply.md)                               | Wendet die aktuellen Eigenschaftsseitenwerte auf das -Objekt an, das der Eigenschaftenseite zugeordnet ist.                                          |
| [**Deaktivieren**](cbasepropertypage-deactivate.md)                     | Zerstört das Dialogfeld.                                                                                                       |
| [**GetPageInfo**](cbasepropertypage-getpageinfo.md)                   | Ruft Informationen zur Eigenschaftenseite ab.                                                                                    |
| [**Hilfe**](cbasepropertypage-help.md)                                 | Ruft die Hilfe zur Eigenschaftenseite auf.                                                                                                   |
| [**IsPageDirty**](cbasepropertypage-ispagedirty.md)                   | Gibt an, ob sich die Eigenschaftenseite seit ihrer Aktivierung oder seit dem letzten Aufruf von **IPropertyPage::Apply geändert hat.** |
| [**Move**](cbasepropertypage-move.md)                                 | Positioniert das Dialogfeld und seine Größe.                                                                                             |
| [**SetObjects**](cbasepropertypage-setobjects.md)                     | Stellt **IUnknown-Zeiger** für die -Objekte dar, die der Eigenschaftenseite zugeordnet sind.                                                 |
| [**SetPageSite**](cbasepropertypage-setpagesite.md)                   | Initialisiert die Eigenschaftenseite.                                                                                                    |
| [**Zeigen**](cbasepropertypage-show.md)                                 | Zeigt das Dialogfeld an oder blendet es aus.                                                                                                    |
| [**Translateaccelerator**](cbasepropertypage-translateaccelerator.md) | Weist die Eigenschaftenseite an, eine Tastatureingabe zu verarbeiten.                                                                               |



 

## <a name="remarks"></a>Hinweise

Eine Eigenschaftenseite ist ein COM-Objekt, daher müssen Sie eine GUID für den Klassenbezeichner (CLSID) generieren und einen Eintrag im [**CFactoryTemplate-Array**](cfactorytemplate.md) bereitstellen. Weitere Informationen finden Sie unter [DirectShow und COM.](directshow-and-com.md) Das folgende Beispiel zeigt einen typischen Klassen factory-Eintrag:


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



Ihr Filter muss die **ISpecifyPropertyPages-Schnittstelle** verfügbar machen. Diese Schnittstelle enthält eine einzelne Methode, **GetPages,** die die CLSID der Eigenschaftenseite zurückgibt. Das folgende Beispiel zeigt, wie diese Methode implementiert wird:


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



Denken Sie daran, auch die **NonDelegatingQueryInterface-Methode** des Filters zu überschreiben. Weitere Informationen finden Sie unter [DirectShow und COM](directshow-and-com.md) und [**INonDelegatingUnknown**](inondelegatingunknown.md).

Erstellen Sie als Nächstes den Dialog als Ressource in Ihrem Projekt, und erstellen Sie eine Zeichenfolgenressource, die den Dialogtitel enthält. Beide Ressourcen-IDs sind Parameter für den **CBasePropertyPage-Konstruktor.** Wenn Sie die Titelzeichenfolge in einer Ressource behalten, ist es einfacher, Ihre Eigenschaftenseite zu lokalisieren.

Die **CBasePropertyPage-Klasse** stellt ein Framework für die **IPropertyPage-Schnittstelle** bereit. Dieses Framework ruft eine Reihe von virtuellen Methoden auf, einschließlich [**CBasePropertyPage::OnActivate,**](cbasepropertypage-onactivate.md) [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md)und so weiter. In der Basisklasse geben diese Methoden einfach S \_ OK zurück. Ihre abgeleitete Klasse muss einige oder alle dieser virtuellen Methoden überschreiben. Weitere Informationen finden Sie in den Anmerkungen zu den einzelnen Methoden.

Ein erweitertes Beispiel für die Verwendung dieser Klasse zum Erstellen einer Eigenschaftenseite finden Sie unter [Erstellen einer Filtereigenschaftsseite.](creating-a-filter-property-page.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




