---
description: Die cbasepropertypage-Klasse ist eine abstrakte Klasse zum Implementieren einer Eigenschaften Seite. Verwenden Sie diese Klasse, wenn Sie einen Filter (oder ein anderes Objekt) schreiben, der Eigenschaften Seiten unterstützt.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Cbasepropertypage-Klasse (cprop. h)
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
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365685"
---
# <a name="cbasepropertypage-class"></a>Cbasepropertypage-Klasse

![cbasepropertypage-Klassenhierarchie](images/cprop01.png)

Die- `CBasePropertyPage` Klasse ist eine abstrakte Klasse zum Implementieren einer Eigenschaften Seite. Verwenden Sie diese Klasse, wenn Sie einen Filter (oder ein anderes Objekt) schreiben, der Eigenschaften Seiten unterstützt.



| Geschützte Member-Variablen                                             | BESCHREIBUNG                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bdirty**](cbasepropertypage-m-bdirty.md)                        | Gibt an, ob eine der Eigenschaften geändert wurde.                                                                             |
| [**m- \_ dialogID**](cbasepropertypage-m-dialogid.md)                    | Ressourcen Bezeichner für den Dialog.                                                                                               |
| [**m \_ Dlg**](cbasepropertypage-m-dlg.md)                              | Handle für das Dialogfeld Fenster.                                                                                                      |
| [**m- \_ HWND**](cbasepropertypage-m-hwnd.md)                            | Handle für das Dialogfeld Fenster.                                                                                                      |
| [**m \_ ppagesite**](cbasepropertypage-m-ppagesite.md)                  | Zeiger auf die **ipropertypagesite** -Schnittstelle der Eigenschaften Seiten Website.                                                         |
| [**m \_ TitleId**](cbasepropertypage-m-titleid.md)                      | Ressourcen Bezeichner für eine Zeichenfolge, die den Dialog Titel enthält.                                                                  |
| Öffentliche Methoden                                                         | BESCHREIBUNG                                                                                                                       |
| [**Cbasepropertypage**](cbasepropertypage-cbasepropertypage.md)       | Konstruktormethode.                                                                                                               |
| [**~ Cbasepropertypage**](cbasepropertypage--cbasepropertypage.md)     | Dekonstruktormethode. Virtu.                                                                                                       |
| [**Onaktivierung**](cbasepropertypage-onactivate.md)                     | Wird aufgerufen, wenn die Eigenschaften Seite aktiviert wird. Virtu.                                                                              |
| [**Onapplychanges**](cbasepropertypage-onapplychanges.md)             | Wird aufgerufen, wenn der Benutzer Änderungen auf der Eigenschaften Seite anwendet. Virtu.                                                               |
| [**OnConnect**](cbasepropertypage-onconnect.md)                       | Stellt einen **IUnknown** -Zeiger auf das-Objekt bereit, das der Eigenschaften Seite zugeordnet ist. Virtu.                                        |
| [**Ondeaktivieren**](cbasepropertypage-ondeactivate.md)                 | Wird aufgerufen, wenn das Dialogfeld Fenster zerstört wird. Virtu.                                                                          |
| [**OnDisconnect**](cbasepropertypage-ondisconnect.md)                 | Wird aufgerufen, wenn die Eigenschaften Seite das zugeordnete-Objekt freigeben soll. Virtu.                                                      |
| [**Onreceivemess**](cbasepropertypage-onreceivemessage.md)         | Wird aufgerufen, wenn das Dialogfeld eine Meldung empfängt. Virtu.                                                                           |
| IPropertyPage-Methoden                                                  | BESCHREIBUNG                                                                                                                       |
| [**Aktivieren**](cbasepropertypage-activate.md)                         | Erstellt das Fenster des Dialog Felds.                                                                                                    |
| [**Anwenden**](cbasepropertypage-apply.md)                               | Wendet die aktuellen Eigenschaften Seiten Werte auf das-Objekt an, das der Eigenschaften Seite zugeordnet ist.                                          |
| [**Deaktivieren**](cbasepropertypage-deactivate.md)                     | Zerstört das Dialogfenster.                                                                                                       |
| [**Getpageingefo**](cbasepropertypage-getpageinfo.md)                   | Ruft Informationen zur Eigenschaften Seite ab.                                                                                    |
| [**Hilfe**](cbasepropertypage-help.md)                                 | Ruft die Hilfe der Eigenschaften Seite auf.                                                                                                   |
| [**Ispagedirty**](cbasepropertypage-ispagedirty.md)                   | Gibt an, ob die Eigenschaften Seite seit der Aktivierung oder seit dem letzten Aufrufen von **IPropertyPage:: apply** geändert wurde. |
| [**Move**](cbasepropertypage-move.md)                                 | Positioniert und ändert die Größe des Dialog Felds.                                                                                             |
| [**"Eintobjects"**](cbasepropertypage-setobjects.md)                     | Stellt **IUnknown** -Zeiger für die Objekte bereit, die der Eigenschaften Seite zugeordnet sind.                                                 |
| [**Setpagesite**](cbasepropertypage-setpagesite.md)                   | Initialisiert die Eigenschaften Seite.                                                                                                    |
| [**Auftritt**](cbasepropertypage-show.md)                                 | Zeigt das Dialogfeld an oder blendet es aus.                                                                                                    |
| [**TranslateAccelerator**](cbasepropertypage-translateaccelerator.md) | Weist die Eigenschaften Seite an, eine Tastatureingabe zu verarbeiten.                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Eine Eigenschaften Seite ist ein COM-Objekt, daher müssen Sie eine GUID für den Klassen Bezeichner (CLSID) generieren und einen Eintrag im [**cfactorytemplate**](cfactorytemplate.md) -Array bereitstellen. Weitere Informationen finden Sie unter [DirectShow und com](directshow-and-com.md). Das folgende Beispiel zeigt einen typischen klassenfactoryeintrag:


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



Der Filter muss die **ISpecifyPropertyPages** -Schnittstelle verfügbar machen. Diese Schnittstelle enthält eine einzelne Methode, **GetPages**, die die CLSID der Eigenschaften Seite zurückgibt. Im folgenden Beispiel wird gezeigt, wie diese Methode implementiert wird:


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



Denken Sie daran, die **nondelegatingqueryinterface** -Methode des Filters ebenfalls zu überschreiben. Weitere Informationen finden Sie unter [DirectShow und com](directshow-and-com.md) und [**inondelegatingunknown**](inondelegatingunknown.md).

Erstellen Sie als nächstes das Dialogfeld als Ressource in Ihrem Projekt, und erstellen Sie eine Zeichen folgen Ressource, die den Dialog Titel enthält. Beide Ressourcen-IDs sind Parameter des **cbasepropertypage** -Konstruktors. Wenn Sie die Titel Zeichenfolge in einer Ressource aufbewahren, ist es einfacher, die Eigenschaften Seite zu lokalisieren.

Die **cbasepropertypage** -Klasse stellt ein Framework für die **IPropertyPage** -Schnittstelle bereit. Dieses Framework ruft eine Reihe von virtuellen Methoden auf, einschließlich [**cbasepropertypage:: onaktivierung**](cbasepropertypage-onactivate.md), [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md)usw. In der Basisklasse geben diese Methoden einfach S \_ OK zurück. Ihre abgeleitete Klasse muss einige oder alle dieser virtuellen Methoden überschreiben. Weitere Informationen finden Sie in den Hinweisen für die einzelnen Methoden.

Ein erweitertes Beispiel für die Verwendung dieser Klasse zum Erstellen einer Eigenschaften Seite finden Sie unter [Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




