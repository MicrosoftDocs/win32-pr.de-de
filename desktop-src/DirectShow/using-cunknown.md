---
description: DirectShow implementiert IUnknown in einer Basisklasse namens CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Verwenden von CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211ebf8c581502665c5f07b3720759efc7afab75a05a49a68f9945029dd6cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051380"
---
# <a name="using-cunknown"></a>Verwenden von CUnknown

DirectShow implementiert [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in einer Basisklasse namens [**CUnknown.**](cunknown.md) Sie können **CUnknown verwenden,** um andere Klassen ableiten und dabei nur die Methoden außer Kraft zu setzen, die sich komponentenübergreifend ändern. Die meisten anderen Basisklassen in DirectShow sind von **CUnknown** ableiten, sodass Ihre Komponente direkt von **CUnknown** oder von einer anderen Basisklasse erben kann.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) implementiert [**INonDelegatingUnknown.**](inondelegatingunknown.md) Die Verweisanzahl wird intern verwaltet, und in den meisten Situationen kann Ihre abgeleitete Klasse die beiden Verweiszählungsmethoden ohne Änderung erben. Beachten Sie, **dass CUnknown sich** selbst löscht, wenn der Verweiszähler auf 0 (null) fällt. Andererseits müssen Sie [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md)überschreiben, da die Methode in der Basisklasse E NOINTERFACE zurückgibt, wenn sie eine andere IID als \_ IID \_ IUnknown empfängt. Testen Sie in der abgeleiteten Klasse auf die IIDs von Schnittstellen, die Sie unterstützen, wie im folgenden Beispiel gezeigt:


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



Die Hilfsfunktion [**GetInterface**](getinterface.md) (siehe [**COM-Hilfsfunktionen**](com-helper-functions.md)) legt den Zeiger fest, erhöht die Verweisanzahl threadsicher und gibt S OK \_ zurück. Rufen Sie im Standardfall die Basisklassenmethode auf, und geben Sie das Ergebnis zurück. Wenn Sie von einer anderen Basisklasse ableiten, rufen Sie stattdessen deren [**NonDelegatingQueryInterface-Methode**](cunknown-nondelegatingqueryinterface.md) auf. Dadurch können Sie alle Schnittstellen unterstützen, die von der übergeordneten Klasse unterstützt werden.

## <a name="iunknown"></a>IUnknown

Wie bereits erwähnt, ist die delegierende Version von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für jede Komponente identisch, da sie nur die richtige Instanz der nicht delegierenden Version aufruft. Der Einfachheit halber enthält die Headerdatei Combase.h das Makro [**DECLARE \_ IUNKNOWN,**](declare-iunknown.md)das die drei delegierenden Methoden als Inlinemethoden deklariert. Er wird auf den folgenden Code erweitert:


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



Die Hilfsfunktion [**CUnknown::GetOwner**](cunknown-getowner.md) ruft einen Zeiger auf die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) der Komponente ab, die diese Komponente besitzt. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls besitzt sich die Komponente selbst. Schließen Sie das DECLARE \_ IUNKNOWN-Makro in den öffentlichen Abschnitt Ihrer Klassendefinition ein.

## <a name="class-constructor"></a>Klassenkonstruktor

Ihr Klassenkonstruktor sollte die Konstruktormethode für die übergeordnete Klasse aufrufen, zusätzlich zu allem, was für Ihre Klasse spezifisch ist. Das folgende Beispiel ist eine typische Konstruktormethode:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



Die -Methode verwendet die folgenden Parameter, die sie direkt an die [**CUnknown-Konstruktormethode**](cunknown.md) übergibt.

-   *tszName* gibt einen Namen für die Komponente an.
-   *pUnk* ist ein Zeiger auf die aggregierende [**IUnknown-**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   *pHr* ist ein Zeiger auf einen HRESULT-Wert, der den Erfolg oder Fehler der Methode angibt.

## <a name="summary"></a>Zusammenfassung

Das folgende Beispiel zeigt eine abgeleitete Klasse, die [**IUnknown unterstützt,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und eine hypothetische Schnittstelle namens ISomeInterface:


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

-   Die [**CUnknown-Klasse**](cunknown.md) implementiert die [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Die neue Komponente erbt **von CUnknown** und von allen Schnittstellen, die die Komponente unterstützt. Die Komponente könnte stattdessen von einer anderen Basisklasse ableiten, die von **CUnknown erbt.**
-   Das [**DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) deklariert die delegierenden [**IUnknown-Methoden**](/windows/win32/api/unknwn/nn-unknwn-iunknown) als Inlinemethoden.
-   Die [**CUnknown-Klasse**](cunknown.md) stellt die Implementierung für [**INonDelegatingUnknown zur Anwendung.**](inondelegatingunknown.md)
-   Um eine andere Schnittstelle als [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)zu unterstützen, muss die abgeleitete Klasse die [**NonDelegatingQueryInterface-Methode**](cunknown-nondelegatingqueryinterface.md) überschreiben und auf die IID der neuen Schnittstelle testen.
-   Der Klassenkonstruktor ruft die Konstruktormethode für [**CUnknown auf.**](cunknown.md)

Der nächste Schritt beim Schreiben eines Filters besteht im Aktivieren einer Anwendung zum Erstellen neuer Instanzen der Komponente. Dies erfordert ein Verständnis von DLLs und ihrer Beziehung zu Klassen factorys und Klassenkonstruktormethoden. Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL.](how-to-create-a-dll.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
