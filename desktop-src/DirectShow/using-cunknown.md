---
description: DirectShow implementiert IUnknown in einer Basisklasse mit dem Namen cunknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Verwenden von cunknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348710"
---
# <a name="using-cunknown"></a>Verwenden von cunknown

DirectShow implementiert [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in einer Basisklasse mit dem Namen [**cunknown**](cunknown.md). Sie können mit **cunknown** andere Klassen ableiten und nur die Methoden überschreiben, die sich Komponenten übergreifend ändern. Die meisten anderen Basisklassen in DirectShow werden von **cunknown** abgeleitet, sodass Ihre Komponente direkt von **cunknown** oder einer anderen Basisklasse erben kann.

## <a name="inondelegatingunknown"></a>Inondelegatingunknown

[**Cunknown**](cunknown.md) implementiert [**inondelegatingunknown**](inondelegatingunknown.md). Sie verwaltet Verweis Zähler intern, und in den meisten Fällen kann die abgeleitete Klasse die beiden Verweis Zählmethoden ohne Änderung erben. Beachten Sie, dass **cunknown** sich selbst löscht, wenn der Verweis Zähler auf 0 (null) sinkt. Andererseits müssen Sie [**cunknown:: nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md)überschreiben, da die-Methode in der Basisklasse E nointerface zurückgibt, \_ Wenn Sie eine andere IID als IID \_ IUnknown empfängt. Testen Sie in der abgeleiteten Klasse die IIDs der Schnittstellen, die Sie unterstützen, wie im folgenden Beispiel gezeigt:


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



Die Hilfsprogrammfunktion [**GetInterface**](getinterface.md) (siehe [**com**](com-helper-functions.md)-Hilfselemente) legt den-Zeiger fest, erhöht den Verweis Zähler auf Thread sichere Weise und gibt S \_ OK zurück. Im Standardfall wird die Basisklassen Methode aufgerufen und das Ergebnis zurückgegeben. Wenn Sie von einer anderen Basisklasse ableiten, müssen Sie stattdessen die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode aufzurufen. Dadurch können Sie alle Schnittstellen unterstützen, die von der übergeordneten Klasse unterstützt werden.

## <a name="iunknown"></a>IUnknown

Wie bereits erwähnt, ist die delegier Ende Version von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für jede Komponente identisch, da Sie nichts anderes bewirkt, als die richtige Instanz der nicht delegierenden Version aufzurufen. Aus Gründen der Bequemlichkeit enthält die Header Datei "ComBase. h" ein Makro, [**deklarieren Sie " \_ IUnknown**](declare-iunknown.md)", das die drei delegierenden Methoden als Inline Methoden deklariert. Es wird auf den folgenden Code erweitert:


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



Die Utility-Funktion [**cunknown:: GetOwner**](cunknown-getowner.md) Ruft einen Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle der Komponente ab, die diese Komponente besitzt. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls ist die Komponente eigenständig. Fügen Sie das \_ Makro DECLARE IUnknown in den Abschnitt Public der Klassendefinition ein.

## <a name="class-constructor"></a>Klassenkonstruktor

Der Klassenkonstruktor sollte zusätzlich zu allem, was für Ihre Klasse spezifisch ist, die Konstruktormethode für die übergeordnete Klasse aufrufen. Das folgende Beispiel ist eine typische Konstruktormethode:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



Die-Methode übernimmt die folgenden Parameter, die Sie direkt an die [**cunknown**](cunknown.md) -Konstruktormethode übergibt.

-   *zzname* gibt einen Namen für die Komponente an.
-   der *Punk* ist ein Zeiger auf die Aggregations- [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   *PHR* ist ein Zeiger auf einen HRESULT-Wert, der angibt, dass die Methode erfolgreich war oder fehlgeschlagen ist.

## <a name="summary"></a>Zusammenfassung

Das folgende Beispiel zeigt eine abgeleitete Klasse, die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und eine hypothetische Schnittstelle mit dem Namen "isominput Face" unterstützt:


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



In diesem Beispiel werden die folgenden Punkte veranschaulicht:

-   Die [**cunknown**](cunknown.md) -Klasse implementiert die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. Die neue Komponente erbt von **cunknown** und von allen Schnittstellen, die von der Komponente unterstützt werden. Die Komponente kann stattdessen von einer anderen Basisklasse abgeleitet werden, die von **cunknown** erbt.
-   Das-Makro [**Declare \_ IUnknown**](declare-iunknown.md) deklariert die delegierenden [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methoden als Inline Methoden.
-   Die [**cunknown**](cunknown.md) -Klasse stellt die Implementierung für [**inondelegatingunknown**](inondelegatingunknown.md)bereit.
-   Zur Unterstützung einer anderen Schnittstelle als [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)muss die abgeleitete Klasse die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode überschreiben und die IID der neuen Schnittstelle testen.
-   Der Klassenkonstruktor Ruft die Konstruktormethode für [**cunknown**](cunknown.md)auf.

Der nächste Schritt beim Schreiben eines Filters besteht darin, eine Anwendung zum Erstellen neuer Instanzen der Komponente zu aktivieren. Dies erfordert ein Verständnis der DLLs und deren Beziehung zu Klassenfactorys und Klassenkonstruktormethoden. Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
