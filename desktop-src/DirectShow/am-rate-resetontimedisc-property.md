---
description: 'AM_RATE_ResetOnTimeDisc-Eigenschaft: Gilt für Windows Vista und höher.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096608"
---
# <a name="am_rate_resetontimedisc-property"></a>AM \_ RATE \_ ResetOnTimeDisc-Eigenschaft

Gilt für Windows Vista und höher.

Diese Eigenschaft fragt ab, ob der Decoder die Ausgabezeitstempel mit den Eingabezeitstempeln neu synchronisiert, wenn der Decoder eine Stichprobe mit dem Diskontinuitätsflag empfängt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |
| Eigenschafts-ID       | AM \_ RATE \_ ResetOnTimeDisc     |
| Datentyp         | **DWORD**                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft unterstützt Smooth Rate-Änderungen. Wenn der Wert dieser Eigenschaft **TRUE** ist und der Decoder ein Eingabebeispiel mit dem AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flag empfängt, sollte der decodierte Frame den gleichen Zeitstempel wie der Eingaberahmen haben.

Um das AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flag abzurufen, rufen [**Sie IMediaSample2::GetProperties im**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) Beispiel auf. Das Flag wird im **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) festgelegt.

Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




