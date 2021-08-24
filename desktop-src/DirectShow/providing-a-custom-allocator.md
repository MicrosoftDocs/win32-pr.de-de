---
description: Bereitstellen einer benutzerdefinierten Zuweisung
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Bereitstellen einer benutzerdefinierten Zuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b2f36f269ff30545d648c5df22e3070ec5588bcc2fa8791852fe9b6a59215c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747910"
---
# <a name="providing-a-custom-allocator"></a>Bereitstellen einer benutzerdefinierten Zuweisung

In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Zuweisung für einen Filter bereitstellen. Es [**werden nur IMemInputPin-Verbindungen**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) beschrieben, die Schritte für eine [**IAsyncReader-Verbindung**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sind jedoch ähnlich.

Definieren Sie zunächst eine C++-Klasse für die Zuweisung. Ihre Zuweisung kann von einer der Standardzuweisungsklassen [**,CBaseAllocator**](cbaseallocator.md) oder [**CMemAllocator'**](cmemallocator.md)ableiten, oder Sie können eine völlig neue Zuweisungsklasse erstellen. Wenn Sie eine neue Klasse erstellen, muss sie die [**IMemAllocator-Schnittstelle verfügbar**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) machen.

Die verbleibenden Schritte hängen davon ab, ob Ihre Zuweisung zu einem Eingabepin oder einem Ausgabepin in Ihrem Filter gehört. Eingabepins spielen während der Zuweisungsaushandlungsphase eine andere Rolle als Ausgabepins, da der Ausgabepin letztendlich die Zuweisung auswählt.

**Bereitstellen einer benutzerdefinierten Zuweisung für einen Eingabepin**

Um eine Zuweisung für einen Eingabepin zur Verfügung zu stellen, überschreiben Sie die [**CBaseInputPin::GetAllocator-Methode**](cbaseinputpin-getallocator.md) des Eingabepins. Überprüfen Sie in dieser Methode die **m \_ pAllocator-Membervariable.** Wenn diese Variable nicht NULL **ist,** bedeutet dies, dass die Zuweisung bereits für diese Verbindung ausgewählt wurde, sodass die **GetAllocator-Methode** einen Zeiger auf diese Zuweisung zurückgeben muss. Wenn **m \_ pAllocator** **NULL ist,** bedeutet dies, dass die Zuweisung nicht ausgewählt wurde, sodass die **GetAllocator-Methode** einen Zeiger auf die bevorzugte Zuweisung des Eingabepins zurückgeben sollte. Erstellen Sie in diesem Fall eine Instanz Ihrer benutzerdefinierten Zuweisung, und geben Sie den [**IMemAllocator-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) zurück. Der folgende Code zeigt, wie die **GetAllocator-Methode implementiert** wird:


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Wenn der Upstreamfilter eine Zuweisung auswählt, ruft er die [**IMemInputPin::NotifyAllocator-Methode des Eingabepins**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) auf. Überschreiben Sie [**die CBaseInputPin::NotifyAllocator-Methode,**](cbaseinputpin-notifyallocator.md) um die Zuweisungseigenschaften zu überprüfen. In einigen Fällen kann der Eingabepin die Zuweisung ablehnen, wenn es sich nicht um Ihre benutzerdefinierte Zuweisung handelt, obwohl dies dazu führen kann, dass die gesamte Pinverbindung fehlschlägt.

**Bereitstellen einer benutzerdefinierten Zuweisung für einen Ausgabepin**

Um eine Zuweisung für einen Ausgabepin zur Verfügung zu stellen, überschreiben Sie die [**CBaseOutputPin::InitAllocator-Methode,**](cbaseoutputpin-initallocator.md) um eine Instanz Ihrer Zuweisung zu erstellen:


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Standardmäßig fordert die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) zuerst eine Zuweisung vom Eingabepin an. Wenn diese Zuweisung nicht geeignet ist, erstellt der Ausgabepin eine eigene Zuweisung. Um zu erzwingen, dass die Verbindung Ihre benutzerdefinierte Zuweisung verwendet, überschreiben Sie [**die CBaseOutputPin::D ecideAllocator-Methode.**](cbaseoutputpin-decideallocator.md) Beachten Sie jedoch, dass dadurch verhindert werden kann, dass Ihr Ausgabepin eine Verbindung mit bestimmten Filtern herstellen kann, da der andere Filter möglicherweise auch eine eigene benutzerdefinierte Zuweisung erfordert. Eine dritte Möglichkeit besteht im Wechseln der Reihenfolge: Testen Sie zuerst Ihre benutzerdefinierte Zuweisung, und lehnen Sie dann auf die Zuweisung des anderen Filters ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aushandeln von Zuweisungen](negotiating-allocators.md)
</dt> </dl>

 

 



