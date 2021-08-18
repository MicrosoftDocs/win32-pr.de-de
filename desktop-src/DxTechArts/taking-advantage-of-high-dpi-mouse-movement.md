---
title: Nutzen der High-Definition Mausbewegung
description: In diesem Artikel geht es um die beste Möglichkeit, die Leistung von High-Definition-Mauseingaben in einem Spiel wie einem Erstperson-Spieler zu optimieren.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7a6efe6916ad8605e3cdc056ffd716ac5113b66c022b0a95fd8a78b1a62e30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042390"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Nutzen der High-Definition Mausbewegung

Eine Standard-Computermaus gibt Daten bei 400 DPI (Dots per Inch) zurück, während eine HdM-Maus Daten mit mindestens 800 DPI generiert. Dadurch wird die Eingabe von einer hdind-Maus viel präziser als die Eingabe mit einer Standardmaus. Allerdings können high-definition-Daten nicht über die standardmäßigen WM \_ MOUSEMOVE-Meldungen erhalten werden. Im Allgemeinen profitieren Spiele von leistungsstarken Mausgeräten, aber Spiele, die Mausdaten nur mitHILFE von WM MOUSEMOVE abrufen, können nicht auf die vollständige, ungefilterte Auflösung der Maus \_ zugreifen.

Eine Reihe von Unternehmen stellt High-Definition-Mausgeräte her, z. B. Microsoft und Logitech. Mit der zunehmenden Beliebtheit von hochauflösenden Mausgeräten ist es wichtig, dass Entwickler verstehen, wie die von diesen Geräten generierten Informationen optimal verwendet werden. In diesem Artikel geht es um die beste Möglichkeit, die Leistung von High-Definition-Mauseingaben in einem Spiel wie einem Erstperson-Spieler zu optimieren.

## <a name="retrieving-mouse-movement-data"></a>Abrufen von Mausbewegungsdaten

Hier sind die drei primären Methoden zum Abrufen von Mausdaten:

-   [WM \_ MOUSEMOVE](/windows)
-   [\_WM-EINGABE](/windows)
-   [DirectInput](#directinput)

Je nachdem, wie die Daten verwendet werden, gibt es Vor- und Nachteile für jede Methode.

### <a name="wm_mousemove"></a>WM \_ MOUSEMOVE

Die einfachste Methode zum Lesen von Mausbewegungsdaten ist das Lesen von WM \_ MOUSEMOVE-Nachrichten. Im Folgenden finden Sie ein Beispiel für das Lesen von Mausbewegungsdaten aus der WM \_ MOUSEMOVE-Meldung:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

Der Hauptnachteil von Daten von WM \_ MOUSEMOVE ist, dass sie auf die Bildschirmauflösung beschränkt sind. Dies bedeutet, dass keine WM MOUSEMOVE-Meldung generiert wird, wenn Sie die Maus leicht bewegen – aber nicht genug, um den Zeiger zum nächsten Pixel zu \_ bewegen. Daher negiert die Verwendung dieser Methode zum Lesen von Mausbewegungen die Vorteile von High-Definition-Eingaben.

Der Vorteil von WM MOUSEMOVE ist jedoch, dass Windows die Zeigerbeschleunigung (auch als "Ballistik" bezeichnet) auf die rohen Mausdaten angewendet, wodurch sich der Mauszeiger wie erwartet \_ verhält. Dies macht WM MOUSEMOVE zur bevorzugten Option für die Zeigersteuerung (über WM INPUT oder \_ DirectInput), da dies zu einem natürlicheren Verhalten \_ für Benutzer führt. WM MOUSEMOVE eignet sich zwar ideal zum Bewegen von Mauszeigern, eignet sich jedoch nicht so gut zum Bewegen einer Erstpersonkamera, da die hohe Genauigkeit \_ verloren geht.

Weitere Informationen zu WM \_ MOUSEMOVE finden Sie unter [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>\_WM-EINGABE

Die zweite Methode zum Abrufen von Mausdaten ist das Lesen von WM \_ INPUT-Nachrichten. Die Verarbeitung von WM INPUT-Nachrichten ist komplizierter als die Verarbeitung von WM MOUSEMOVE-Nachrichten, aber WM INPUT-Nachrichten werden direkt aus dem \_ \_ Eingabegeräte-Stapel (HID) gelesen und spiegeln ergebnisse mit hoher Definition \_ wider.

Um Mausbewegungsdaten aus der WM INPUT-Nachricht zu lesen, muss das Gerät zuerst registriert werden. Der folgende Code \_ enthält ein Beispiel dafür:

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

Der folgende Code verarbeitet WM \_ INPUT-Meldungen im WinProc-Handler der Anwendung:

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

Der Vorteil der Verwendung von WM INPUT ist, dass Ihr Spiel rohe Daten von der Maus auf \_ der niedrigsten möglichen Ebene empfängt.

Der Nachteil ist, dass WM INPUT keine Ballistik auf seine Daten angewendet hat. Wenn Sie also einen Cursor mit diesen Daten bewegen möchten, ist zusätzlicher Aufwand erforderlich, damit sich der Cursor wie in der \_ Windows. Weitere Informationen zum Anwenden von Zeigerballistik finden Sie unter [Zeigerballistik für](https://www.microsoft.com/whdc/archive/pointer-bal.mspx)Windows XP .

Weitere Informationen zu WM \_ INPUT finden Sie unter About Raw [Input](/windows/desktop/inputdev/about-raw-input).

### <a name="directinput"></a>DirectInput

[DirectInput ist](/windows-hardware/drivers/hid/directinput) eine Gruppe von API-Aufrufen, die Eingabegeräte im System abstrahiert. Intern erstellt DirectInput einen zweiten Thread zum Lesen von WM INPUT-Daten, und die Verwendung der DirectInput-APIs führt zu mehr Aufwand als das direkte Lesen \_ von WM \_ INPUT. DirectInput ist nur nützlich zum Lesen von Daten aus DirectInput-Beschriftungen. Wenn Sie jedoch nur den Xbox 360-Controller für Windows müssen, verwenden Sie [stattdessen XInput.](/windows/desktop/xinput/xinput-game-controller-apis-portal) Insgesamt bietet die Verwendung von DirectInput keine Vorteile beim Lesen von Daten von Maus- oder Tastaturgeräten, und die Verwendung von DirectInput in diesen Szenarien wird davon abgeraten.

Vergleichen Sie die Komplexität der Verwendung [von DirectInput](/windows-hardware/drivers/hid/directinput), wie im folgenden Code gezeigt, mit den zuvor beschriebenen Methoden. Die folgenden Aufrufe sind erforderlich, um eine DirectInput-Maus zu erstellen:

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

Anschließend kann das DirectInput-Mausgerät für jeden Frame gelesen werden:

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>Zusammenfassung

Insgesamt ist WM INPUT die beste Methode zum Empfangen von Daten zur Mausbewegung mit hoher \_ Definition. Wenn Ihre Benutzer nur einen Mauszeiger bewegen, sollten Sie WM MOUSEMOVE verwenden, um zu vermeiden, dass \_ Zeigerballistiken verwendet werden müssen. Beide Fenstermeldungen funktionieren auch dann gut, wenn es sich bei der Maus nicht um eine hdind-Maus handelt. Durch die Unterstützung von High Definition Windows Können Spiele benutzern eine präzisere Kontrolle bieten.