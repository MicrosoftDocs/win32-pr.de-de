---
title: Ändern der Scale-Eigenschaft
description: Ändern der Scale-Eigenschaft
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player Plug-Ins, Echo-Beispieleigenschaften
- Plug-Ins, Echo-Beispieleigenschaften
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispieleigenschaften
- DSP-Plug-Ins, Echo-Beispieleigenschaften
- Echo-DSP-Plug-In-Beispiel, Scale-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10073e01213469dcb6a85ddffd378421fddb6ae8f2fd432b9822c3a5046fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574617"
---
# <a name="modifying-the-scale-property"></a>Ändern der Scale-Eigenschaft

Die Standardmäßige Assistentenimplementierungen machen die Skalierungseigenschaft verfügbar. Sie können die vorhandene Implementierung ändern, um stattdessen die Verzögerungszeiteigenschaft verfügbar zu machen.

Verwenden Sie zunächst das folgende Beispiel, um die Funktionsprototypen für die Skalierung zu ändern \_ und die Skalierung in \_ Echo.h zu versetzen. Ändern Sie den Namen der Methoden und Datentypen für die Parameter:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Ändern Sie als Nächstes die Implementierungen der Get \_ Scale-Methode, und legen Sie \_ Skalierungsmethoden in Echo.cpp ab. Stellen Sie sicher, dass der Code mit den folgenden Beispielen übereinstimmt:


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



Im vorangehenden Beispielcode werden die Methodennamen und die Parameterdatentypen geändert. Der Name der Membervariablen sollte zuvor geändert worden sein. Denken Sie daran, die Kommentare zu ändern, die auch die einzelnen Methoden einführen.

Ändern Sie nun die Schnittstellendefinition. Der folgende Code ersetzt den Code in der IEcho-Schnittstellendeklaration in Echo.idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo Sample Properties**](echo-sample-properties.md)
</dt> </dl>

 

 




