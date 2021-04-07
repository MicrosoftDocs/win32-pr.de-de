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
# <a name="getting-started-with-xinput"></a><span data-ttu-id="525be-104">Einstieg in xinput</span><span class="sxs-lookup"><span data-stu-id="525be-104">Getting Started With XInput</span></span>

<span data-ttu-id="525be-105">Xinput ist eine API, mit der Anwendungen Eingaben vom Xbox-Controller für Windows empfangen können.</span><span class="sxs-lookup"><span data-stu-id="525be-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="525be-106">Die Auswirkungen des Controllers und die Spracheingabe und-Ausgabe werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="525be-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="525be-107">Dieses Thema enthält eine kurze Übersicht über die Funktionen von XInput und deren Einrichtung in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="525be-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="525be-108">Dies umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="525be-108">It includes the following:</span></span>

-   [<span data-ttu-id="525be-109">Einführung in xinput</span><span class="sxs-lookup"><span data-stu-id="525be-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="525be-110">Der Xbox-Controller</span><span class="sxs-lookup"><span data-stu-id="525be-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="525be-111">Verwenden von xinput</span><span class="sxs-lookup"><span data-stu-id="525be-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="525be-112">Mehrere Controller</span><span class="sxs-lookup"><span data-stu-id="525be-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="525be-113">Erhalten des Controller Zustands</span><span class="sxs-lookup"><span data-stu-id="525be-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="525be-114">Unzustellbare Zone</span><span class="sxs-lookup"><span data-stu-id="525be-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="525be-115">Festlegen von Vibrations Effekten</span><span class="sxs-lookup"><span data-stu-id="525be-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="525be-116">Erhalten von audiogerätebezeichgern</span><span class="sxs-lookup"><span data-stu-id="525be-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="525be-117">Erhalten von DirectSound-GUIDs (nur Legacy-DirectX SDK)</span><span class="sxs-lookup"><span data-stu-id="525be-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="525be-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="525be-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="525be-119">Einführung in xinput</span><span class="sxs-lookup"><span data-stu-id="525be-119">Introduction to XInput</span></span>

<span data-ttu-id="525be-120">Die Xbox-Konsole verwendet einen Spiele Controller, der mit Windows kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="525be-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="525be-121">Anwendungen können die xinput-API für die Kommunikation mit diesen Controllern verwenden, wenn Sie an einem Windows-PC angeschlossen sind (bis zu vier eindeutige Controller können gleichzeitig eingebunden werden).</span><span class="sxs-lookup"><span data-stu-id="525be-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="525be-122">Mit dieser API können alle verbundenen Xbox-Controller für den Status abgefragt werden, und es können Vibrationseffekte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="525be-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="525be-123">Controller, denen das-Headset zugeordnet ist, können auch auf Audioeingabe-und Ausgabegeräte abgefragt werden, die mit dem Headset für die Sprachverarbeitung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="525be-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="525be-124">Der Xbox-Controller</span><span class="sxs-lookup"><span data-stu-id="525be-124">The Xbox Controller</span></span>

<span data-ttu-id="525be-125">Der Xbox Controller verfügt über zwei analoge direktionale Stifte, von denen jeder über eine digitale Schaltfläche, zwei analoge Trigger, ein digitales direktionales Pad mit vier Richtungen und acht digitale Schaltflächen verfügt.</span><span class="sxs-lookup"><span data-stu-id="525be-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="525be-126">Die Zustände der einzelnen Eingaben werden in der [**xinput- \_ Gamepad**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) -Struktur zurückgegeben, wenn die Funktion " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="525be-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="525be-127">Der Controller verfügt auch über zwei Vibrationsmotoren, um dem Benutzer Force-Feedback Effekte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="525be-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="525be-128">Die Geschwindigkeiten dieser Motoren werden in der [**xinput- \_ Vibrations**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) Struktur angegeben, die an die Funktion " [**xinputsetstate**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) " übertragen wird, um Schwingungs Effekte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="525be-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="525be-129">Optional kann ein Headset mit dem Controller verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="525be-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="525be-130">Das Headset verfügt über ein Mikrofon für die Spracheingabe und ein Telefon für die Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="525be-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="525be-131">Sie können die Funktion " [**xinputgetaudiode viceids**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) " oder "Legacy [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) " aufrufen, um die Geräte Bezeichner zu erhalten, die den Geräten für das Mikrofon und das Telefon entsprechen.</span><span class="sxs-lookup"><span data-stu-id="525be-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="525be-132">Sie können dann die [kernaudio-APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) verwenden, um Spracheingaben zu empfangen und Audioausgaben zu senden.</span><span class="sxs-lookup"><span data-stu-id="525be-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="525be-133">Verwenden von xinput</span><span class="sxs-lookup"><span data-stu-id="525be-133">Using XInput</span></span>

<span data-ttu-id="525be-134">Die Verwendung von xinput ist so einfach wie das Aufrufen der xinput-Funktionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="525be-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="525be-135">Mithilfe der xinput-Funktionen können Sie den Controller Zustand abrufen, die Headset-audioids abrufen und die Auswirkungen des Controllers auf den Controller festlegen.</span><span class="sxs-lookup"><span data-stu-id="525be-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="525be-136">Mehrere Controller</span><span class="sxs-lookup"><span data-stu-id="525be-136">Multiple Controllers</span></span>

<span data-ttu-id="525be-137">Die xinput-API unterstützt bis zu vier Controller, die zu einem beliebigen Zeitpunkt verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="525be-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="525be-138">Die xinput-Funktionen erfordern alle einen *dwuserindex* -Parameter, der übergeben wird, um den Controller zu identifizieren, der festgelegt oder abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="525be-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="525be-139">Diese ID befindet sich im Bereich von 0-3 und wird automatisch von xinput festgelegt.</span><span class="sxs-lookup"><span data-stu-id="525be-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="525be-140">Die Zahl entspricht dem Port, an dem der Controller angeschlossen ist, und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="525be-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="525be-141">Jeder Controller zeigt an, welche ID er verwendet, indem er einen Quadranten in der Mitte des Controllers in der Mitte des Controllers beleuchtet.</span><span class="sxs-lookup"><span data-stu-id="525be-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="525be-142">Der *dwuserindex* -Wert 0 entspricht dem oberen linken Quadranten. die Nummerierung wird im Uhrzeigersinn um den Ring fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="525be-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="525be-143">Anwendungen sollten mehrere Controller unterstützen.</span><span class="sxs-lookup"><span data-stu-id="525be-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="525be-144">Erhalten des Controller Zustands</span><span class="sxs-lookup"><span data-stu-id="525be-144">Getting Controller State</span></span>

<span data-ttu-id="525be-145">Während der gesamten Dauer einer Anwendung wird das erhalten des Zustands von einem Controller wahrscheinlich am häufigsten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="525be-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="525be-146">Von Frame zu Frame in einer Spiel Anwendung sollte State abgerufen werden, und die Spielinformationen werden aktualisiert, um die Controller Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="525be-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="525be-147">Verwenden Sie zum Abrufen des Zustands die Funktion " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) ":</span><span class="sxs-lookup"><span data-stu-id="525be-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

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

<span data-ttu-id="525be-148">Beachten Sie, dass der Rückgabewert von " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) " verwendet werden kann, um zu bestimmen, ob der Controller verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="525be-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="525be-149">Anwendungen sollten eine Struktur zum Speichern interner Controller Informationen definieren. Diese Informationen sollten mit den Ergebnissen von " **xinputgetstate** " verglichen werden, um zu bestimmen, welche Änderungen, wie z. b. Schaltflächen-oder analoge Controller Delta, zu diesem Frame gemacht wurden.</span><span class="sxs-lookup"><span data-stu-id="525be-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="525be-150">Im obigen Beispiel stellt *g \_ Controller* eine solche Struktur dar.</span><span class="sxs-lookup"><span data-stu-id="525be-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="525be-151">Nachdem der Zustand in einer [**xinput- \_ Zustands**](/windows/desktop/api/XInput/ns-xinput-xinput_state) Struktur abgerufen wurde, können Sie ihn auf Änderungen überprüfen und bestimmte Informationen zum Controller Status abrufen.</span><span class="sxs-lookup"><span data-stu-id="525be-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="525be-152">Der *dwpacketnumber* -Member der [**xinput- \_ Status**](/windows/desktop/api/XInput/ns-xinput-xinput_state) Struktur kann verwendet werden, um zu überprüfen, ob sich der Zustand des Controllers seit dem letzten Aufrufen von " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)" geändert hat.</span><span class="sxs-lookup"><span data-stu-id="525be-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="525be-153">Wenn *dwpacketnumber* sich nicht zwischen zwei sequenziellen Aufrufen von " **xinputgetstate**" ändert, hat sich der Status nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="525be-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="525be-154">Wenn Sie sich unterscheidet, sollte die Anwendung den *Gamepad* -Member der **xinput \_** -Struktur überprüfen, um ausführlichere Zustandsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="525be-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="525be-155">Aus Leistungsgründen wird " [**xinputgetstate**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) " nicht für einen "leeren" Benutzer Slot jeden Frame aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="525be-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="525be-156">Es wird empfohlen, dass Sie stattdessen alle paar Sekunden Überprüfungen auf neue Controller durchführen.</span><span class="sxs-lookup"><span data-stu-id="525be-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="525be-157">Unzustellbare Zone</span><span class="sxs-lookup"><span data-stu-id="525be-157">Dead Zone</span></span>

<span data-ttu-id="525be-158">Damit Benutzer ein konsistentes Spielverhalten haben, muss Ihr Spiel die Zone "Dead Zone" ordnungsgemäß implementieren.</span><span class="sxs-lookup"><span data-stu-id="525be-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="525be-159">Die unzustellbare Zone ist "Verschiebungs Werte", die vom Controller gemeldet werden, auch wenn die analogen Fingerabdrücke unverändert und zentriert sind.</span><span class="sxs-lookup"><span data-stu-id="525be-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="525be-160">Es gibt auch eine unzustellbare Zone für die 2 analogen Trigger.</span><span class="sxs-lookup"><span data-stu-id="525be-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="525be-161">Spiele, die xinput verwenden, bei denen keine unzustellbare Zone überhaupt gefiltert wird, haben ein schlechtes Spiel.</span><span class="sxs-lookup"><span data-stu-id="525be-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="525be-162">Beachten Sie, dass einige Controller sensibler als andere Controller sind. Daher kann die unzustellbare Zone von Unit zu Unit abweichen.</span><span class="sxs-lookup"><span data-stu-id="525be-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="525be-163">Es wird empfohlen, dass Sie Ihre Spiele mit mehreren Xbox-Controllern auf verschiedenen Systemen testen.</span><span class="sxs-lookup"><span data-stu-id="525be-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="525be-164">Anwendungen sollten "unzustellbare Zonen" für analoge Eingaben (Trigger, Stöcke) verwenden, um anzugeben, wann eine Bewegung ausreichend auf dem Stick oder Trigger erstellt wurde, um als gültig betrachtet zu werden.</span><span class="sxs-lookup"><span data-stu-id="525be-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="525be-165">Die Anwendung sollte auf unzustellbare Zonen prüfen und appopriately Antworten, wie in diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="525be-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

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

<span data-ttu-id="525be-166">In diesem Beispiel wird der Richtungsvektor des Controllers und die Länge des Vektors, mit dem der Controller gepusht wurde, berechnet.</span><span class="sxs-lookup"><span data-stu-id="525be-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="525be-167">Dies ermöglicht die Erzwingung einer zirkulären deadzone, indem überprüft wird, ob die Größe des Controllers größer als der deadzonenwert ist.</span><span class="sxs-lookup"><span data-stu-id="525be-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="525be-168">Außerdem normalisiert der Code die Größe des Controllers, der dann mit einem spielspezifischen Faktor multipliziert werden kann, um die Position des Controllers in die für das Spiel relevanten Einheiten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="525be-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="525be-169">Beachten Sie, dass Sie für die Sticks und Trigger (von 0-65534) eigene unzustellbare Zonen definieren können. Sie können aber auch die bereitgestellten deadzones verwenden, die als xinput- \_ Gamepad-" \_ left \_ Thumb \_ deadzone", "xinput \_ Gamepad \_ right \_ Thumb \_ deadzone" und "xinput \_ Gamepad \_ Trigger \_ Threshold" in xinput. h definiert sind:</span><span class="sxs-lookup"><span data-stu-id="525be-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="525be-170">Nachdem die deadzone erzwungen wurde, ist es möglicherweise hilfreich, den resultierenden Bereich \[ 0,0.. 1.0 \] (wie im obigen Beispiel) zu skalieren und optional eine nichtlineare Transformation anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="525be-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="525be-171">Beispielsweise kann es beim Spielen von spielen hilfreich sein, das Ergebnis zu verziften, um ein besseres Gefühl für den Einsatz der Autos mit einem Gamepad zu bieten. das Ergebnis bietet Ihnen mehr Genauigkeit in den unteren Bereichen, was wünschenswert ist, da Spieler in der Regel eine weiche Kraft anwenden, um eine feine Bewegung zu erzielen oder eine harte Kraft auf eine Richtung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="525be-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="525be-172">Festlegen von Vibrations Effekten</span><span class="sxs-lookup"><span data-stu-id="525be-172">Setting Vibration Effects</span></span>

<span data-ttu-id="525be-173">Zusätzlich zum Status des Controllers können Sie auch Vibrations Daten an den Controller senden, um das Feedback für den Benutzer des Controllers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="525be-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="525be-174">Der Controller enthält zwei rauschende Motoren, die unabhängig voneinander gesteuert werden können, indem Werte an die Funktion " [**xinputsetstate**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="525be-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="525be-175">Die Geschwindigkeit der einzelnen Fahrzeuge kann mithilfe eines Wort Werts in der [**xinput- \_ Vibrations**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) Struktur angegeben werden, die wie folgt an die Funktion " [**xinputsetstate**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) " übermittelt wird:</span><span class="sxs-lookup"><span data-stu-id="525be-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="525be-176">Beachten Sie, dass es sich bei dem richtigen Motor um den Hochleistungs-Motor handelt, der linke Motor ist der niedrige Häufigkeits Motor.</span><span class="sxs-lookup"><span data-stu-id="525be-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="525be-177">Sie müssen nicht immer auf denselben Betrag festgelegt werden, da Sie unterschiedliche Effekte bieten.</span><span class="sxs-lookup"><span data-stu-id="525be-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="525be-178">Erhalten von audiogerätebezeichgern</span><span class="sxs-lookup"><span data-stu-id="525be-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="525be-179">Das Headset für einen Xbox-Controller verfügt über folgende Funktionen:</span><span class="sxs-lookup"><span data-stu-id="525be-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="525be-180">Sound mithilfe eines Mikrofons aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="525be-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="525be-181">Wiedergabe von Sound mit einem Telefon</span><span class="sxs-lookup"><span data-stu-id="525be-181">Play back sound using a headphone</span></span>

<span data-ttu-id="525be-182">Verwenden Sie diesen Code zum Abrufen der Geräte Bezeichner für das Headset:</span><span class="sxs-lookup"><span data-stu-id="525be-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="525be-183">Nachdem Sie die Geräte Bezeichner abgerufen haben, können Sie die entsprechenden Schnittstellen erstellen.</span><span class="sxs-lookup"><span data-stu-id="525be-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="525be-184">Wenn Sie z. b. xaudio2,8 verwenden, verwenden Sie diesen Code, um eine Mastering-Stimme für dieses Gerät zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="525be-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="525be-185">Informationen zur Verwendung des captureid-Geräte Bezeichners finden Sie unter [Erfassen eines Streams](/windows/desktop/CoreAudio/capturing-a-stream).</span><span class="sxs-lookup"><span data-stu-id="525be-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="525be-186">Erhalten von DirectSound-GUIDs (nur Legacy-DirectX SDK)</span><span class="sxs-lookup"><span data-stu-id="525be-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="525be-187">Das Headset, das mit einem Xbox-Controller verbunden werden kann, verfügt über zwei Funktionen: er kann Sound mithilfe eines Mikrofons aufzeichnen und Sound mit einem Telefon abspielen.</span><span class="sxs-lookup"><span data-stu-id="525be-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="525be-188">In der xinput-API werden diese Funktionen mithilfe von [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))mithilfe der **IDirectSound8** -und **IDirectSoundCapture8** -Schnittstellen erreicht.</span><span class="sxs-lookup"><span data-stu-id="525be-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="525be-189">Um dem Headset-Mikrofon und dem Telefon den entsprechenden [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) -Schnittstellen zuzuordnen, müssen Sie die directsoundguids für die Erfassungs-und Rendering-Geräte abrufen, indem Sie " [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="525be-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="525be-190">Die Verwendung des Legacy- [directsounds](/previous-versions/windows/desktop/ee416960(v=vs.85)) wird nicht empfohlen und ist in Windows Store-Apps nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="525be-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="525be-191">Die Informationen in diesem Abschnitt gelten nur für die DirectX SDK-Version von xinput (xinput 1,3).</span><span class="sxs-lookup"><span data-stu-id="525be-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="525be-192">Die Windows 8-Version von xinput (xinput 1,4) verwendet exklusiv die von " [**xinputgetaudiodeviceids**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)" erhaltenen Geräte Bezeichner der Windows-audiositzungsapi (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="525be-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="525be-193">Nachdem Sie die GUIDs abgerufen haben, können Sie die entsprechenden Schnittstellen erstellen, indem Sie DirectSoundCreate8 und DirectSoundCaptureCreate8 wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="525be-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="525be-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="525be-194">Related topics</span></span>

[<span data-ttu-id="525be-195">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="525be-195">Programming Reference</span></span>](programming-reference.md)