---
description: Bereitstellen einer benutzerdefinierten Zuweisung
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Bereitstellen einer benutzerdefinierten Zuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392521"
---
# <a name="providing-a-custom-allocator"></a>Bereitstellen einer benutzerdefinierten Zuweisung

In diesem Abschnitt wird beschrieben, wie Sie einen benutzerdefinierten Zuweiser für einen Filter bereitstellen. Es werden nur [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Verbindungen beschrieben, die Schritte für eine [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Verbindung sind jedoch ähnlich.

Definieren Sie zuerst eine C++-Klasse für die Zuweisung. Ihre Zuweisung kann von einer der standardzuordnerklassen, [**cbasezucator**](cbaseallocator.md) oder [**cmemzuordcator**](cmemallocator.md)abgeleitet werden, oder Sie können eine vollständig neue zuordnerklasse erstellen. Wenn Sie eine neue Klasse erstellen, muss Sie die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle verfügbar machen.

Die verbleibenden Schritte hängen davon ab, ob ihre Zuweisung zu einer Eingabe-PIN oder einer Ausgabe-PIN in Ihrem Filter gehört. Eingabe Pins spielen während der zuordneraushandlungs Phase eine andere Rolle als Ausgabe Pins, da die Ausgabepin letztendlich die Zuweisung auswählt.

**Bereitstellen einer benutzerdefinierten Zuweisung für eine Eingabe-PIN**

Um eine Zuweisung für eine Eingabe-PIN bereitzustellen, überschreiben Sie die [**cbaseinputpin:: getallocator**](cbaseinputpin-getallocator.md) -Methode der Eingabe-PIN. Überprüfen Sie in dieser Methode die **m \_ pallocator** -Member-Variable. Wenn diese Variable nicht **null** ist, bedeutet dies, dass die Zuweisung bereits für diese Verbindung ausgewählt wurde. Daher muss die **getallocator** -Methode einen Zeiger auf diese Zuweisung zurückgeben. Wenn **m \_ pallocator** **null** ist, bedeutet dies, dass die Zuweisung nicht ausgewählt wurde. Daher sollte die **getallocator** -Methode einen Zeiger auf die bevorzugte Zuweisung der Eingabe-PIN zurückgeben. Erstellen Sie in diesem Fall eine Instanz Ihrer benutzerdefinierten Zuweisung, und geben Sie den [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Zeiger zurück. Der folgende Code zeigt, wie die **getallocator** -Methode implementiert wird:


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



Wenn der upstreamfilter eine Zuweisung auswählt, ruft er die [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode der Eingabe-PIN auf. Überschreiben Sie die [**cbaseinputpin:: notifyzuweisung**](cbaseinputpin-notifyallocator.md) -Methode, um die zuordnereigenschaften zu überprüfen. In einigen Fällen kann die Eingabe-PIN die Zuweisung ablehnen, wenn Sie nicht Ihre benutzerdefinierte Zuweisung ist, obwohl dies dazu führen kann, dass die gesamte Pin-Verbindung fehlschlägt.

**Bereitstellen einer benutzerdefinierten Zuweisung für eine Ausgabepin**

Zum Bereitstellen einer Zuweisung für eine Ausgabepin überschreiben Sie die [**cbaseoutputpin:: initaccesscator**](cbaseoutputpin-initallocator.md) -Methode, um eine Instanz Ihrer Zuweisung zu erstellen:


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



Standardmäßig fordert die [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse zuerst einen Zuweiser von der eingabepin an. Wenn diese Zuweisung nicht geeignet ist, erstellt die Ausgabe-PIN eine eigene Zuweisung. Um die Verbindung mit der benutzerdefinierten Zuweisung zu erzwingen, überschreiben Sie die [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode. Beachten Sie jedoch, dass dadurch verhindert werden kann, dass Ihre Ausgabe-PIN eine Verbindung mit bestimmten Filtern herstellt, da der andere Filter möglicherweise auch eine eigene benutzerdefinierte Zuweisung erfordert. Eine dritte Möglichkeit besteht darin, die Reihenfolge zu ändern: Testen Sie zuerst die benutzerdefinierte Zuweisung, und greifen Sie dann auf die Zuweisung des anderen Filters zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aushandeln von Zuweisungen](negotiating-allocators.md)
</dt> </dl>

 

 



