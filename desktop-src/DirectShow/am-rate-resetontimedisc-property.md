---
description: 'AM_RATE_ResetOnTimeDisc-Eigenschaft: Gilt für Windows Vista und höher.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42b8e9d158f644d9e630555d96bf4d06e4ea9ef3cddced67742c057d0ab3859
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079520"
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



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft unterstützt Smooth Rate-Änderungen. Wenn der Wert dieser Eigenschaft **TRUE** ist und der Decoder ein Eingabebeispiel mit dem AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flag empfängt, sollte der decodierte Frame den gleichen Zeitstempel wie der Eingaberahmen haben.

Rufen Sie zum Abrufen des AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flags im Beispiel [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) auf. Das Flag wird im **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) festgelegt.

Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




