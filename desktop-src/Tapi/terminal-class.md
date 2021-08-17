---
description: Die Terminalklassen-GUIDs identifizieren ein bestimmtes Terminal nach Funktionen.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Terminal-Klasse (Tapi3if.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd20d3e540529b343d1fb848b9e8cb2579a621b40146e0d170fdb175c4c9a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975450"
---
# <a name="terminal-class"></a>Terminal-Klasse

Die Terminalklassen-GUIDs identifizieren ein bestimmtes Terminal nach Funktionen.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**CLSID \_ FilePlaybackTerminal**
</dt> <dd> <dl> <dt>



Terminal für die Dateiwiedergabe.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**CLSID \_ FileRecordingTerminal**
</dt> <dd> <dl> <dt>



Dateiaufzeichnungsterminal.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**CLSID \_ FileRecordingTrack**
</dt> <dd> <dl> <dt>



Dateiaufzeichnungsspur.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**CLSID \_ HandsetTerminal**
</dt> <dd> <dl> <dt>



Telefonhandset.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**CLSID \_ HeadsetTerminal**
</dt> <dd> <dl> <dt>



Kopfsatz.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ MediaStreamTerminal**
</dt> <dd> <dl> <dt>



Medienstreamterminal, dynamisch erstellt.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**CLSID \_ MicrophoneTerminal**
</dt> <dd> <dl> <dt>



Mikrofon.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**CLSID \_ SpeakerphoneTerminal**
</dt> <dd> <dl> <dt>



Telefon des Sprechers.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**CLSID \_ SpeakersTerminal**
</dt> <dd> <dl> <dt>



Lautsprecher.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ VideoInputTerminal**
</dt> <dd> <dl> <dt>



Videoeingabeterminal.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**CLSID \_ VideoWindowTerm**
</dt> <dd> <dl> <dt>



Videoanzeigefenster, dynamisch erstellt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die **BSTR-Version** der Terminalklassen ist hauptsächlich für die Verwendung von Visual Basic vorgesehen. (Sie werden z. B. als die Elemente der Auflistung zurückgegeben, die mit [**get \_ DynamicTerminalClasses erhalten wurden.)**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)

-   BSTR CLSID \_ String \_ HandsetTerminal
-   BSTR CLSID \_ String \_ HeadsetTerminal
-   BSTR CLSID \_ String \_ MediaStreamTerminal
-   BSTR CLSID \_ String \_ MicrophoneTerminal
-   BSTR CLSID \_ String \_ SpeakerphoneTerminal
-   BSTR CLSID \_ String \_ SpeakersTerminal
-   BSTR CLSID \_ String \_ VideoInputTerminal
-   BSTR CLSID \_ String \_ VideoWindowTerm

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Tapi3if.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

