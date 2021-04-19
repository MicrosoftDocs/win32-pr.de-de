---
description: In diesem Thema wird beschrieben, wie die Fehler Protokollierung in DirectShow-Bearbeitungs Diensten implementiert wird.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Erstellen einer Fehler Protokollierungs Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346005"
---
# <a name="creating-an-error-logging-class"></a>Erstellen einer Fehler Protokollierungs Klasse

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Thema wird beschrieben, wie die Fehler Protokollierung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md)implementiert wird.

Deklarieren Sie zuerst eine Klasse, die die Fehler Protokollierung implementiert. Die Klasse erbt die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle. Sie enthält Deklarationen für die drei **IUnknown** -Methoden und für die einzige Methode in [iamerrorlog](implementing-iamerrorlog.md). Die Klassen Deklaration lautet wie folgt:


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



Die einzige Member-Variable in der-Klasse ist m \_ lref, die den Verweis Zähler des Objekts enthält.

Definieren Sie als nächstes die Methoden in **IUnknown**. Das folgende Beispiel zeigt eine Standard Implementierung für diese Methoden:


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



Wenn das com-Framework vorhanden ist, können Sie nun die **iamerrorlog** -Schnittstelle implementieren. Im nächsten Abschnitt wird beschrieben, wie dies geschieht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungs Fehler](logging-errors.md)
</dt> </dl>

 

 



