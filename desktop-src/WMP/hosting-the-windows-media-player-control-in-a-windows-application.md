---
title: Hosten des Windows Media Player-Steuerelements in einer Windows Anwendung
description: Hosten des Windows Media Player-Steuerelements in einer Windows Anwendung
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player,einbetten ActiveX Steuerelement
- Windows Media Player-Objektmodell, Einbetten ActiveX Steuerelement
- Objektmodell,Einbetten ActiveX Steuerelement
- Windows Media Player Mobil,einbetten ActiveX Steuerelement
- Windows Media Player ActiveX,Einbetten
- Windows Media Player Mobile ActiveX-Steuerelement,Einbetten
- ActiveX,Einbetten
- Windows Media Player,Windows-basierten Programmen
- Windows Media Player Objektmodell,Windows-basierte Programme
- Objektmodell,Windows-basierte Programme
- Windows Media Player Mobile, Windows-basierte Programme
- Windows Media Player ActiveX,Windows-basierte Programme
- Windows Media Player Mobile ActiveX-Steuerelement, Windows-basierte Programme
- ActiveX,Windows-basierte Programme
- Windows-basiertes Einbetten von Programmen
- Einbetten, Windows-basierten Programmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3c2b4d84194376bd16842f0a9567c83fce2aa616ed4bfef4f20f7255068e8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748277"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hosten des Windows Media Player-Steuerelements in einer Windows Anwendung

Um das Windows Media Player ActiveX -Steuerelement (einschließlich der Benutzeroberfläche) in einem Windows-basierten Programm zu verwenden, müssen Sie einen ActiveX bereitstellen. ATL stellt die **CAxWindow-Klasse** zur Verfügung, um ActiveX Hostfensterfunktionalität zu bieten.

Um das Steuerelement Windows Media Player **CAxWindow-Klasse zu hosten,** führen Sie die folgenden Schritte aus:

1.  Schließen Sie die folgenden Header ein:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Deklarieren Sie Membervariablen wie folgt:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Wenn Ihr Anwendungsfenster erstellt wird, rufen **Sie AtlAxWinInit** auf. Dies ist erforderlich, wenn Sie das ATL ActiveX Hostfenster verwenden.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Deklarieren Sie lokale Variablen für Rückgabecodes und , um den Zeiger auf die Hostfensterschnittstelle zu enthalten:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Erstellen Sie das Hostfenster:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Rufen Sie den Hostfenster-Schnittstellenzeiger ab:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Erstellen Sie Windows Media Player-Steuerelement im Hostfenster mithilfe der Klassen-ID:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Rufen Sie den **IWMPPlayer-Schnittstellenzeiger** ab:
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Wenn Sie ihren eigenen Code schreiben, überprüfen Sie jeden **HRESULT-Rückgabecode** auf Fehler.

Ein vollständiges Beispiel, das das Hosten des Windows Media Player ActiveX-Steuerelements mithilfe der **CAxWindow-Klasse** veranschaulicht, finden Sie im WMPHost-Beispiel.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hosten des Windows Media Player 10 Mobile-Steuerelements in Windows CE

Microsoft eMbedded Visual C++ 4.0 und das Pocket PC 2003 SDK oder das Smartphone 2003 SDK müssen installiert werden, wenn sie Windows CE-basierte Anwendungen entwickeln, die ein Windows Media Player 10 Mobile-Steuerelement hosten. Im Gegensatz zu ATL für Windows unterstützt ATL für Windows CE auch das Apartmentthreadingmodell nicht. Daher müssen Sie alle Instanzen des Apartmentthreadings in Ihrem ATL-Projekt finden und ändern, um free threading zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuerelements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




