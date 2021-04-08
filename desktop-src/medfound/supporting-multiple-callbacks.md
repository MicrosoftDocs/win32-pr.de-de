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
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="58b7e-103">Unterstützen mehrerer Rückrufe</span><span class="sxs-lookup"><span data-stu-id="58b7e-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="58b7e-104">Wenn Sie mehr als eine asynchrone Methode aufrufen, erfordert jedes eine separate Implementierung von [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="58b7e-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="58b7e-105">Möglicherweise möchten Sie jedoch die Rückrufe innerhalb einer einzelnen C++-Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="58b7e-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="58b7e-106">Die Klasse kann nur eine Methode zum **aufrufen** haben. Daher besteht eine Lösung darin, eine Hilfsklasse bereitzustellen, die **Aufruf** Aufrufe an eine andere Methode in einer Container Klasse delegiert.</span><span class="sxs-lookup"><span data-stu-id="58b7e-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="58b7e-107">Der folgende Code zeigt eine Klassen Vorlage mit dem Namen `AsyncCallback` , die diese Vorgehensweise veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="58b7e-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


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



<span data-ttu-id="58b7e-108">Der Vorlagen Parameter ist der Name der Container Klasse.</span><span class="sxs-lookup"><span data-stu-id="58b7e-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="58b7e-109">Der `AsyncCallback` Konstruktor verfügt über zwei Parameter: einen Zeiger auf die Container Klasse und die Adresse einer Rückruf Methode für die Container Klasse.</span><span class="sxs-lookup"><span data-stu-id="58b7e-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="58b7e-110">Die Container Klasse kann mehrere Instanzen der `AsyncCallback` Klasse als Element Variablen aufweisen, eine für jede asynchrone Methode.</span><span class="sxs-lookup"><span data-stu-id="58b7e-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="58b7e-111">Wenn die Container Klasse eine asynchrone Methode aufruft, wird die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des entsprechenden `AsyncCallback` Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="58b7e-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="58b7e-112">Wenn die `AsyncCallback` Aufruf Methode [](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) des Objekts aufgerufen wird, wird der Aufruf an die richtige Methode für die Container Klasse delegiert.</span><span class="sxs-lookup"><span data-stu-id="58b7e-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="58b7e-113">Das `AsyncCallback` -Objekt delegiert auch **adressf** -und **releaseaufrufe** an die Container-Klasse, sodass die Container Klasse die Lebensdauer des- `AsyncCallback` Objekts verwaltet.</span><span class="sxs-lookup"><span data-stu-id="58b7e-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="58b7e-114">Dadurch wird sichergestellt, dass das `AsyncCallback` Objekt nicht gelöscht wird, bis das Container Objekt selbst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="58b7e-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="58b7e-115">Der folgende Code zeigt, wie diese Vorlage verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="58b7e-115">The following code shows how to use this template:</span></span>


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



<span data-ttu-id="58b7e-116">In diesem Beispiel heißt die Container Klasse `CMyObject` .</span><span class="sxs-lookup"><span data-stu-id="58b7e-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="58b7e-117">Die *m \_ CB* -Element Variable ist ein- `AsyncCallback` Objekt.</span><span class="sxs-lookup"><span data-stu-id="58b7e-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="58b7e-118">Im `CMyObject` Konstruktor wird die *m \_ CB* -Member-Variable mit der Adresse der-Methode initialisiert `CMyObject::OnInvoke` .</span><span class="sxs-lookup"><span data-stu-id="58b7e-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58b7e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58b7e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58b7e-120">Asynchrone Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="58b7e-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



