---
title: DRM_LICENSE_STATE_DATA Struktur (wmdrmsdk. h)
description: Die Datenstruktur des DRM- \_ Lizenz \_ Zustands \_ enthält Informationen zu den Lizenzbeschränkungen für ein DRM-Recht.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370232"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA Struktur (wmdrmsdk. h)

Die **Datenstruktur des DRM- \_ Lizenz \_ Zustands \_** enthält Informationen zu den Lizenzbeschränkungen für ein DRM-Recht.

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

Kategorie der anzuzeigenden Zeichenfolge. Mögliche Werte und deren Bedeutung finden Sie unter [**DRM- \_ Lizenz \_ Zustands \_ Kategorie**](drmdrm-license-state-category.md) .

</dd> <dt>

**dwnumcounts**
</dt> <dd>

Anzahl der Elemente, die in **dwCount** bereitgestellt werden. Dieser Wert ist in der Regel 0 oder 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Ein Array von 0 oder mindestens einem **DWORD** -Wert, der die Häufigkeit darstellt, mit der die in **dwcategory** angegebene Aktion ausgeführt werden kann. Siehe Hinweise.

</dd> <dt>

**dwnumdates**
</dt> <dd>

Anzahl der Elemente, die in **DateTime** bereitgestellt werden. In der Regel werden nicht mehr als zwei Datumsangaben verwendet, z. b. mit einer Lizenz, die von einem Datum bis zu einem anderen Datum gültig ist.

</dd> <dt>

**DateTime \[ 4\]**
</dt> <dd>

Ein Array aus einer oder mehreren **FILETIME** -Strukturen, die ein oder mehrere Datumsangaben in der Lizenz darstellen. Die Bedeutung eines bestimmten Datums hängt vom Wert von **dwcategory** ab.

</dd> <dt>

**dwvague**
</dt> <dd>

NULL oder mehr der folgenden Flags in Kombination mit einem bitweisen **or**-Operator:



| Flag                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM- \_ Lizenz \_ Zustandsdaten sind \_ \_ ungenau        | Wenn diese Einstellung festgelegt ist, sind möglicherweise weitere Lizenzen für den Inhalt vorhanden. Die einzige Möglichkeit, sich über die einzelnen Lizenzen zu kümmern, die für eine bestimmte Schlüssel-ID gelten, ist die Enumeration der Lizenzen. Um dies zu erreichen, nennen Sie [**iwmdrmlicenaberation:: kreatelicensetup**](iwmdrmlicensemanagement-createlicenseenumeration.md), und übergeben Sie dabei die Schlüssel-ID als bstrinkid-Parameter. Verwenden Sie dann die abgerufene iwmdrmlicense-Schnittstelle, um die Lizenzen zu überprüfen. |
| DRM- \_ Lizenz \_ Zustandsdaten- \_ \_ OPL \_ vorhanden | Wenn diese Option festgelegt ist, enthält die Lizenz die Ausgabe Schutz Ebenen (opls), die abgerufen und mit dem Ziel der Ausgabe der Anwendung überprüft werden müssen.                                                                                                                                                                                                                                                                                  |
| DRM- \_ Lizenz \_ Zustands \_ Daten \_ SAP \_ vorhanden | Wenn diese Einstellung festgelegt ist, muss der Inhalt über einen sicheren Audiopfad (SAP) zugestellt werden.                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird durch Aufrufen von **iwmdrmlicensequery:: querylicenserstate** abgerufen.

Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis** ist, enthält das **DateTime** -Array in der Regel zwei Datumsangaben: ein "from"-Datum und ein "Until"-Datum. Es können auch zwei Datums Paare angegeben werden, um komplexere Lizenzen zu erstellen.

Die Elemente des **dwCount** -Arrays entsprechen den Datumsangaben oder Datumsbereichen, die im **DateTime** -Array angegeben sind. Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis** und **DateTime** ein Datums Paar enthält, enthält **dwCount** ein Element. Wenn **DateTime** zwei Datums Paare (vier Elemente) enthält, sollte **dwCount** zwei Elemente enthalten, eine für jedes Datums Paar.

In einigen Fällen haben Benutzer möglicherweise mehr als eine Lizenz für eine Datei ausgestellt. Beispielsweise könnten Sie eine Lizenz erworben haben, die bis zum Ende des Monats fünf Spiele zulässt und später eine zweite Lizenz für unbegrenzte Rechte erhalten hat. In einem solchen Fall wird das kennflag für die DRM- \_ Lizenz \_ Zustands \_ Daten \_ in **dwvague** () festgelegt, `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` und die DRM-Komponente verwendet einen Algorithmus, um den wahrscheinlichsten Satz von Rechten zu ermitteln, die angewendet wurden. Wenn eine Lizenz abläuft, werden die verbleibenden Lizenzen von der DRM-Komponente untersucht usw., bis alle Lizenzen abgelaufen sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





