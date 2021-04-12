---
title: Hosting des Windows Media Player-Steuer Elements in einer Windows-Anwendung
description: Hosting des Windows Media Player-Steuer Elements in einer Windows-Anwendung
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Windows-basierte Programme
- Windows Media Player-Objektmodell, Windows-basierte Programme
- Objektmodell, Windows-basierte Programme
- Windows Media Player Mobile, Windows-basierte Programme
- Windows Media Player ActiveX-Steuerelement, Windows-basierte Programme
- Windows Media Player Mobile ActiveX-Steuerelement, Windows-basierte Programme
- ActiveX-Steuerelement, Windows-basierte Programme
- Windows-basierte Programm Einbettung
- einbetten, Windows-basierte Programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310767"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="d623f-119">Hosting des Windows Media Player-Steuer Elements in einer Windows-Anwendung</span><span class="sxs-lookup"><span data-stu-id="d623f-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="d623f-120">Wenn Sie das Windows Media Player ActiveX-Steuerelement (einschließlich der Benutzeroberfläche) in einem Windows-basierten Programm verwenden möchten, müssen Sie einen ActiveX-Steuerelement Container bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d623f-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="d623f-121">ATL stellt die **CAxWindow** -Klasse bereit, um die Funktionalität des ActiveX-Host Fensters bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d623f-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="d623f-122">Gehen Sie folgendermaßen vor, um das Windows Media Player-Steuerelement mithilfe der **CAxWindow** -Klasse zu hosten:</span><span class="sxs-lookup"><span data-stu-id="d623f-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="d623f-123">Fügen Sie die folgenden Header ein:</span><span class="sxs-lookup"><span data-stu-id="d623f-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="d623f-124">Deklarieren Sie Member-Variablen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d623f-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="d623f-125">Wenn das Anwendungsfenster erstellt wurde, wird **AtlAxWinInit** aufgerufen, das bei Verwendung des ATL-ActiveX-Host Fensters erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d623f-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="d623f-126">Deklarieren Sie lokale Variablen für Rückgabecodes, und enthalten Sie den Zeiger auf die Schnittstelle des Host Fensters:</span><span class="sxs-lookup"><span data-stu-id="d623f-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="d623f-127">Erstellen Sie das Host Fenster:</span><span class="sxs-lookup"><span data-stu-id="d623f-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="d623f-128">Rufen Sie den Schnittstellen Zeiger des Host Fensters ab:</span><span class="sxs-lookup"><span data-stu-id="d623f-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="d623f-129">Erstellen Sie das Windows Media Player-Steuerelement im Host Fenster mit der Klassen-ID:</span><span class="sxs-lookup"><span data-stu-id="d623f-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="d623f-130">Rufen Sie den **iwmpplayer** -Schnittstellen Zeiger ab:</span><span class="sxs-lookup"><span data-stu-id="d623f-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="d623f-131">Wenn Sie eigenen Code schreiben, achten Sie darauf, jeden **HRESULT** -Rückgabecode auf Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d623f-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="d623f-132">Ein umfassendes Beispiel, das veranschaulicht, wie das Windows Media Player ActiveX-Steuerelement mithilfe der **CAxWindow** -Klasse gehostet wird, finden Sie im wmphost-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d623f-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="d623f-133">Hosting des Windows Media Player 10 Mobile-Steuer Elements in Windows CE</span><span class="sxs-lookup"><span data-stu-id="d623f-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="d623f-134">Wenn Sie Windows CE basierte Anwendungen entwickeln, die ein Windows Media Player 10 Mobile-Steuerelement hosten, müssen Microsoft Embedded Visual C++ 4,0 und das Pocket PC 2003 SDK oder das Smartphone 2003 SDK installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d623f-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="d623f-135">Im Gegensatz zu ATL für Windows unterstützt ATL für Windows CE das Apartment Threading Modell nicht.</span><span class="sxs-lookup"><span data-stu-id="d623f-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="d623f-136">Daher müssen Sie alle Instanzen von Apartment Threading in Ihrem ATL-Projekt suchen und diese ändern, um das kostenlose Threading zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d623f-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d623f-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d623f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d623f-138">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="d623f-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="d623f-139">**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**</span><span class="sxs-lookup"><span data-stu-id="d623f-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




