---
description: Die DEVINTERFACE \_ XXX-GUIDs werden verwendet, um die GUIDs für Geräteschnittstellen zu darstellen.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: DEVINTERFACE_XXX GUIDs (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cef6a105ed8e34519a2ca0a06d9d4f43a7aa91495fae9f54eedfa44d79b043c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406793"
---
# <a name="devinterface_xxx-guids"></a>DEVINTERFACE \_ XXX-GUIDs

Die DEVINTERFACE \_ XXX-GUIDs werden verwendet, um die GUIDs für Geräteschnittstellen zu darstellen.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_DEVINTERFACE-AUDIOAUFNAHME \_**
</dt> <dd> <dl> <dt>



Gibt die Abfragezeichenfolge an, die zum Aufzählen aller Audioaufnahmegeräte im System verwendet wird. Dieser Wert wird von [**MediaDevice::GetAudioCaptureSelector zurückgegeben.**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)

Wenn Sie diesen Wert an [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) übergeben, wird die angeforderte Schnittstelle auf dem Standardgerät für die Audioaufnahme aktiviert.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE \_ AUDIO \_ RENDER**
</dt> <dd> <dl> <dt>



Gibt die Abfragezeichenfolge an, die zum Aufzählen aller Audiorenderinggeräte im System verwendet wird. Dieser Wert wird von [**MediaDevice::GetAudioRenderSelector zurückgegeben.**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)

Durch Übergeben dieses Werts [**an ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) wird die angeforderte Schnittstelle auf dem Standardaudiorendergerät aktiviert.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_DEVINTERFACE-EINGANGSEINGABE \_**
</dt> <dd> <dl> <dt>



Gibt die Abfragezeichenfolge an, die zum Aufzählen [**allerPort-Objekte**](/uwp/api/Windows.Devices.Midi.MidiInPort) im System verwendet wird. Dieser Wert wird von [**EinerPort::GetDeviceSelector zurückgegeben.**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_DEVINTERFACE-AUSGABE \_**
</dt> <dd> <dl> <dt>



Gibt die Abfragezeichenfolge an, die zum Aufzählen aller [**AttributoutPort-Objekte**](/uwp/api/Windows.Devices.Midi.MidiOutPort) im System verwendet wird. Dieser Wert wird von [**Einerport::GetDeviceSelector zurückgegeben.**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



 

