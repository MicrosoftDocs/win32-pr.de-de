---
title: Behandeln von Ereignissen in C++
description: Behandeln von Ereignissen in C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Windows Media Player-Objektmodell, C++
- Objektmodell, C++
- Windows Media Player Mobile, C++
- Windows Media Player ActiveX-Steuerelement, C++
- Windows Media Player Mobile ActiveX-Steuerelement, C++
- ActiveX-Steuerelement, C++
- C++-Programm Einbettung
- einbetten, C++-Programme
- Windows Media Player ActiveX-Steuerelement, Ereignis Behandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignis Behandlung
- ActiveX-Steuerelement, Ereignis Behandlung
- Ereignisse, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100746"
---
# <a name="handling-events-in-c"></a>Behandeln von Ereignissen in C++

Sie können Ereignisse von Windows Media Player auf zweierlei Weise empfangen.

-   Über **IDispatch** mithilfe der **\_ wmpocxevents** -Schnittstelle. Dies ist die Schnittstelle, die für die meisten Einbettungs Szenarien verwendet wird.
-   Über die **iwmpevents** -Schnittstelle. Diese Schnittstelle ist verfügbar, wenn Ihr Code mit dem vollmodusplayer verbunden ist, z. b. beim Remoting des Windows Media Player-Steuer Elements oder eines UI-Plug-ins.

In jedem Szenario beginnen Sie mit dem lauschen an Ereignissen mithilfe von com-Verbindungs Punkten.

Der folgende Beispielcode verwendet drei Element Variablen:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Zum Abrufen eines Verbindungs Punkts müssen Sie zuerst **QueryInterface** für den Verbindungspunkt Container durchsuchen.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Fordern Sie als nächstes den Verbindungspunkt für die Ereignis Schnittstelle an, die Sie verwenden möchten. Der folgende Beispielcode versucht zunächst, **iwmpevents** zu verwenden. Wenn diese Schnittstelle nicht verfügbar ist, verwendet Sie **\_ wmpocxevents**.


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



Zum Schluss wird **IConnectionPoint:: Empfehlung** aufgerufen, um Ereignisse anzufordern.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



Im vorherigen Beispiel geht der erste Parameter davon aus, dass die aufrufende Klasse sowohl **iwmpevents** als auch **\_ wmpocxevents** implementiert. Der zweite Parameter ist ein Rückgabewert, den Sie verwenden, um das Lauschen auf Ereignisse zu beenden, z. b. wenn das Programm beendet wird, indem Sie Code wie den folgenden verwenden:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



Das Implementieren von Ereignis Handlern für **iwmpevents** und **\_ wmpocxevents** ist unterschiedlich. Für **iwmpevents** müssen Sie eine Funktion implementieren, die jedes von der-Schnittstelle definierte Ereignis behandelt, auch wenn Sie nicht beabsichtigen, das-Ereignis zu verwenden.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Zum Implementieren von **\_ wmpocxevents** -Handlern müssen Sie **IDispatch:: Aufrufen** verwenden, bei dem es sich um eine Implementierung eines einzelnen Ereignis Handlers für alle Ereignisse handelt, die in der **IDispatch** -Schnittstelle auftreten. Dies bedeutet, dass Sie auswählen können, dass nur bestimmte Ereignisse behandelt und andere ignoriert werden. Der folgende Beispielcode zeigt einen **\_ wmpocxevents** -Handler, der den **Aufruf** verwendet, der nur die Ereignisse **OpenStateChange** und **PlayStateChange** behandelt:


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



Im vorangehenden Beispielcode ruft jeder Fall einfach bis zum **iwmpevents** -Handler für das entsprechende-Ereignis auf. Wenn Ihr Code nur **\_ wmpocxevents** behandelt, können Sie einfach eine benutzerdefinierte Funktion oder das Ereignis nach der **Case** -Anweisung Inline verarbeiten.

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>Empfangen von Ereignissen von Windows Media Player 10 Mobile

Das Windows Media Player 10 Mobile-Steuerelement unterstützt nur das Empfangen bestimmter Ereignisse über **\_ wmpocxevents** und **iwmpevents**. Weitere Informationen finden Sie in der Dokumentation zu **iwmpevents**.

## <a name="samples"></a>Beispiele

Das Windows Media Player Setup-Paket installiert ein Beispiel, das die Ereignis Behandlung veranschaulicht. Weitere Informationen finden Sie im wmphost-Beispiel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




