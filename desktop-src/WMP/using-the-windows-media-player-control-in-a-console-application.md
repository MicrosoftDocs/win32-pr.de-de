---
title: Verwenden des Windows Media Player-Steuer Elements in einer Konsolenanwendung
description: Verwenden des Windows Media Player-Steuer Elements in einer Konsolenanwendung
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Konsolen Anwendungen
- Windows Media Player-Objektmodell, Konsolen Anwendungen
- Objektmodell, Konsolen Anwendungen
- Windows Media Player Mobile, Konsolen Anwendungen
- Windows Media Player ActiveX-Steuerelement, Konsolen Anwendungen
- Windows Media Player Mobile ActiveX-Steuerelement, Konsolen Anwendungen
- ActiveX-Steuerelement, Konsolen Anwendungen
- Einbetten von Konsolen Anwendungen
- einbetten, Konsolen Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310392"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Verwenden des Windows Media Player-Steuer Elements in einer Konsolenanwendung

Sie können eine Instanz des COM-Objekts von Windows Media Player direkt mithilfe von **cokreateinstance** erstellen. Wenn Sie dies tun, zeigt das **Player** -Objekt keine Benutzeroberfläche an. Das-Objekt ist jedoch weiterhin nützlich für Aufgaben, die die Benutzeroberfläche nicht benötigen, z. b. das Arbeiten mit der Bibliothek, das Abspielen digitaler Audiodateien oder das Zugreifen auf die Eigenschaften des Players.

Der folgende Beispielcode zeigt ein einfaches Konsolenprogramm, das die Windows Media Player-Version in einem Meldungs Feld anzeigt. Der Beispielcode verwendet ATL, um intelligente Zeiger und die **CComBSTR** -Zeichen folgen Klasse zu nutzen.


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




