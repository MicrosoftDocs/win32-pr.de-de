---
description: Der Enumerationstyp WPD EXPOSURE METERING MODES beschreibt den Messungsmodus, der bei der Schätzung der Belichtung für die Erfassung von Bildern durch ein Gerät \_ \_ verwendet werden \_ soll.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: WPD_EXPOSURE_METERING_MODES -Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a165493142fc25ea64adc2678e8bc4ccbeace32e245422f0fcea419063a26ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842280"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>WPD \_ EXPOSURE \_ METERING \_ MODES-Enumeration

Der **Enumerationstyp WPD \_ EXPOSURE \_ METERING \_ MODES** beschreibt den Messungsmodus, der bei der Schätzung der Belichtung für die Erfassung von Bildern durch ein Gerät verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD \_ EXPOSURE \_ METERING MODE \_ UNEFINED (WPD-BELICHTUNGSMESSUNGSMODUS \_ NICHT DEFINIERT)**
</dt> <dd>

Der Messungsmodus ist nicht definiert.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD \_ EXPOSURE \_ METERING \_ MODE \_ AVERAGE**
</dt> <dd>

Verwenden Sie die gemittelte Belichtung für das gesamte Bild.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD \_ EXPOSURE \_ METERING \_ MODE \_ CENTER \_ WEIGHTED \_ AVERAGE**
</dt> <dd>

Verwenden Sie eine gemittelte Belichtung, bei der der Mittelpunkt des Bilds mehr Gewichtung erhält.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD \_ EXPOSURE \_ METERING \_ MODE \_ MULTI \_ SPOT**
</dt> <dd>

Verwenden Sie eine Multi-Spot-Mittelungstechnik.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD \_ EXPOSURE \_ METERING \_ MODE \_ CENTER \_ SPOT**
</dt> <dd>

Verwenden Sie eine Mittelplatz-Mittelungstechnik.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Gibt den Messungsmodus des Geräts an. Diese Enumeration wird von der [WPD STILL \_ IMAGE EXPOSURE \_ \_ \_ METERING \_ MODE-Eigenschaft](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




