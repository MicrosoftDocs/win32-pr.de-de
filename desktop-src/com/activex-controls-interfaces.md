---
title: ActiveX-Steuerelement Schnittstellen
description: ActiveX-Steuerelement Schnittstellen
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338175"
---
# <a name="activex-controls-interfaces"></a>ActiveX-Steuerelement Schnittstellen

Zusätzlich zu anderen Mechanismus für die Kommunikation zwischen dem-Steuerelement und dem Client gibt die ActiveX-Steuerelement Technologie die [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) -und [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) -Schnittstellen für die Kommunikation zwischen Client und Steuerelement an. Es gibt auch die [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Schnittstelle für einfache Steuerelement Container.

Diese drei Schnittstellen sind jedoch spezifisch für Steuerelemente und nicht innerhalb des Kontexts von Steuerelementen im Allgemeinen nützlich. Diese Schnittstellen werden wie folgt definiert.

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

Einige Steuerelemente, wie z. b. ein Gruppenfeld, sind lediglich einfache Container anderer Steuerelemente. In solchen Fällen muss das einfache Steuerelement, das als einfacher Frame bezeichnet wird, nicht alle Container Anforderungen implementieren. Sie kann den größten Teil der Schnittstellen Aufrufe aus den darin enthaltenen Steuerelementen an den Container delegieren, der den einfachen Frame verwaltet. Neben Schnittstellen aufrufen muss der einfache Frame auch mit Windows-Meldungen behandelt werden, die potenziell von Steuerelementen in diesem Bereich stammen. Aus diesem Grund stellt ein Container [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) bereit, damit solche einfachen Frame Steuerelemente Nachrichten bis zum Container übergeben können. [**Premessagefilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) verarbeitet zuerst die Nachricht. [**Postmessagefilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) wird aufgerufen, nachdem der einfache Frame die Nachricht selbst verarbeitet hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




