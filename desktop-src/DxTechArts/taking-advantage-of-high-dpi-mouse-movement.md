---
title: Nutzen der High-Definition Mausbewegung
description: Dieser Artikel konzentriert sich auf die beste Methode zur Optimierung der Leistung von High-Definition-Maus Eingaben in einem Spiel, wie z. b. einem ersten Mitarbeiter.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebe2abd9487d95b8fe12aa3c6938e21d72d8e2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390699"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Nutzen der High-Definition Mausbewegung

Eine Standard Computermaus gibt Daten mit 400 Punkten pro Zoll (dpi) zurück, während eine High-Definition-Maus Daten mit 800 dpi oder höher generiert. Dadurch wird die Eingabe von einer High-Definition-Maus wesentlich präziser als die von der Standard Maus. Hoch Definitionsdaten können jedoch nicht über die standardmäßigen WM- \_ mouset-Nachrichten abgerufen werden. Im Allgemeinen profitieren Spiele von High-Definition-Maus Geräten, aber Spiele, die mithilfe von WM MouseMove Maus Daten abrufen, \_ können nicht auf die vollständige, ungefilterte Auflösung der Maus zugreifen.

Eine Reihe von Unternehmen ist die Herstellung von High-Definition-Maus Geräten, z. b. Microsoft und Logitech. Dank der zunehmenden Beliebtheit von Maus Geräten mit hoher Auflösung ist es wichtig, dass Entwickler wissen, wie die von diesen Geräten generierten Informationen optimal verwendet werden. Dieser Artikel konzentriert sich auf die beste Methode zur Optimierung der Leistung von High-Definition-Maus Eingaben in einem Spiel, wie z. b. einem ersten Mitarbeiter.

## <a name="retrieving-mouse-movement-data"></a>Abrufen von Maus Verschiebungs Daten

Im folgenden sind die drei primären Methoden zum Abrufen von Mausdaten aufgeführt:

-   [WM- \_ mouseelmove](/windows)
-   [WM- \_ Eingabe](/windows)
-   [DirectInput](#directinput)

Jede Methode hat vor-und Nachteile, abhängig davon, wie die Daten verwendet werden.

### <a name="wm_mousemove"></a>WM- \_ mouseelmove

Die einfachste Methode zum Lesen von Maus Verschiebungs Daten ist die Verwendung von WM- \_ MouseMove-Nachrichten. Im folgenden finden Sie ein Beispiel für das Lesen von Maus Verschiebungs Daten aus der WM- \_ MouseMove-Nachricht:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

Der primäre Nachteil von Daten aus WM- \_ mousmove ist, dass Sie auf die Bildschirmauflösung beschränkt ist. Dies bedeutet Folgendes: Wenn Sie die Maus leicht verschieben – aber nicht genug, um den Zeiger auf das nächste Pixel zu bewegen – wird keine WM- \_ MouseMove-Nachricht generiert. Die Verwendung dieser Methode zum Lesen der Mausbewegung negiert die Vorteile der Eingabe von hoch Definitionen.

Der Vorteil von WM \_ MouseMove besteht jedoch darin, dass Windows Zeiger Beschleunigung (auch als "Ballistik" bezeichnet) auf die rohdatenmausdaten anwendet, wodurch sich der Mauszeiger wie erwartet verhält. Dies bewirkt, dass WM \_ MouseMove die bevorzugte Option für das Zeiger Steuerelement (über WM- \_ Eingabe oder DirectInput) ist, da es für Benutzer zu einem natürlicheren Verhalten führt. Während WM \_ MouseMove für das Bewegen von Maus Zeigern ideal ist, ist es nicht so gut, eine erste Person Kamera zu verschieben, da die Genauigkeit der hoch Definition verloren geht.

Weitere Informationen zu WM \_ mousee Move finden Sie unter [**WM \_ mousee Move**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>WM- \_ Eingabe

Die zweite Methode zum Abrufen von Maus Daten ist das Lesen von WM- \_ Eingabe Nachrichten. Die Verarbeitung von WM \_ -Eingabe Nachrichten ist komplizierter als \_ die Verarbeitung von WM-mouset-Nachrichten, aber WM \_ -Eingabe Nachrichten werden direkt aus dem Eingabegeräte (HID)-Stapel gelesen und spiegeln Ergebnisse der hoch Definition wider.

Zum Lesen von Maus Verschiebungs Daten aus der WM- \_ Eingabe Nachricht muss das Gerät zuerst registriert werden. der folgende Code stellt ein Beispiel dafür dar:

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

Der folgende Code behandelt WM \_ -Eingabe Meldungen im WinProc-Handler der Anwendung:

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

Der Vorteil der Verwendung von WM- \_ Eingaben besteht darin, dass Ihr Spiel Rohdaten von der Maus auf der niedrigsten möglichen Ebene empfängt.

Der Nachteil ist, dass \_ für die WM-Eingabe keine Ballistik auf die Daten angewendet wird. Wenn Sie also einen Cursor mit diesen Daten steuern möchten, ist zusätzlicher Aufwand erforderlich, um den Cursor wie in Windows aussehen zu lassen. Weitere Informationen zum Anwenden von zeigereignis finden Sie unter [Zeiger-Ballistik für Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Weitere Informationen zu WM- \_ Eingaben finden Sie unter Informationen [zu](/windows/desktop/inputdev/about-raw-input)unformatierten Eingaben.

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) ist ein Satz von API-aufrufen, mit denen Eingabegeräte auf dem System abstrahiert werden. Intern erstellt DirectInput einen zweiten Thread zum Lesen von WM \_ -Eingabedaten, und die Verwendung der DirectInput-APIs führt zu mehr Aufwand als das einfache Lesen von WM- \_ Eingaben. DirectInput ist nur für das Lesen von Daten aus DirectInput-Joysticks nützlich. Wenn Sie jedoch nur den Xbox 360-Controller für Windows unterstützen müssen, verwenden Sie stattdessen [xinput](/windows/desktop/xinput/xinput-game-controller-apis-portal) . Insgesamt bietet die Verwendung von DirectInput keine Vorteile beim Lesen von Daten von Maus-oder Tastatur Geräten, und die Verwendung von DirectInput in diesen Szenarien wird davon abgeraten.

Vergleichen Sie die Komplexität der Verwendung von [DirectInput](/windows-hardware/drivers/hid/directinput), wie im folgenden Code gezeigt, mit den Methoden, die zuvor beschrieben wurden. Die folgenden Aufrufe sind erforderlich, um eine DirectInput-Maus zu erstellen:

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

Und dann kann das DirectInput-Mausgerät jeden Frame lesen:

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

Insgesamt ist die beste Methode zum Empfangen von Daten mit hoher Definitions Datenbewegung "WM \_ Input". Wenn die Benutzer nur einen Mauszeiger bewegen, erwägen Sie die Verwendung von "WM \_ MouseMove", um zu vermeiden, dass Zeiger-ballistiken durchgeführt werden. Beide Fenster Meldungen funktionieren auch dann gut, wenn die Maus keine High-Definition-Maus ist. Durch die Unterstützung hoher Definitionen können Windows-Spiele Benutzern eine präzisere Kontrolle bieten.