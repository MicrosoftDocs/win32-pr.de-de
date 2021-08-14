---
title: Behandeln von Ereignissen in C++
description: Behandeln von Ereignissen in C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player,C++
- Windows Media Player-Objektmodell, C++
- Objektmodell, C++
- Windows Media Player Mobil, C++
- Windows Media Player ActiveX-Steuerelement, C++
- Windows Media Player Mobiles ActiveX-Steuerelement, C++
- ActiveX-Steuerelement, C++
- Einbetten von C++-Programmen
- Einbetten, C++-Programme
- Windows Media Player ActiveX-Steuerelement, Ereignisbehandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignisbehandlung
- ActiveX-Steuerelement, Ereignisbehandlung
- Ereignisse, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5d50be4622cee9ee455710f8b9d2e4cafc63d6560e08faf5c3deaddcdaccc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748405"
---
# <a name="handling-events-in-c"></a>Behandeln von Ereignissen in C++

Sie können Ereignisse von Windows Media Player auf zwei Arten empfangen.

-   Über **IDispatch** mithilfe der **\_ WMPOCXEvents-Schnittstelle.** Dies ist die Schnittstelle, die für die meisten Einbettungsszenarien verwendet werden soll.
-   Über die **IWMPEvents-Schnittstelle.** Diese Schnittstelle ist verfügbar, wenn Ihr Code mit dem Vollmodus-Player verbunden ist, z. B. beim Remoting des Windows Media Player-Steuerelements oder in einem Benutzeroberflächen-Plug-In.

In jedem Szenario beginnen Sie mit dem Lauschen auf Ereignisse, indem Sie COM-Verbindungspunkte verwenden.

Im folgenden Beispielcode werden drei Membervariablen verwendet:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Um einen Verbindungspunkt abzurufen, müssen Sie zunächst **QueryInterface** für den Verbindungspunktcontainer erstellen.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Fordern Sie als Nächstes den Verbindungspunkt für die Ereignisschnittstelle an, die Sie verwenden möchten. Im folgenden Beispielcode wird zunächst versucht, **IWMPEvents** zu verwenden. Wenn diese Schnittstelle nicht verfügbar ist, wird **\_ WMPOCXEvents** verwendet.


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



Rufen Sie abschließend **IConnectionPoint::Advise** auf, um Ereignisse anzufordern.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



Im vorherigen Beispiel geht der erste Parameter davon aus, dass die aufrufende Klasse sowohl **IWMPEvents** als auch **\_ WMPOCXEvents** implementiert. Der zweite Parameter ist ein Rückgabewert, den Sie verwenden, um das Lauschen auf Ereignisse zu beenden, z. B. wenn das Programm beendet wird, indem Sie Code wie den folgenden verwenden:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



Die Implementierung der Ereignishandler für **IWMPEvents** und **\_ WMPOCXEvents** unterscheidet sich. Für **IWMPEvents** müssen Sie eine Funktion implementieren, um jedes von der Schnittstelle definierte Ereignis zu behandeln, auch wenn Sie nicht beabsichtigen, das Ereignis zu verwenden.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Um **\_ WMPOCXEvents-Handler** zu implementieren, müssen Sie **IDispatch::Invoke** verwenden. Dabei handelt es sich um eine einzelne Ereignishandlerimplementierung für alle Ereignisse, die auf der **IDispatch-Schnittstelle** stattfinden. Dies bedeutet, dass Sie nur bestimmte Ereignisse behandeln und andere ignorieren können. Der folgende Beispielcode zeigt einen **\_ WMPOCXEvents-Handler** unter Verwendung von **Invoke,** der nur die **Ereignisse OpenStateChange** und **PlayStateChange** behandelt:


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



Im vorherigen Beispielcode ruft jeder Fall einfach den **IWMPEvents-Handler** für das entsprechende Ereignis auf. Wenn Ihr Code nur **\_ WMPOCXEvents** verarbeitet, können Sie einfach eine benutzerdefinierte Funktion aufrufen oder das Ereignis inline nach der **case-Anweisung** behandeln.

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>Empfangen von Ereignissen von Windows Media Player 10 Mobile

Das Windows Media Player 10 Mobile-Steuerelement unterstützt nur das Empfangen bestimmter Ereignisse über **\_ WMPOCXEvents** und **IWMPEvents.** Weitere Informationen finden Sie in der Dokumentation zu **IWMPEvents.**

## <a name="samples"></a>Beispiele

Das setup-Paket Windows Media Player installiert ein Beispiel, das die Ereignisbehandlung veranschaulicht. Weitere Informationen finden Sie im WMPHost-Beispiel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuerelements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




