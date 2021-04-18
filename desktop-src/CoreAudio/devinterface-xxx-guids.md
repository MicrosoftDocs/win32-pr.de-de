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
# <a name="devinterface_xxx-guids"></a>Devinterface \_ xxx-GUIDs

Die devinterface \_ xxx-GUIDs werden verwendet, um die GUIDs für Geräteschnittstellen darzustellen.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**devinterface \_ - \_ Audioerfassung**
</dt> <dd> <dl> <dt>



Gibt die Abfrage Zeichenfolge an, mit der alle audioerfassungs Geräte im System aufgelistet werden. Dieser Wert wird von [**mediadevice:: getaudiocaptureselector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)zurückgegeben.

Wenn Sie diesen Wert an [**activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) übergeben, wird die angeforderte Schnittstelle auf dem standardmäßigen audioerfassungs Gerät aktiviert.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**devinterface \_ - \_ audiorendering**
</dt> <dd> <dl> <dt>



Gibt die Abfrage Zeichenfolge an, mit der alle audiorendering-Geräte auf dem System aufgelistet werden. Dieser Wert wird von [**mediadevice:: getaudiorenderselector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)zurückgegeben.

Wenn Sie diesen Wert an [**activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) übergeben, wird die angeforderte Schnittstelle auf dem standardaudiorendering-Gerät aktiviert.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**devinterface- \_ MIDI- \_ Eingabe**
</dt> <dd> <dl> <dt>



Gibt die Abfrage Zeichenfolge an, die verwendet wird, um alle [**MIDIINPORT**](/uwp/api/Windows.Devices.Midi.MidiInPort) -Objekte im System aufzuzählen. Dieser Wert wird von [**MIDIINPORT:: getdeviceselector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**Ausgabe von devinterface- \_ MIDI \_**
</dt> <dd> <dl> <dt>



Gibt die Abfrage Zeichenfolge an, die verwendet wird, um alle [**midioutport**](/uwp/api/Windows.Devices.Midi.MidiOutPort) -Objekte im System aufzuzählen. Dieser Wert wird von [**midioutport:: getdeviceselector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)zurückgegeben.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



 

