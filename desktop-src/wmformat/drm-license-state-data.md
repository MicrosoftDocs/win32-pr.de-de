---
title: DRM_LICENSE_STATE_DATA Struktur (drmexternals. h)
description: Die DRM- \_ Lizenz \_ Status- \_ Datenstruktur enthält Lizenzinformationen zu einem angegebenen DRM-Recht.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346514"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA Struktur (drmexternals. h)

Die **DRM- \_ Lizenz \_ Status- \_ Daten** Struktur enthält [*Lizenz*](wmformat-glossary.md) Informationen zu einem angegebenen [*DRM*](wmformat-glossary.md) -Recht.

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

**dwstreamid**
</dt> <dd>

Die streamnummer, für die die Lizenz gilt. Muss 0 sein. Dies bedeutet, dass die Lizenz für alle Streams in der Datei gilt.

</dd> <dt>

**dwcategory**
</dt> <dd>

Kategorie der anzuzeigenden Zeichenfolge. Mögliche Werte und deren Bedeutung finden Sie unter [**DRM- \_ Lizenz \_ Zustands \_ Kategorie**](drm-license-state-category.md) .

</dd> <dt>

**dwnumcounts**
</dt> <dd>

Anzahl der Elemente, die in **dwCount** bereitgestellt werden. Dieser Wert ist in der Regel 0 oder 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Ein Array von 0 oder mindestens einem **DWORD**-Wert, der die Häufigkeit darstellt, mit der die in **dwcategory** angegebene Aktion ausgeführt werden kann. Siehe Bemerkungen.

</dd> <dt>

**dwnumdates**
</dt> <dd>

Anzahl der Elemente, die in **DateTime** bereitgestellt werden. In der Regel werden nicht mehr als zwei Datumsangaben verwendet, z. b. mit einer Lizenz, die von einem Datum bis zu einem anderen Datum gültig ist.

</dd> <dt>

**DateTime \[ 4\]**
</dt> <dd>

Ein Array aus einer oder mehreren FILETIME-Strukturen, die ein oder mehrere Datumsangaben in der Lizenz darstellen. Die Bedeutung eines bestimmten Datums hängt vom Wert von **dwcategory** ab.

</dd> <dt>

**dwvague**
</dt> <dd>

NULL oder mehr der folgenden Flags in Kombination mit einem bitweisen **or**-Operator:



| Flag                                    | Beschreibung                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM- \_ Lizenz \_ Zustandsdaten sind \_ \_ ungenau        | Wenn diese Einstellung festgelegt ist, sind möglicherweise weitere Lizenzen für den Inhalt vorhanden.                                                                                         |
| DRM- \_ Lizenz \_ Zustandsdaten- \_ \_ OPL \_ vorhanden | Wenn diese Option festgelegt ist, enthält die Lizenz die Ausgabe Schutz Ebenen (opls), die abgerufen und mit dem Ziel der Ausgabe der Anwendung überprüft werden müssen. |
| DRM- \_ Lizenz \_ Zustands \_ Daten \_ SAP \_ vorhanden | Wenn diese Einstellung festgelegt ist, muss der Inhalt über einen sicheren Audiopfad (SAP) zugestellt werden.                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von einem [**callmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) -Befehl zurückgegeben (in einer [**WM- \_ Lizenz \_ Zustands \_ Daten**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) Struktur gekapselt), wenn Sie eine der DRM-Lizenz Zustands Eigenschaften angeben. Diese Eigenschaften sind:

-   [**DRM- \_ Lizenz Zustands \_ Wiedergabe**](drm-licensestate-playback.md)
-   [**DRM \_ licenanstate \_ copyper CD**](drm-licensestate-copytocd.md)
-   [**DRM \_ licenanstate \_ copytosdmidevice**](drm-licensestate-copytosdmidevice.md)
-   [**DRM \_ licenanstate \_ copytononsdmidevice**](drm-licensestate-copytononsdmidevice.md)
-   [**DRM \_ licenanstate \_ kollaborativeplay**](drm-licensestate-collaborativeplay.md)
-   [**DRM- \_ Lizenzstatus \_ Kopie**](drm-licensestate-copy.md)
-   [**DRM \_ licenanstate \_ playlistburn**](drm-licensestate-playlistburn.md)

Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von bis ist \_ ,** enthält das **DateTime** -Array in der Regel zwei Datumsangaben, ein "from"-Datum und ein "Until"-Datum. Es können auch zwei Datums Paare angegeben werden, um komplexere Lizenzen zu erstellen.

Die Elemente des **dwCount** -Arrays entsprechen den Datumsangaben oder Datumsbereichen, die im **DateTime** -Array angegeben sind. Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis** und **DateTime** ein Datums Paar enthält, enthält **dwCount** ein Element. Wenn **DateTime** zwei Datums Paare (vier Elemente) enthält, sollte **dwCount** zwei Elemente enthalten, eine für jedes Datums Paar.

In einigen Fällen haben Benutzer möglicherweise mehr als eine Lizenz für eine Datei ausgestellt. Beispielsweise könnten Sie eine Lizenz erworben haben, die bis zum Ende des Monats fünf Spiele zulässt und später eine zweite Lizenz für unbegrenzte Rechte erhalten hat. In einem solchen Fall wird das kennflag für die DRM- \_ Lizenz \_ Zustands \_ Daten \_ in **dwvague** () festgelegt, `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` und die DRM-Komponente verwendet einen Algorithmus, um den wahrscheinlichsten Satz von Rechten zu ermitteln, die angewendet wurden. Wenn eine Lizenz abläuft, untersucht die DRM-Komponente die verbleibenden Lizenzen usw., bis alle Lizenzen abgelaufen sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | SDK für Windows Media-Format 7 oder höhere Versionen des SDKs<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

