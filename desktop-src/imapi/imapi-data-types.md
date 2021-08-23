---
title: IMAPI-Datentypen (Imapi2.h)
description: Spezifikationen für optische Medien und zugehörige Geräte definieren Bereichswerte für Elemente wie die Beschreibung der DVD-Struktur, die Beschreibung der Datenträgerinformationen und die Größe der Featureseite.
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612010"
---
# <a name="imapi-data-types"></a>IMAPI-Datentypen

Spezifikationen für optische Medien und zugehörige Geräte definieren Bereichswerte für Elemente wie die Beschreibung der DVD-Struktur, die Beschreibung der Datenträgerinformationen und die Größe der Featureseite. IMAPI definiert die folgenden ULONG-Typen (Long Integer) ohne Vorzeichen, die Grenzwerte für Bereichswerte erzwingen. Diese Typen sind streng für eine optimale IDL-Validierung von Parametern und als Dokumentationshilfe für Aufrufer in Bezug auf die Obergrenzen für bestimmte verfügbare Datenübertragungsvorgänge definiert.


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| Datentyp                                                                                                                                  | Beschreibung                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ \_ IMAPI2-DVD-STRUKTUR \_**                | Bereich: 0,65535 (0,0x0000FFFF)<br/> Die DVD-Struktur ist aufgrund eines Zwei-Byte-Zuordnungsfelds auf 64 KB beschränkt.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**ULONG \_ \_ IMAPI2-ADAPTERDESKRIPTOR \_** | Bereich: 0,268435455 (0,0x0FFFFFFF)<br/> Die Größe des Adapterdeskriptors ist nicht implizit beschränkt.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**ULONG \_ \_ IMAPI2-GERÄTEDESKRIPTOR \_**    | Bereich: 0,268435455 (0,0x0FFFFFFF)<br/> Die Größe des Gerätedeskriptors ist nicht implizit beschränkt.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG \_ \_ IMAPI2-DATENTRÄGERINFORMATIONEN \_**       | Bereich: 0,65538 (0,0x00010002)<br/> Datenträgerinformationen sind für das Größenfeld auf 64 KB plus 2 Bytes beschränkt.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG \_ IMAPI2– \_ NACHVERFOLGEN VON \_ INFORMATIONEN**    | Bereich: 0,65538 (0,0x00010002)<br/> Nachverfolgungsinformationen sind für das Größenfeld auf 64 KB plus 2 Bytes beschränkt.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**ULONG \_ \_ IMAPI2-FEATURESEITE \_**                   | Bereich: 0.256 (0,0x00000100)<br/> Eine einzelne Featureseite ist auf 256 Bytes beschränkt.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**SEITE "ULONG \_ \_ IMAPI2-MODUS" \_**                            | Bereich: 0.257 (0,0x00000101)<br/> Eine Seite im Einzelmodus ist auf 257 Bytes beschränkt.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ ALL \_ FEATURE \_ PAGES**   | Bereich: 0,65536 (0,0x00010000)<br/> Die Anzahl der Features ist auf ein Zwei-Byte-Feld beschränkt.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ ALL \_ PROFILES**                   | Bereich: 0,63 (0,0x0000003F)<br/> Die Anzahl der Profile für ein Gerät ist die Anzahl von Profilen, die in ein einzelnes Feature passen. Jedes Profil belegt vier Bytes. Ein einzelnes Feature kann 252 zusätzliche Bytes an Daten enthalten, die zum Speichern von maximal 63 Profilen ausreichen.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ ALL \_ MODE \_ PAGES**            | Bereich: 0,32763 (0,0x00007FFB)<br/> Anzahl der Modusseiten für ein Gerät. Die Anzahl über MODE \_ SENSE10 ist auf ein Zwei-Byte-Feld beschränkt.<br/> Der Mode-Parameterheader beträgt 8 Bytes. Jede Seite besteht aus mindestens zwei Bytes. Die maximale Anzahl von Seiten im Modus beträgt 32763: (65535 – 8)/2 abgerundet.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ NONZERO**                                   | Bereich: 1,2147483647 (1,0x7FFFFFFF)<br/> Generischer Wert ungleich 0 (null), mit dem überprüft werden kann, ob ein Wert nicht 0 (null) ist.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ NICHT \_ NEGATIV**                   | Bereich: 0, 2147483647 (0,0x7FFFFFFF)<br/> Eine 32-Bit-Ganzzahl mit einem nicht negativen Wert.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Imapi2.h</dt> </dl> |



 

 





