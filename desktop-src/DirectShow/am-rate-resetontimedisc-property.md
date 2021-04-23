---
description: Gilt für Windows Vista und höher.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910248"
---
# <a name="am_rate_resetontimedisc-property"></a>AM \_ RATE \_ ResetOnTimeDisc-Eigenschaft

Gilt für Windows Vista und höher.

Diese Eigenschaft fragt ab, ob der Decoder die Ausgabezeitstempel erneut mit den Eingabezeitstempeln synchronisiert, wenn der Decoder ein Beispiel mit dem Diskontinuitätsflag empfängt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |
| Eigenschafts-ID       | AM \_ RATE \_ ResetOnTimeDisc     |
| Datentyp         | **Dword**                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft unterstützt Smooth Rate-Änderungen. Wenn der Wert dieser Eigenschaft **TRUE** ist und der Decoder ein Eingabebeispiel mit dem \_ AM SAMPLE \_ TIMEDISCONTINUITY-Flag empfängt, sollte der decodierte Frame den gleichen Zeitstempel wie der Eingaberahmen aufweisen.

Um das AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flag abzurufen, rufen [**Sie IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Beispiel auf. Das Flag wird im **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) festgelegt.

Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratenänderungseigenschaftensatz**](rate-change-property-set.md)
</dt> </dl>

 

 




