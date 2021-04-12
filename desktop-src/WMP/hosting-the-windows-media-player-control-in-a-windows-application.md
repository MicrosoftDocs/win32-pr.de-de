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
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hosting des Windows Media Player-Steuer Elements in einer Windows-Anwendung

Wenn Sie das Windows Media Player ActiveX-Steuerelement (einschließlich der Benutzeroberfläche) in einem Windows-basierten Programm verwenden möchten, müssen Sie einen ActiveX-Steuerelement Container bereitstellen. ATL stellt die **CAxWindow** -Klasse bereit, um die Funktionalität des ActiveX-Host Fensters bereitzustellen.

Gehen Sie folgendermaßen vor, um das Windows Media Player-Steuerelement mithilfe der **CAxWindow** -Klasse zu hosten:

1.  Fügen Sie die folgenden Header ein:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Deklarieren Sie Member-Variablen wie folgt:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Wenn das Anwendungsfenster erstellt wurde, wird **AtlAxWinInit** aufgerufen, das bei Verwendung des ATL-ActiveX-Host Fensters erforderlich ist.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Deklarieren Sie lokale Variablen für Rückgabecodes, und enthalten Sie den Zeiger auf die Schnittstelle des Host Fensters:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Erstellen Sie das Host Fenster:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Rufen Sie den Schnittstellen Zeiger des Host Fensters ab:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Erstellen Sie das Windows Media Player-Steuerelement im Host Fenster mit der Klassen-ID:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Rufen Sie den **iwmpplayer** -Schnittstellen Zeiger ab:
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Wenn Sie eigenen Code schreiben, achten Sie darauf, jeden **HRESULT** -Rückgabecode auf Fehler zu überprüfen.

Ein umfassendes Beispiel, das veranschaulicht, wie das Windows Media Player ActiveX-Steuerelement mithilfe der **CAxWindow** -Klasse gehostet wird, finden Sie im wmphost-Beispiel.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hosting des Windows Media Player 10 Mobile-Steuer Elements in Windows CE

Wenn Sie Windows CE basierte Anwendungen entwickeln, die ein Windows Media Player 10 Mobile-Steuerelement hosten, müssen Microsoft Embedded Visual C++ 4,0 und das Pocket PC 2003 SDK oder das Smartphone 2003 SDK installiert werden. Im Gegensatz zu ATL für Windows unterstützt ATL für Windows CE das Apartment Threading Modell nicht. Daher müssen Sie alle Instanzen von Apartment Threading in Ihrem ATL-Projekt suchen und diese ändern, um das kostenlose Threading zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




