---
title: Ändern des vom Assistenten generierten Codes
description: Ändern des vom Assistenten generierten Codes
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Windows Media Player Mobile, Plug-ins
- Windows Media Player Mobile, Benutzerschnittstellen-Plug-ins
- Mobile Windows Media Player-Plug-ins
- Plug-ins, Benutzeroberfläche
- Plug-ins, Windows Media Player Mobile
- Plug-Ins für Benutzeroberflächen, Windows Media Player Mobile
- UI-Plug-ins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340440"
---
# <a name="modifying-wizard-generated-code"></a>Ändern des vom Assistenten generierten Codes

Der vom Assistenten generierte Plug-in-Code, den Sie ändern müssen, muss geändert werden, damit das Plug-in mit Windows Media Player 10 Mobile funktioniert. Der Code, den Sie ändern müssen, ist in den folgenden Beispielen fett formatiert.

## <a name="changes-to-wmpplugh"></a>Änderungen an "wmpplug. h"

ANSI-Methoden werden auf Geräten, auf denen Windows CE ausgeführt wird, nicht unterstützt, daher müssen Sie die folgende ANSI-Methode ändern, die vom Assistenten in wmpplug. h generiert wird:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



Ändern Sie die Datei wie im folgenden dargestellt, sodass Sie zu einer Unicode-Methode wird:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>Änderungen an networkplugin. h

Suchen Sie den folgenden Code in der Datei networkplugin. h:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



Ändern Sie den Code so, dass er wie folgt aussieht:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>Änderungen an networkplugindll. cpp

Suchen Sie die **DllMain** -Funktion in networkplugindll. cpp:


```C++
extern "C" BOOL WINAPI DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, hInstance);
        DisableThreadLibraryCalls(hInstance);
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



Ändern Sie den Code so, dass er wie folgt aussieht:


```C++
extern "C" BOOL WINAPI DllMain(HANDLE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, (HINSTANCE)hInstance);
#ifndef UNDER_CE
        DisableThreadLibraryCalls((HINSTANCE)hInstance);
#endif
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



## <a name="changes-to-networkplugincpp"></a>Änderungen an networkplugin. cpp

Suchen Sie den folgenden Code in der Datei networkplugin. cpp:


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



Ändern Sie den Code so, dass er wie folgt aussieht:


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>Ändern des Threading Modells

Anders als ATL für Windows unterstützt ATL für Windows CE das Apartment Threading Modell nicht, da das Apartment Modell mehr Speicherressourcen benötigt als die einzelnen Threading-und freien Threading Modelle. Daher müssen Sie alle Instanzen von Apartment Threading in "stdafx. h" und "networkplugin. RGS" finden und Sie ändern, um das kostenlose Threading anzugeben.

Außerdem können Sie das Windows Media Player 10 Mobile-Steuerelement nur aus dem Thread, in dem er erstellt wurde, abrufen.

## <a name="build-and-test-the-project"></a>Erstellen und Testen des Projekts

Nachdem Sie diese Änderungen hier beschrieben haben, können Sie das Projekt erstellen, um zu überprüfen, ob es kompiliert wird, bevor Sie benutzerdefinierten Code hinzufügen.

1.  Legen Sie die aktive Projekt Konfiguration auf Win32 (WCE ARMV4) Debug oder Win32 (WCE ARMV4)-Release fest.
2.  Legen Sie die aktive Plattform auf Pocket PC 2003 fest.
3.  Klicken Sie auf das Menü Element **Erstellen** , und wählen Sie dann **NetworkPlugin.dllerstellen** aus. Es sollte kompiliert, heruntergeladen und auf Ihrem Gerät registriert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




