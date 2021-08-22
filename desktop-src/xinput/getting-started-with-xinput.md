---
title: Erste Schritte mit XInput
description: XInput ist eine API, mit der Anwendungen Eingaben vom Xbox Controller für Windows empfangen können. Controller-Rumble-Effekte sowie Spracheingabe und -ausgabe werden unterstützt.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a9ca17e3046db676887290b9b9dcbb7318f2dc89d4dd9543cbe790bf271b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962499"
---
# <a name="getting-started-with-xinput"></a>Erste Schritte mit XInput

XInput ist eine API, mit der Anwendungen Eingaben vom Xbox Controller für Windows empfangen können. Controller-Rumble-Effekte sowie Spracheingabe und -ausgabe werden unterstützt.

Dieses Thema bietet eine kurze Übersicht über die Funktionen von XInput und die Einrichtung in einer Anwendung. Dies umfasst Folgendes:

-   [Einführung in XInput](#introduction-to-xinput)
    -   [The Xbox Controller](#the-xbox-controller)
-   [Verwenden von XInput](#using-xinput)
    -   [Mehrere Controller](#multiple-controllers)
    -   [Abrufen des Controllerzustands](#getting-controller-state)
    -   [In tote Zone](#dead-zone)
    -   [Festlegen von Schwingungseffekten](#setting-vibration-effects)
    -   [Abrufen von Audiogerätebezeichnern](#getting-audio-device-identifiers)
    -   [Abrufen von DirectSound-GUIDs (nur Legacy-DirectX SDK)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-xinput"></a>Einführung in XInput

Die Xbox-Konsole verwendet einen Gamingcontroller, der mit Windows kompatibel ist. Anwendungen können die XInput-API verwenden, um mit diesen Controllern zu kommunizieren, wenn sie an einen Windows PC angeschlossen sind (bis zu vier eindeutige Controller können gleichzeitig angeschlossen werden).

Mit dieser API kann jeder verbundene Xbox Controller nach seinem Zustand abgefragt und Schwingungseffekte festgelegt werden. Controller, an die das Headset angeschlossen ist, können auch nach Audioeingabe- und Ausgabegeräten abgefragt werden, die mit dem Headset für die Sprachverarbeitung verwendet werden können.

### <a name="the-xbox-controller"></a>The Xbox Controller

Der Xbox Controller verfügt über zwei analoge Richtungsstäbchen, jeweils mit einer digitalen Schaltfläche, zwei analogen Triggern, einem digitalen direktionalen Pad mit vier Richtungen und acht digitalen Schaltflächen. Die Zustände jeder dieser Eingaben werden in der [**XINPUT \_ GAMEPAD-Struktur**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) zurückgegeben, wenn die [**XInputGetState-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) aufgerufen wird.

Der Controller verfügt auch über zwei Schwingungsbringe, um dem Benutzer Force-Feedback-Effekte zu liefern. Die Geschwindigkeiten dieser Vibrationen werden in der [**XINPUT \_ VIBRATION-Struktur**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) angegeben, die an die [**XInputSetState-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) übergeben wird, um Schwingungseffekte festzulegen.

Optional kann ein Headset mit dem Controller verbunden werden. Das Headset verfügt über ein Mikrofon für die Spracheingabe und eine Audioausgabe. Sie können die [**XInputGetAudioDeviceIds-**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) oder legacy [**XInputGetDSoundAudioDeviceGuids-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) aufrufen, um die Gerätebezeichner abzurufen, die den Geräten für mikrofon und audio entsprechen. Anschließend können Sie die [Core Audio-APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) verwenden, um Spracheingaben zu empfangen und Audioausgaben zu senden.

## <a name="using-xinput"></a>Verwenden von XInput

Die Verwendung von XInput ist so einfach wie das Aufrufen der XInput-Funktionen. Mithilfe der XInput-Funktionen können Sie den Controllerzustand abrufen, Headset-Audio-IDs abrufen und Controller-Rumble-Effekte festlegen.

### <a name="multiple-controllers"></a>Mehrere Controller

Die XInput-API unterstützt bis zu vier Controller, die jederzeit verbunden sind. Alle XInput-Funktionen erfordern einen *dwUserIndex-Parameter,* der übergeben wird, um den controller zu identifizieren, der festgelegt oder abgefragt wird. Diese ID liegt im Bereich von 0 bis 3 und wird automatisch von XInput festgelegt. Die Zahl entspricht dem Port, an den der Controller angeschlossen ist, und ist nicht änderbar.

Jeder Controller zeigt an, welche ID er verwendet, indem er einen Quadranten am "Lichtring" in der Mitte des Controllers auslicht. Der *dwUserIndex-Wert* 0 entspricht dem oberen linken Quadranten. Die Nummerierung wird im Uhrzeigersinn um den Ring herum fortgesetzt.

Anwendungen sollten mehrere Controller unterstützen.

### <a name="getting-controller-state"></a>Abrufen des Controllerstatus

Während der gesamten Dauer einer Anwendung erfolgt das Abrufen des Zustands von einem Controller wahrscheinlich am häufigsten. Von Frame zu Frame in einer Spielanwendung sollte der Zustand abgerufen und die Spielinformationen aktualisiert werden, um die Controlleränderungen widerzuspiegeln.

Verwenden Sie zum Abrufen des Zustands die [**XInputGetState-Funktion:**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

Beachten Sie, dass der Rückgabewert von [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) verwendet werden kann, um zu bestimmen, ob der Controller verbunden ist. Anwendungen sollten eine Struktur definieren, die interne Controllerinformationen enthält. Diese Informationen sollten mit den Ergebnissen von **XInputGetState** verglichen werden, um zu bestimmen, welche Änderungen an diesem Frame vorgenommen wurden, z. B. Tastendrucke oder analoge Controllerdelta. Im obigen Beispiel stellt *g \_ Controllers* eine solche Struktur dar.

Nachdem der Zustand in einer [**XINPUT \_ STATE-Struktur**](/windows/desktop/api/XInput/ns-xinput-xinput_state) abgerufen wurde, können Sie ihn auf Änderungen überprüfen und spezifische Informationen zum Controllerzustand abrufen.

Der *dwPacketNumber-Member* der [**XINPUT \_ STATE-Struktur**](/windows/desktop/api/XInput/ns-xinput-xinput_state) kann verwendet werden, um zu überprüfen, ob sich der Zustand des Controllers seit dem letzten Aufruf von [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)geändert hat. Wenn *dwPacketNumber* zwischen zwei sequenziellen Aufrufen von **XInputGetState** nicht geändert wird, hat sich der Zustand nicht geändert. Wenn sich dies unterscheidet, sollte die Anwendung den *Gamepad-Member* der **XINPUT \_ STATE-Struktur** überprüfen, um ausführlichere Zustandsinformationen zu erhalten.

Rufen Sie aus Leistungsgründen nicht [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) für einen "leeren" Benutzerslot für jeden Frame auf. Es wird empfohlen, dass Sie stattdessen alle paar Sekunden Leerraumüberprüfungen für neue Controller durchführen.

### <a name="dead-zone"></a>In tote Zone

Damit Benutzer ein konsistentes Spielerlebnis erhalten, muss Ihr Spiel die intakte Zone ordnungsgemäß implementieren. Bei der intakten Zone handelt es sich um "Bewegungswerte", die vom Controller gemeldet werden, auch wenn die analogen Sticks unverändert und zentriert sind. Es gibt auch eine in dead zone für die zwei analogen Trigger.

> [!Note]  
> Spiele, die XInput verwenden, die keine intime Zone filtern, erhalten schlechtes Spiel. Beachten Sie, dass einige Controller sensibler sind als andere, sodass die zone für unzufällige Daten von Einheit zu Einheit variieren kann. Es wird empfohlen, Ihre Spiele mit mehreren Xbox-Controllern auf verschiedenen Systemen zu testen.

Anwendungen sollten "dead zones" für analoge Eingaben (Trigger, Striche) verwenden, um anzugeben, wann eine Bewegung ausreichend auf dem Stick oder Trigger vorgenommen wurde, um als gültig angesehen zu werden.

Ihre Anwendung sollte auf inaktive Zonen überprüfen und wie im folgenden Beispiel appopriately reagieren:

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

In diesem Beispiel wird der Richtungsvektor des Controllers berechnet, und es wird berechnet, wie weit entlang des Vektors der Controller gepusht wurde. Dies ermöglicht die Erzwingung einer zirkulären in deadzone, indem einfach überprüft wird, ob die Größe des Controllers größer als der Wert für die un tote Zone ist. Darüber hinaus normalisiert der Code die Größe des Controllers, die dann mit einem spielspezifischen Faktor multipliziert werden kann, um die Position des Controllers in für das Spiel relevante Einheiten zu konvertieren.

Beachten Sie, dass Sie ihre eigenen intakten Zonen für die Sticks und Trigger definieren können (zwischen 0 und 65534), oder Sie können die bereitgestellten deadzones verwenden, die als XINPUT \_ GAMEPAD \_ LEFT THUMB \_ \_ DEADZONE, XINPUT \_ GAMEPAD RIGHT THUMB \_ \_ \_ DEADZONE und XINPUT \_ GAMEPAD TRIGGER THRESHOLD in \_ \_ XInput.h definiert sind:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Nachdem die unzustellbare Zone erzwungen wurde, kann es hilfreich sein, den resultierenden Bereich \[ 0.0...1.0 \] gleitkomma (wie im obigen Beispiel) zu skalieren und optional eine nicht lineare Transformation anzuwenden.

Beispielsweise kann es beim Fahren von Spielen hilfreich sein, das Ergebnis zu würfeln, um das Autofahren mithilfe eines Gamepads besser zu gestalten, da das Cubing des Ergebnisses ihnen eine höhere Genauigkeit in den unteren Bereichen bietet. Dies ist wünschenswert, da Gamer in der Regel soft force anwenden, um eine dezente Bewegung zu erhalten, oder harte Kraft in einer Richtung anwenden, um rd-Antworten zu erhalten.

### <a name="setting-vibration-effects"></a>Festlegen von Schwingungseffekten

Zusätzlich zum Abrufen des Zustands des Controllers können Sie auch Schwingungsdaten an den Controller senden, um das Feedback zu ändern, das dem Benutzer des Controllers zur Verfügung gestellt wird. Der Controller enthält zwei Rumble-Schaltungen, die unabhängig gesteuert werden können, indem Werte an die [**XInputSetState-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) übergeben werden.

Die Geschwindigkeit jedes Motor kann mithilfe eines WORD-Werts in der [**XINPUT \_ VIBRATION-Struktur**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) angegeben werden, der wie folgt an die [**XInputSetState-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) übergeben wird:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Beachten Sie, dass der rechte Motor der Hochfrequenz-Motor und der linke Motor der Motor mit niedriger Frequenz ist. Sie müssen nicht immer auf die gleiche Menge festgelegt werden, da sie unterschiedliche Auswirkungen haben.

### <a name="getting-audio-device-identifiers"></a>Abrufen von Audiogerätebezeichnern

Das Headset für einen Xbox Controller verfügt über die folgenden Funktionen:

-   Aufzeichnen von Sound mithilfe eines Mikrofons
-   Wiedergeben von Sound mithilfe eines Rauschens

Verwenden Sie diesen Code, um die Gerätebezeichner für das Headset abzurufen:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Nachdem Sie die Gerätebezeichner erhalten haben, können Sie die entsprechenden Schnittstellen erstellen. Wenn Sie beispielsweise XAudio 2.8 verwenden, verwenden Sie diesen Code, um eine Masteringstimme für dieses Gerät zu erstellen:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Informationen zur Verwendung des CaptureId-Gerätebezeichners finden Sie unter [Erfassen eines Streams.](/windows/desktop/CoreAudio/capturing-a-stream)

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Abrufen von DirectSound-GUIDs (nur Legacy-DirectX SDK)

Das Headset, das mit einem Xbox Controller verbunden werden kann, verfügt über zwei Funktionen: Es kann Sound mithilfe eines Mikrofons aufzeichnen und sound mithilfe eines Sprechgeräts wiedergeben. In der XInput-API werden diese Funktionen über [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))mithilfe der Schnittstellen **IDirectSound8** und **IDirectSoundCapture8** ausgeführt.

Um das Mikrofon und die Mikrofone des Headsets den entsprechenden [DirectSound-Schnittstellen](/previous-versions/windows/desktop/ee416960(v=vs.85)) zuzuordnen, müssen Sie die DirectSoundGUIDs für die Erfassungs- und Rendergeräte abrufen, indem Sie [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids)aufrufen.

> [!Note]  
> Die Verwendung des [Legacy-DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) wird nicht empfohlen und ist in Windows Store-Apps nicht verfügbar. Die Informationen in diesem Abschnitt gelten nur für die DirectX SDK-Version von XInput (XInput 1.3). Die Windows 8 Version von XInput (XInput 1.4) verwendet ausschließlich Windows WASAPI-Gerätebezeichner (Audio Session API), die über [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)abgerufen werden.

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Nachdem Sie die GUIDs abgerufen haben, können Sie die entsprechenden Schnittstellen erstellen, indem Sie DirectSoundCreate8 und DirectSoundCaptureCreate8 wie folgt aufrufen:

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a>Zugehörige Themen

[Programmierverzeichnis](programming-reference.md)