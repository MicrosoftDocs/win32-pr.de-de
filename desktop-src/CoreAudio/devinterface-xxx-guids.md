---
description: Die devinterface \_ xxx-GUIDs werden verwendet, um die GUIDs für Geräteschnittstellen darzustellen.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: DEVINTERFACE_XXX GUIDs (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365520"
---
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="3320f-103">Devinterface \_ xxx-GUIDs</span><span class="sxs-lookup"><span data-stu-id="3320f-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="3320f-104">Die devinterface \_ xxx-GUIDs werden verwendet, um die GUIDs für Geräteschnittstellen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="3320f-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="3320f-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**devinterface \_ - \_ Audioerfassung**</span><span class="sxs-lookup"><span data-stu-id="3320f-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3320f-106">Gibt die Abfrage Zeichenfolge an, mit der alle audioerfassungs Geräte im System aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="3320f-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="3320f-107">Dieser Wert wird von [**mediadevice:: getaudiocaptureselector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3320f-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="3320f-108">Wenn Sie diesen Wert an [**activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) übergeben, wird die angeforderte Schnittstelle auf dem standardmäßigen audioerfassungs Gerät aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3320f-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3320f-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**devinterface \_ - \_ audiorendering**</span><span class="sxs-lookup"><span data-stu-id="3320f-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3320f-110">Gibt die Abfrage Zeichenfolge an, mit der alle audiorendering-Geräte auf dem System aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="3320f-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="3320f-111">Dieser Wert wird von [**mediadevice:: getaudiorenderselector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3320f-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="3320f-112">Wenn Sie diesen Wert an [**activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) übergeben, wird die angeforderte Schnittstelle auf dem standardaudiorendering-Gerät aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3320f-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3320f-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**devinterface- \_ MIDI- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="3320f-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3320f-114">Gibt die Abfrage Zeichenfolge an, die verwendet wird, um alle [**MIDIINPORT**](/uwp/api/Windows.Devices.Midi.MidiInPort) -Objekte im System aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="3320f-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="3320f-115">Dieser Wert wird von [**MIDIINPORT:: getdeviceselector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3320f-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3320f-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**Ausgabe von devinterface- \_ MIDI \_**</span><span class="sxs-lookup"><span data-stu-id="3320f-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3320f-117">Gibt die Abfrage Zeichenfolge an, die verwendet wird, um alle [**midioutport**](/uwp/api/Windows.Devices.Midi.MidiOutPort) -Objekte im System aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="3320f-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="3320f-118">Dieser Wert wird von [**midioutport:: getdeviceselector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3320f-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3320f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3320f-119">Requirements</span></span>



| <span data-ttu-id="3320f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3320f-120">Requirement</span></span> | <span data-ttu-id="3320f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3320f-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3320f-122">Header</span><span class="sxs-lookup"><span data-stu-id="3320f-122">Header</span></span><br/> | <dl> <span data-ttu-id="3320f-123"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3320f-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 

