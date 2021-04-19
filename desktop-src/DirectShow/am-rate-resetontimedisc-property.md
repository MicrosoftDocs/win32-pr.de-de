---
description: Gilt für Windows Vista und höher.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371651"
---
# <a name="am_rate_resetontimedisc-property"></a>\_Ate \_ rementontimedisc (Eigenschaft)

Gilt für Windows Vista und höher.

Diese Eigenschaft fragt ab, ob der Decoder die Ausgabezeit Stempel erneut mit den Eingabe Zeitstempeln synchronisiert, wenn der Decoder ein Beispiel mit dem Diskontinuität-Flag empfängt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.



|                   |                               |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropltid \_ |
| Eigenschafts-ID       | \_Rate \_ rementimedisc     |
| Datentyp         | **DWORD**                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft unterstützt Smooth-Rate-Änderungen. Wenn der Wert dieser Eigenschaft " **true** " ist und der Decoder ein Eingabe Beispiel mit dem "am \_ Sample \_ timediscontinuity"-Flag erhält, sollte der decodierte Frame denselben Zeitstempel wie der Eingabe Rahmen aufweisen.

Rufen Sie zum Abrufen des am \_ Sample Sample \_ timediscontinuity-Flags [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Beispiel auf. Das-Flag wird im **dwsampleflags** -Member der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur festgelegt.

Weitere Informationen finden Sie unter [Verbesserungen der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md)
</dt> </dl>

 

 




