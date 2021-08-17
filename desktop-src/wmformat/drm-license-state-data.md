---
title: DRM_LICENSE_STATE_DATA -Struktur (Drmexternals.h)
description: Die DRM \_ LICENSE \_ STATE \_ DATA-Struktur enthält Lizenzinformationen zu einem angegebenen DRM-Recht.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6703481dc1d3608a8bf08ab2bbd216db4a9ecdc91bd4604d2b9de7d7de4fa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848533"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA -Struktur (Drmexternals.h)

Die **DRM \_ LICENSE STATE \_ \_ DATA-Struktur** enthält [*Lizenzinformationen*](wmformat-glossary.md) zu einem angegebenen [*DRM-Recht.*](wmformat-glossary.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwStreamId**
</dt> <dd>

Streamnummer, für die die Lizenz gilt. Muss 0 sein, was angibt, dass die Lizenz für alle Streams in der Datei gilt.

</dd> <dt>

**dwCategory**
</dt> <dd>

Kategorie der anzuzeigenden Zeichenfolge. Mögliche Werte und deren Bedeutung finden Sie unter [**DRM \_ LICENSE STATE \_ \_ CATEGORY.**](drm-license-state-category.md)

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Anzahl der in **dwCount bereitgestellten Elemente.** Dieser Wert ist in der Regel 0 oder 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Ein Array von 0 oder 1 oder mehr **DWORD-s,** die angeben, wie oft die in **dwCategory** angegebene Aktion ausgeführt werden kann. Siehe Bemerkungen.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Anzahl der in **datetime angegebenen Elemente.** In der Regel werden nicht mehr als zwei Datumsangaben verwendet, z. B. mit einer Lizenz, die von einem Datum bis zu einem anderen Datum gültig ist.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Ein Array von einer oder mehr FILETIME-Strukturen, die ein oder mehrere Datumsangaben in der Lizenz darstellen. Die Bedeutung eines bestimmten Datums hängt vom Wert von **dwCategory ab.**

</dd> <dt>

**dwVague**
</dt> <dd>

Null oder mehr der folgenden Flags in Kombination mit einem bitweisem **OR:**



| Flag                                    | Beschreibung                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ DRM-LIZENZSTATUSDATEN \_ \_        | Wenn festgelegt, gibt es möglicherweise weitere Lizenzen, die für den Inhalt gelten.                                                                                         |
| \_ \_ DRM-LIZENZZUSTANDSDATEN \_ \_ OPL \_ VORHANDEN | Wenn festgelegt, enthält die Lizenz Ausgabeschutzebenen (Output Protection Levels, OPLs), die abgerufen und mit dem Ziel der Anwendungsausgabe überprüft werden müssen. |
| \_ \_ DRM-LIZENZSTATUSDATEN \_ \_ SAP \_ VORHANDEN | Wenn festgelegt, muss der Inhalt mithilfe eines sicheren Audiopfads (SECURE AUDIO Path, SAP) übermittelt werden.                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird (gekapselt in einer [**WM \_ LICENSE STATE \_ \_ DATA-Struktur)**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) von einem Aufruf von [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) zurückgegeben, wenn Sie eine der DRM-Lizenzstatuseigenschaften angeben. Diese Eigenschaften sind:

-   [**DRM \_ \_ LicenseState-Wiedergabe**](drm-licensestate-playback.md)
-   [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)
-   [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)
-   [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)
-   [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)
-   [**DRM \_ LicenseState \_ Copy**](drm-licensestate-copy.md)
-   [**DRM \_ LicenseState \_ Playlist Playlist**](drm-licensestate-playlistburn.md)

Wenn **dwCategory** **WM \_ DRM LICENSE STATE COUNT \_ FROM UNTIL \_ \_ \_ \_ ist,** enthält das **datetime-Array** in der Regel zwei Datumsangaben: ein "from"-Datum und ein "until"-Datum. Es können auch zwei Datumspaare angegeben werden, um komplexere Lizenzen zu erstellen.

Die Elemente des **dwCount-Arrays** entsprechen den Datums- oder Datumsbereichen, die im **datetime-Array angegeben** sind. Wenn **dwCategory** **WM \_ DRM LICENSE STATE COUNT \_ FROM UNTIL \_ \_ \_ \_ ist** und **datetime** ein Datumspaar enthält, enthält **dwCount** ein Element. Wenn **datetime** zwei Datumspaare (vier Elemente) enthält, sollte **dwCount** zwei Elemente enthalten, eines für jedes Datumspaar.

In einigen Fällen wurden Benutzern möglicherweise mehrere Lizenzen für eine Datei ausgestellt. Beispielsweise haben sie möglicherweise eine Lizenz erworben, die fünf Spiele bis zum Ende des Monats erlaubt hat, und später eine zweite Lizenz für unbegrenzte Rechte erworben. In einem solchen Fall wird das FLAG DRM \_ LICENSE STATE DATA ALGORITHM in \_ \_ \_ **dwVague** ( ) festgelegt, und die `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` DRM-Komponente verwendet einen Algorithmus, um den wahrscheinlichsten Satz von Rechten zu bestimmen, die angewendet wurden. Wenn eine Lizenz abläuft, überprüft die DRM-Komponente die verbleibenden Lizenzen und so weiter, bis alle Lizenzen abgelaufen sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK oder neuere Versionen des SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

