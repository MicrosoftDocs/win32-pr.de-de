---
description: Die Geschwindigkeit der Kamera, als das Foto aufgenommen wurde. Dies wird in APEX-Einheiten angegeben.
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: System.Photo.Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e5a919019e7e1f48bc8a65105c649f51745f1d33cda8518a0bfa501155ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970049"
---
# <a name="systemphotoshutterspeed"></a>System.Photo.Speed

Die Geschwindigkeit der Kamera, als das Foto aufgenommen wurde. Dies wird in APEX-Einheiten angegeben. Diese Eigenschaft wird aus [System.Photo.SpeedNumerator](./props-system-photo-shutterspeednumerator.md) und [System.Photo.SpeedDenominator berechnet.](./props-system-photo-shutterspeeddenominator.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Informationen zur Konvertierung dieses Werts in die Belichtungszeit finden Sie in der Spezifikation Exchangeable Image File (EXIF) 2.2, Anhang C. Verwenden [Sie System.Photo.ExposureTime](./props-system-photo-exposuretime.md) in allen Shellansichten anstelle von [System.Photo.Speed .]()

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Exchangeable Image File Format für Digital Still Cameras: Exif Version 2.2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
