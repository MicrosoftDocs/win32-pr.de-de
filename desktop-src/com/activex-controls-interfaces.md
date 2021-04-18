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
# <a name="activex-controls-interfaces"></a><span data-ttu-id="6634e-103">ActiveX-Steuerelement Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6634e-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="6634e-104">Zusätzlich zu anderen Mechanismus für die Kommunikation zwischen dem-Steuerelement und dem Client gibt die ActiveX-Steuerelement Technologie die [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) -und [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) -Schnittstellen für die Kommunikation zwischen Client und Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="6634e-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="6634e-105">Es gibt auch die [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Schnittstelle für einfache Steuerelement Container.</span><span class="sxs-lookup"><span data-stu-id="6634e-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="6634e-106">Diese drei Schnittstellen sind jedoch spezifisch für Steuerelemente und nicht innerhalb des Kontexts von Steuerelementen im Allgemeinen nützlich.</span><span class="sxs-lookup"><span data-stu-id="6634e-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="6634e-107">Diese Schnittstellen werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="6634e-107">These interfaces are defined as follows.</span></span>

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

<span data-ttu-id="6634e-108">Einige Steuerelemente, wie z. b. ein Gruppenfeld, sind lediglich einfache Container anderer Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="6634e-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="6634e-109">In solchen Fällen muss das einfache Steuerelement, das als einfacher Frame bezeichnet wird, nicht alle Container Anforderungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="6634e-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="6634e-110">Sie kann den größten Teil der Schnittstellen Aufrufe aus den darin enthaltenen Steuerelementen an den Container delegieren, der den einfachen Frame verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6634e-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="6634e-111">Neben Schnittstellen aufrufen muss der einfache Frame auch mit Windows-Meldungen behandelt werden, die potenziell von Steuerelementen in diesem Bereich stammen.</span><span class="sxs-lookup"><span data-stu-id="6634e-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="6634e-112">Aus diesem Grund stellt ein Container [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) bereit, damit solche einfachen Frame Steuerelemente Nachrichten bis zum Container übergeben können.</span><span class="sxs-lookup"><span data-stu-id="6634e-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="6634e-113">[**Premessagefilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) verarbeitet zuerst die Nachricht. [**Postmessagefilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) wird aufgerufen, nachdem der einfache Frame die Nachricht selbst verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="6634e-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6634e-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6634e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6634e-115">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6634e-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




