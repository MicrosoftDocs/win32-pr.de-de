---
description: XAudio2-spezifische Fehlercodes, die von XAudio2-Methoden zurückgegeben werden.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: XAudio2-Fehlercodes (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbfb29153ca55064c1019e9cfb8fd1019caaa0ffe17dfa103f123faa812f762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545400"
---
# <a name="xaudio2-error-codes"></a>XAudio2-Fehlercodes

XAudio2-spezifische Fehlercodes, die von XAudio2-Methoden zurückgegeben werden.



| Konstante/Wert                                                                                                                                                                                                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E \_ \_ UNGÜLTIGE**</dt> <dt>0X88960001</dt> </dl>                          | Wird von XAudio2 für bestimmte API-Verwendungsfehler (ungültige Aufrufe und so weiter) zurückgegeben, die schwer vollständig zu vermeiden sind und zur Laufzeit von einem Titel behandelt werden sollten. (API-Verwendungsfehler, die vollständig vermeidbar sind, z. B. ungültige Parameter, verursachen eine ASSERT-Funktion in Debugbuilds und undefiniertes Verhalten in Einzelhandelsbuilds, sodass kein Fehlercode für sie definiert wird.)<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ E \_ XMA \_ DECODER ERROR \_ 0X88960002**</dt> <dt></dt> </dl>          | Bei Xbox 360 XMA-Hardware ist ein nicht behebbarer Fehler aufgetreten.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ FEHLER \_ BEI DER XAPO-0X88960003 \_ \_**</dt> <dt></dt> </dl> | Ein Effekt konnte nicht instanziiert werden.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ E \_ GERÄT \_ UNGÜLTIG 0X88960004**</dt> <dt></dt> </dl>        | Ein Audiogerät wurde unbrauchbar, da es aus dem Netz entfernt wurde oder ein anderes Ereignis auftauen kann.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Hinweise

### <a name="platform-requirements"></a>Plattformanforderungen

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Xaudio2.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XAudio2::Constants](constants.md)
</dt> </dl>

 

 




