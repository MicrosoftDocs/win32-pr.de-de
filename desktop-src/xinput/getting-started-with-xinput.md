---
title: Einstieg in xinput
description: Xinput ist eine API, mit der Anwendungen Eingaben vom Xbox-Controller für Windows empfangen können. Die Auswirkungen des Controllers und die Spracheingabe und-Ausgabe werden unterstützt.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727657"
---
# <a name="getting-started-with-xinput"></a>Einstieg in xinput

Xinput ist eine API, mit der Anwendungen Eingaben vom Xbox-Controller für Windows empfangen können. Die Auswirkungen des Controllers und die Spracheingabe und-Ausgabe werden unterstützt.

Dieses Thema enthält eine kurze Übersicht über die Funktionen von XInput und deren Einrichtung in einer Anwendung. Dies umfasst Folgendes:

-   [Einführung in xinput](#introduction-to-xinput)
    -   [Der Xbox-Controller](#the-xbox-controller)
-   [Verwenden von xinput](#using-xinput)
    -   [Mehrere Controller](#multiple-controllers)
    -   [Erhalten des Controller Zustands](#getting-controller-state)
    -   [Unzustellbare Zone](#dead-zone)
    -   [Festlegen von Vibrations Effekten](#setting-vibration-effects)
    -   [Erhalten von audiogerätebezeichgern](#getting-audio-device-identifiers)
    -   [Erhalten von DirectSound-GUIDs (nur Legacy-DirectX SDK)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-xinput"></a>Einführung in xinput

Die Xbox-Konsole verwendet einen Spiele Controller, der mit Windows kompatibel ist. Anwendungen können die xinput-API für die Kommunikation mit diesen Controllern verwenden, wenn Sie an einem Windows-PC angeschlossen sind (bis zu vier eindeutige Controller können gleichzeitig eingebunden werden).

Mit dieser API können alle verbundenen Xbox-Controller für den Status abgefragt werden, und es können Vibrationseffekte festgelegt werden. Controller, denen das-Headset zugeordnet ist, können auch auf Audioeingabe-und Ausgabegeräte abgefragt werden, die mit dem Headset für die Sprachverarbeitung verwendet werden können.

### <a name="the-xbox-controller"></a>Der Xbox-Controller

Der Xbox Controller verfügt über zwei analoge direktionale Stifte, von denen jeder über eine digitale Schaltfläche, zwei analoge Trigger, ein digitales direktionales Pad mit vier Richtungen und acht digitale Schaltflächen verfügt. Die Zustände der einzelnen Eingaben werden in der [**xinput- \_ Gamepad**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) -Struktur zurückgegeben, wenn die Funktion " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) " aufgerufen wird.

Der Controller verfügt auch über zwei Vibrationsmotoren, um dem Benutzer Force-Feedback Effekte bereitzustellen. Die Geschwindigkeiten dieser Motoren werden in der [**xinput- \_ Vibrations**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) Struktur angegeben, die an die Funktion " [**xinputsetstate**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) " übertragen wird, um Schwingungs Effekte festzulegen.

Optional kann ein Headset mit dem Controller verbunden werden. Das Headset verfügt über ein Mikrofon für die Spracheingabe und ein Telefon für die Audioausgabe. Sie können die Funktion " [**xinputgetaudiode viceids**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) " oder "Legacy [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) " aufrufen, um die Geräte Bezeichner zu erhalten, die den Geräten für das Mikrofon und das Telefon entsprechen. Sie können dann die [kernaudio-APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) verwenden, um Spracheingaben zu empfangen und Audioausgaben zu senden.

## <a name="using-xinput"></a>Verwenden von xinput

Die Verwendung von xinput ist so einfach wie das Aufrufen der xinput-Funktionen nach Bedarf. Mithilfe der xinput-Funktionen können Sie den Controller Zustand abrufen, die Headset-audioids abrufen und die Auswirkungen des Controllers auf den Controller festlegen.

### <a name="multiple-controllers"></a>Mehrere Controller

Die xinput-API unterstützt bis zu vier Controller, die zu einem beliebigen Zeitpunkt verbunden sind. Die xinput-Funktionen erfordern alle einen *dwuserindex* -Parameter, der übergeben wird, um den Controller zu identifizieren, der festgelegt oder abgefragt wird. Diese ID befindet sich im Bereich von 0-3 und wird automatisch von xinput festgelegt. Die Zahl entspricht dem Port, an dem der Controller angeschlossen ist, und kann nicht geändert werden.

Jeder Controller zeigt an, welche ID er verwendet, indem er einen Quadranten in der Mitte des Controllers in der Mitte des Controllers beleuchtet. Der *dwuserindex* -Wert 0 entspricht dem oberen linken Quadranten. die Nummerierung wird im Uhrzeigersinn um den Ring fortgesetzt.

Anwendungen sollten mehrere Controller unterstützen.

### <a name="getting-controller-state"></a>Erhalten des Controller Zustands

Während der gesamten Dauer einer Anwendung wird das erhalten des Zustands von einem Controller wahrscheinlich am häufigsten durchgeführt. Von Frame zu Frame in einer Spiel Anwendung sollte State abgerufen werden, und die Spielinformationen werden aktualisiert, um die Controller Änderungen widerzuspiegeln.

Verwenden Sie zum Abrufen des Zustands die Funktion " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) ":

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

Beachten Sie, dass der Rückgabewert von " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) " verwendet werden kann, um zu bestimmen, ob der Controller verbunden ist. Anwendungen sollten eine Struktur zum Speichern interner Controller Informationen definieren. Diese Informationen sollten mit den Ergebnissen von " **xinputgetstate** " verglichen werden, um zu bestimmen, welche Änderungen, wie z. b. Schaltflächen-oder analoge Controller Delta, zu diesem Frame gemacht wurden. Im obigen Beispiel stellt *g \_ Controller* eine solche Struktur dar.

Nachdem der Zustand in einer [**xinput- \_ Zustands**](/windows/desktop/api/XInput/ns-xinput-xinput_state) Struktur abgerufen wurde, können Sie ihn auf Änderungen überprüfen und bestimmte Informationen zum Controller Status abrufen.

Der *dwpacketnumber* -Member der [**xinput- \_ Status**](/windows/desktop/api/XInput/ns-xinput-xinput_state) Struktur kann verwendet werden, um zu überprüfen, ob sich der Zustand des Controllers seit dem letzten Aufrufen von " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)" geändert hat. Wenn *dwpacketnumber* sich nicht zwischen zwei sequenziellen Aufrufen von " **xinputgetstate**" ändert, hat sich der Status nicht geändert. Wenn Sie sich unterscheidet, sollte die Anwendung den *Gamepad* -Member der **xinput \_** -Struktur überprüfen, um ausführlichere Zustandsinformationen zu erhalten.

Aus Leistungsgründen wird " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) " nicht für einen "leeren" Benutzer Slot jeden Frame aufgerufen. Es wird empfohlen, dass Sie stattdessen alle paar Sekunden Überprüfungen auf neue Controller durchführen.

### <a name="dead-zone"></a>Unzustellbare Zone

Damit Benutzer ein konsistentes Spielverhalten haben, muss Ihr Spiel die Zone "Dead Zone" ordnungsgemäß implementieren. Die unzustellbare Zone ist "Verschiebungs Werte", die vom Controller gemeldet werden, auch wenn die analogen Fingerabdrücke unverändert und zentriert sind. Es gibt auch eine unzustellbare Zone für die 2 analogen Trigger.

> [!Note]  
> Spiele, die xinput verwenden, bei denen keine unzustellbare Zone überhaupt gefiltert wird, haben ein schlechtes Spiel. Beachten Sie, dass einige Controller sensibler als andere Controller sind. Daher kann die unzustellbare Zone von Unit zu Unit abweichen. Es wird empfohlen, dass Sie Ihre Spiele mit mehreren Xbox-Controllern auf verschiedenen Systemen testen.

Anwendungen sollten "unzustellbare Zonen" für analoge Eingaben (Trigger, Stöcke) verwenden, um anzugeben, wann eine Bewegung ausreichend auf dem Stick oder Trigger erstellt wurde, um als gültig betrachtet zu werden.

Die Anwendung sollte auf unzustellbare Zonen prüfen und appopriately Antworten, wie in diesem Beispiel:

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

In diesem Beispiel wird der Richtungsvektor des Controllers und die Länge des Vektors, mit dem der Controller gepusht wurde, berechnet. Dies ermöglicht die Erzwingung einer zirkulären deadzone, indem überprüft wird, ob die Größe des Controllers größer als der deadzonenwert ist. Außerdem normalisiert der Code die Größe des Controllers, der dann mit einem spielspezifischen Faktor multipliziert werden kann, um die Position des Controllers in die für das Spiel relevanten Einheiten zu konvertieren.

Beachten Sie, dass Sie für die Sticks und Trigger (von 0-65534) eigene unzustellbare Zonen definieren können. Sie können aber auch die bereitgestellten deadzones verwenden, die als xinput- \_ Gamepad-" \_ left \_ Thumb \_ deadzone", "xinput \_ Gamepad \_ right \_ Thumb \_ deadzone" und "xinput \_ Gamepad \_ Trigger \_ Threshold" in xinput. h definiert sind:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Nachdem die deadzone erzwungen wurde, ist es möglicherweise hilfreich, den resultierenden Bereich \[ 0,0.. 1.0 \] (wie im obigen Beispiel) zu skalieren und optional eine nichtlineare Transformation anzuwenden.

Beispielsweise kann es beim Spielen von spielen hilfreich sein, das Ergebnis zu verziften, um ein besseres Gefühl für den Einsatz der Autos mit einem Gamepad zu bieten. das Ergebnis bietet Ihnen mehr Genauigkeit in den unteren Bereichen, was wünschenswert ist, da Spieler in der Regel eine weiche Kraft anwenden, um eine feine Bewegung zu erzielen oder eine harte Kraft auf eine Richtung zu erhalten.

### <a name="setting-vibration-effects"></a>Festlegen von Vibrations Effekten

Zusätzlich zum Status des Controllers können Sie auch Vibrations Daten an den Controller senden, um das Feedback für den Benutzer des Controllers zu ändern. Der Controller enthält zwei rauschende Motoren, die unabhängig voneinander gesteuert werden können, indem Werte an die Funktion " [**xinputsetstate**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) " übergeben werden.

Die Geschwindigkeit der einzelnen Fahrzeuge kann mithilfe eines Wort Werts in der [**xinput- \_ Vibrations**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) Struktur angegeben werden, die wie folgt an die Funktion " [**xinputsetstate**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) " übermittelt wird:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Beachten Sie, dass es sich bei dem richtigen Motor um den Hochleistungs-Motor handelt, der linke Motor ist der niedrige Häufigkeits Motor. Sie müssen nicht immer auf denselben Betrag festgelegt werden, da Sie unterschiedliche Effekte bieten.

### <a name="getting-audio-device-identifiers"></a>Erhalten von audiogerätebezeichgern

Das Headset für einen Xbox-Controller verfügt über folgende Funktionen:

-   Sound mithilfe eines Mikrofons aufzeichnen
-   Wiedergabe von Sound mit einem Telefon

Verwenden Sie diesen Code zum Abrufen der Geräte Bezeichner für das Headset:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Nachdem Sie die Geräte Bezeichner abgerufen haben, können Sie die entsprechenden Schnittstellen erstellen. Wenn Sie z. b. xaudio2,8 verwenden, verwenden Sie diesen Code, um eine Mastering-Stimme für dieses Gerät zu erstellen:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Informationen zur Verwendung des captureid-Geräte Bezeichners finden Sie unter [Erfassen eines Streams](/windows/desktop/CoreAudio/capturing-a-stream).

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Erhalten von DirectSound-GUIDs (nur Legacy-DirectX SDK)

Das Headset, das mit einem Xbox-Controller verbunden werden kann, verfügt über zwei Funktionen: er kann Sound mithilfe eines Mikrofons aufzeichnen und Sound mit einem Telefon abspielen. In der xinput-API werden diese Funktionen mithilfe von [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))mithilfe der **IDirectSound8** -und **IDirectSoundCapture8** -Schnittstellen erreicht.

Um dem Headset-Mikrofon und dem Telefon den entsprechenden [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) -Schnittstellen zuzuordnen, müssen Sie die directsoundguids für die Erfassungs-und Rendering-Geräte abrufen, indem Sie " [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids)" aufrufen.

> [!Note]  
> Die Verwendung des Legacy- [directsounds](/previous-versions/windows/desktop/ee416960(v=vs.85)) wird nicht empfohlen und ist in Windows Store-Apps nicht verfügbar. Die Informationen in diesem Abschnitt gelten nur für die DirectX SDK-Version von xinput (xinput 1,3). Die Windows 8-Version von xinput (xinput 1,4) verwendet exklusiv die von " [**xinputgetaudiodeviceids**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)" erhaltenen Geräte Bezeichner der Windows-audiositzungsapi (WASAPI).

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