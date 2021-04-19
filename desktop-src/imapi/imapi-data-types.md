---
title: IMAPI-Datentypen (Imapi2. h)
description: Spezifikationen für optische Medien und zugeordnete Geräte definieren Bereichs Werte für Elemente, wie z. b. die Beschreibung der DVD-Struktur, die Beschreibung der Festplatten Informationen und die Größe der funktionsseite.
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
ms.openlocfilehash: 7793bab123e2939bdc2f5a68bb705d7468da5666
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343053"
---
# <a name="imapi-data-types"></a>IMAPI-Datentypen

Spezifikationen für optische Medien und zugeordnete Geräte definieren Bereichs Werte für Elemente, wie z. b. die Beschreibung der DVD-Struktur, die Beschreibung der Festplatten Informationen und die Größe der funktionsseite. IMAPI definiert die folgenden ULONG-Typen (Ganzzahl ohne Vorzeichen Long Integer), die Bereichs Wert Limits erzwingen. Diese Typen werden ausschließlich für die optimale IDL-Validierung von Parametern definiert und als Dokumentations Hilfe für Aufrufer bezüglich der Obergrenzen für bestimmte Datenübertragungs Vorgänge verfügbar.


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





| Datentyp                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ IMAPI2 \_ DVD- \_ Struktur**                | Bereich: 0, 65535 (0, 0X0000FFFF)<br/> Die DVD-Struktur ist aufgrund eines zwei-Byte-Zuordnungs Felds auf 64 KB beschränkt.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**ULONG \_ IMAPI2 \_ Adapter \_ Deskriptor** | Bereich: 0, 268435455 (0, 0x0fffffff)<br/> Der Adapter Deskriptor ist nicht implizit in der Größe beschränkt.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**ULONG \_ IMAPI2 \_ Geräte \_ Deskriptor**    | Bereich: 0, 268435455 (0, 0x0fffffff)<br/> Der Gerätedeskriptor ist nicht implizit in der Größe beschränkt.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG \_ IMAPI2 \_ Disk- \_ Informationen**       | Bereich: 0, 65538 (0, 0x00010002)<br/> Die Festplatten Informationen sind auf 64 KB plus 2 Bytes für das Feld Größe beschränkt.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG \_ IMAPI2 nach \_ Verfolgen von \_ Informationen**    | Bereich: 0, 65538 (0, 0x00010002)<br/> Die Nachverfolgung von Informationen ist auf 64 KB plus 2 Bytes für das Feld Größe beschränkt.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**ULONG \_ IMAPI2 \_ \_ Featureseite**                   | Bereich: 0256 (0, 0x00000100)<br/> Eine einzelne funktionsseite ist auf 256 Bytes beschränkt.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**ULONG \_ IMAPI2 \_ Modus ( \_ Seite)**                            | Bereich: 0257 (0, 0x00000101)<br/> Eine Seite mit einem einzelnen Modus ist auf 257 Bytes beschränkt.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ alle \_ \_ Featureseiten**   | Bereich: 0, 65536 (0, 0x00010000 bis)<br/> Die Anzahl der Features ist auf ein 2-Byte-Feld beschränkt.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ alle \_ profile**                   | Bereich: 0, 63 (0, 0x0000003F)<br/> Die Anzahl von Profilen für ein Gerät entspricht der Anzahl von Profilen, die in eine einzelne Funktion passt. Jedes Profil belegt vier Bytes. Eine einzelne Funktion kann 252 zusätzliche Daten Bytes enthalten, die ausreichen, um maximal 63 Profile zu speichern.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ alle \_ Modus- \_ Seiten**            | Bereich: 0, 32763 (0, 0x00007ffb)<br/> Anzahl der Modusseiten für ein Gerät. Die Anzahl, über den Modus \_ SENSE10, ist auf ein Feld mit zwei Byte beschränkt.<br/> Der Mode-Parameter Header ist 8 Bytes. Jede Seite weist mindestens zwei Bytes auf. Die maximale Anzahl von Modus-Seiten ist 32763: (65535-8)/2 abgerundet.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ nicht NULL**                                   | Bereich: 1, 2147483647 (1, 0x7FFFFFFF)<br/> Generischer Wert ungleich NULL, mit dem überprüft werden kann, ob ein Wert ungleich 0 (null) ist.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ nicht \_ negativ**                   | Bereich: 0, 2147483647 (0, 0x7FFFFFFF)<br/> Eine 32-Bit-Ganzzahl mit einem nicht negativen Wert.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Imapi2. h</dt> </dl> |



 

 





