---
description: XAudio2 spezifische Fehlercodes, die von XAudio2-Methoden zurückgegeben werden.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: XAudio2-Fehler Codes (XAudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373957"
---
# <a name="xaudio2-error-codes"></a>XAudio2-Fehler Codes

XAudio2 spezifische Fehlercodes, die von XAudio2-Methoden zurückgegeben werden.



| Konstante/Wert                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E \_ ungültiger- \_ Rückruf**</dt> <dt>0x88960001</dt> </dl>                          | Wird von XAudio2 für bestimmte API-Verwendungs Fehler (ungültige Aufrufe usw.) zurückgegeben, die nur schwer zu vermeiden sind und von einem Titel zur Laufzeit behandelt werden müssen. (API-Verwendungs Fehler, die vollständig vermeidbar sind, wie z. b. ungültige Parameter, verursachen eine Assert in Debugbuilds und undefiniertes Verhalten in Einzelhandels Builds, sodass kein Fehlercode für Sie definiert ist.)<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ E \_ XMA \_ - \_ Decoderfehler**</dt> <dt>0x88960002</dt> </dl>          | Nicht BEHEB barer Fehler bei der Xbox 360-XMA-Hardware.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ Fehler beim \_ \_ Erstellen von \_ E xapo**</dt> <dt>0x88960003</dt> . </dl> | Ein Effekt konnte nicht instanziiert werden.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ E \_ - \_ Gerät**</dt> hat <dt>0x88960004</dt> ungültig </dl>        | Ein Audiogerät kann nicht mehr verwendet werden, da es nicht mehr funktioniert oder ein anderes Ereignis ist<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Bemerkungen

### <a name="platform-requirements"></a>Plattformanforderungen

Windows 10 (xaudio2.9); Windows 8, Windows Phone 8 (xaudio2,8); DirectX SDK (xaudio2,7)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XAudio2:: Konstanten](constants.md)
</dt> </dl>

 

 




