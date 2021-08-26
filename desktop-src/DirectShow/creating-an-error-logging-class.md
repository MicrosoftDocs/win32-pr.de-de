---
description: In diesem Thema wird beschrieben, wie Sie die Fehlerprotokollierung in DirectShow Editing Services implementieren.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Erstellen einer Fehlerprotokollierungsklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 194d927b2e4eae73f75a326ed03363d96f6121634e46b606ba87409e3bf07f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108200"
---
# <a name="creating-an-error-logging-class"></a>Erstellen einer Fehlerprotokollierungsklasse

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

In diesem Thema wird beschrieben, wie die Fehlerprotokollierung in [DirectShow Editing Services implementiert wird.](directshow-editing-services.md)

Deklarieren Sie zunächst eine Klasse, die die Fehlerprotokollierung implementiert. Die -Klasse erbt die [**IAMErrorLog-Schnittstelle.**](iamerrorlog.md) Sie enthält Deklarationen für die drei **IUnknown-Methoden** und für die einzelne Methode in [IAMErrorLog](implementing-iamerrorlog.md). Die Klassendeklaration lautet wie folgt:


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



Die einzige Membervariable in der -Klasse ist m \_ lRef, die die Verweisanzahl des Objekts enthält.

Definieren Sie als Nächstes die Methoden in **IUnknown**. Das folgende Beispiel zeigt eine Standardimplementierung für diese Methoden:


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



Wenn das COM-Framework implementiert ist, können Sie jetzt die **IAMErrorLog-Schnittstelle** implementieren. Im nächsten Abschnitt wird dies beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungsfehler](logging-errors.md)
</dt> </dl>

 

 



