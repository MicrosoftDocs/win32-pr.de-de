---
title: Ändern der Scale-Eigenschaft
description: Ändern der Scale-Eigenschaft
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Scale-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338580"
---
# <a name="modifying-the-scale-property"></a>Ändern der Scale-Eigenschaft

Die Standard Implementierung des Assistenten macht die Scale-Eigenschaft verfügbar. Sie können die vorhandene Implementierung ändern, um stattdessen die Eigenschaft Verzögerungszeit verfügbar zu machen.

Verwenden Sie zunächst das folgende Beispiel, um die Funktionsprototypen für get \_ Scale und Put \_ Scale in Echo. h zu ändern. Ändern Sie den Namen der Methoden und Datentypen für die Parameter:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Ändern Sie als nächstes die Implementierungen der \_ Methoden get Scale und Put \_ Scale in Echo. cpp. Stellen Sie den Code den folgenden Beispielen entsprechend dar:


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



Im vorherigen Beispielcode werden die Methodennamen und die Parameter Datentypen geändert. Der Name der Element Variablen sollte zuvor geändert worden sein. Denken Sie daran, die Kommentare zu ändern, in denen auch die einzelnen Methoden eingeführt werden.

Ändern Sie nun die Schnittstellen Definition. Der folgende Code ersetzt den Code in der IEcho-Schnittstellen Deklaration in Echo. idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo-Beispiel Eigenschaften**](echo-sample-properties.md)
</dt> </dl>

 

 




