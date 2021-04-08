---
description: Unterstützen mehrerer Rückrufe
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Unterstützen mehrerer Rückrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755264"
---
# <a name="supporting-multiple-callbacks"></a>Unterstützen mehrerer Rückrufe

Wenn Sie mehr als eine asynchrone Methode aufrufen, erfordert jedes eine separate Implementierung von [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Möglicherweise möchten Sie jedoch die Rückrufe innerhalb einer einzelnen C++-Klasse implementieren. Die Klasse kann nur eine Methode zum **aufrufen** haben. Daher besteht eine Lösung darin, eine Hilfsklasse bereitzustellen, die **Aufruf** Aufrufe an eine andere Methode in einer Container Klasse delegiert.

Der folgende Code zeigt eine Klassen Vorlage mit dem Namen `AsyncCallback` , die diese Vorgehensweise veranschaulicht.


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



Der Vorlagen Parameter ist der Name der Container Klasse. Der `AsyncCallback` Konstruktor verfügt über zwei Parameter: einen Zeiger auf die Container Klasse und die Adresse einer Rückruf Methode für die Container Klasse. Die Container Klasse kann mehrere Instanzen der `AsyncCallback` Klasse als Element Variablen aufweisen, eine für jede asynchrone Methode. Wenn die Container Klasse eine asynchrone Methode aufruft, wird die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des entsprechenden `AsyncCallback` Objekts verwendet. Wenn die `AsyncCallback` Aufruf Methode [](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) des Objekts aufgerufen wird, wird der Aufruf an die richtige Methode für die Container Klasse delegiert.

Das `AsyncCallback` -Objekt delegiert auch **adressf** -und **releaseaufrufe** an die Container-Klasse, sodass die Container Klasse die Lebensdauer des- `AsyncCallback` Objekts verwaltet. Dadurch wird sichergestellt, dass das `AsyncCallback` Objekt nicht gelöscht wird, bis das Container Objekt selbst gelöscht wird.

Der folgende Code zeigt, wie diese Vorlage verwendet wird:


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



In diesem Beispiel heißt die Container Klasse `CMyObject` . Die *m \_ CB* -Element Variable ist ein- `AsyncCallback` Objekt. Im `CMyObject` Konstruktor wird die *m \_ CB* -Member-Variable mit der Adresse der-Methode initialisiert `CMyObject::OnInvoke` .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Rückruf Methoden](asynchronous-callback-methods.md)
</dt> </dl>

 

 



