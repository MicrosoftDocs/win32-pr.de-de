---
description: Die terminalklassenguids identifizieren ein bestimmtes Terminal durch Funktionen.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Terminal Klasse (Tapi3if. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d67d7668f9e4e16ad357408c8e9087fce870a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354742"
---
# <a name="terminal-class"></a>Terminal Klasse

Die terminalklassenguids identifizieren ein bestimmtes Terminal durch Funktionen.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**CLSID \_ fileplaybackterminal**
</dt> <dd> <dl> <dt>



Terminal für die Dateiwiedergabe.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**CLSID \_ filerecordingterminal**
</dt> <dd> <dl> <dt>



Datei Aufzeichnungs Terminal.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**CLSID \_ filerecordingtrack**
</dt> <dd> <dl> <dt>



Datei Aufzeichnungs Track.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**CLSID- \_ handsetterminal**
</dt> <dd> <dl> <dt>



Telefonnummer.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**CLSID- \_ headsetterminal**
</dt> <dd> <dl> <dt>



Kopfsatz.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ mediastreamterminal**
</dt> <dd> <dl> <dt>



Medienstrom Terminal, dynamisch erstellt.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**CLSID- \_ mikrophoneterminal**
</dt> <dd> <dl> <dt>



Tritt.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**CLSID \_ speakerphoneterminal**
</dt> <dd> <dl> <dt>



Redner Telefon.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**CLSID- \_ speakersterminal**
</dt> <dd> <dl> <dt>



Refer.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ videoinputterminal**
</dt> <dd> <dl> <dt>



Video Eingabe Terminal.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**CLSID \_ videowindowterm**
</dt> <dd> <dl> <dt>



Video Anzeige Fenster, dynamisch erstellt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **BSTR** -Version der Terminal Klassen ist hauptsächlich für die Verwendung von Visual Basic Anwendungen vorgesehen. (Sie werden z. b. als Elemente der Auflistung zurückgegeben, die mit [**get \_ dynamicterminalclasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)abgerufen werden.)

-   BSTR-CLSID- \_ Zeichenfolge \_ handsetterminal
-   BSTR CLSID- \_ Zeichenfolge \_ headsetterminal
-   BSTR CLSID- \_ Zeichenfolge \_ mediastreamterminal
-   BSTR CLSID- \_ Zeichenfolge " \_ mikrophoneterminal"
-   BSTR CLSID- \_ Zeichenfolge \_ speakerphoneterminal
-   BSTR CLSID- \_ Zeichenfolge \_ speakersterminal
-   BSTR-CLSID- \_ Zeichenfolge \_ videoinputterminal
-   BSTR-CLSID- \_ Zeichenfolge \_ videowindowterm

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Tapi3if. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itterminalsupport:: "kreateterminal"**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**Itterminal:: get \_ terminalclass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**Itterminalmanager:: kreatedynamicterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**Itterminalmanager:: getdynamicterminalclasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**Itterminalsupport:: enumeratedynamicterminalclasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

