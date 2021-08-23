---
title: DRM_LICENSE_STATE_DATA -Struktur (Wmdrmsdk.h)
description: Die DRM \_ LICENSE \_ STATE \_ DATA-Struktur enthält Informationen zu den Lizenzeinschränkungen für ein DRM-Recht.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: 63ba00384ec7c3340aa099f1b427cd8953969704bd0585f0da58cd4fd0ffd6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708930"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA -Struktur (Wmdrmsdk.h)

Die **DRM \_ LICENSE STATE \_ \_ DATA-Struktur** enthält Informationen zu den Lizenzeinschränkungen für ein DRM-Recht.

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

Kategorie der anzuzeigenden Zeichenfolge. Mögliche Werte und deren Bedeutung finden Sie unter [**DRM \_ LICENSE STATE \_ \_ CATEGORY.**](drmdrm-license-state-category.md)

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Anzahl der in **dwCount bereitgestellten Elemente.** Dieser Wert ist in der Regel 0 oder 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Ein Array von 0 oder 1 oder mehr **DWORD-Werten,** die angeben, wie oft die in **dwCategory** angegebene Aktion ausgeführt werden kann. Siehe Hinweise.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Anzahl der in **datetime angegebenen Elemente.** In der Regel werden nicht mehr als zwei Datumsangaben verwendet, z. B. mit einer Lizenz, die von einem Datum bis zu einem anderen Datum gültig ist.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Ein Array von einer oder mehr **FILETIME-Strukturen,** die ein oder mehrere Datumsangaben in der Lizenz darstellen. Die Bedeutung eines bestimmten Datums hängt vom Wert von **dwCategory ab.**

</dd> <dt>

**dwVague**
</dt> <dd>

Null oder mehr der folgenden Flags in Kombination mit einem bitweisem **OR:**



| Flag                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ DRM-LIZENZSTATUSDATEN \_ \_        | Wenn festgelegt, gibt es möglicherweise weitere Lizenzen, die für den Inhalt gelten. Die einzige Möglichkeit, sich über die einzelnen Lizenzen zu sorgen, die für eine bestimmte Schlüssel-ID gelten, besteht im Aufzählen der Lizenzen. Rufen Sie hierzu [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)auf, und übergeben Sie die Schlüssel-ID als bstrKID-Parameter. Verwenden Sie dann die abgerufene IWMDRMLicense-Schnittstelle, um die Lizenzen zu untersuchen. |
| \_ \_ DRM-LIZENZZUSTANDSDATEN \_ \_ OPL \_ VORHANDEN | Wenn festgelegt, enthält die Lizenz Ausgabeschutzebenen (Output Protection Levels, OPLs), die abgerufen und mit dem Ziel der Anwendungsausgabe überprüft werden müssen.                                                                                                                                                                                                                                                                                  |
| \_ \_ DRM-LIZENZSTATUSDATEN \_ \_ SAP \_ VORHANDEN | Wenn festgelegt, muss der Inhalt mithilfe eines sicheren Audiopfads (SECURE AUDIO Path, SAP) übermittelt werden.                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird durch Aufrufen von **IWMDRMLicenseQuery::QueryLicenseState abgerufen.**

Wenn **dwCategory** **WM \_ DRM LICENSE STATE COUNT \_ FROM \_ \_ \_ \_ UNTIL** ist, enthält das **datetime-Array** in der Regel zwei Datumsangaben: ein "from"-Datum und ein "until"-Datum. Es können auch zwei Datumspaare angegeben werden, um komplexere Lizenzen zu erstellen.

Die Elemente des **dwCount-Arrays** entsprechen den Datums- oder Datumsbereichen, die im **datetime-Array angegeben** sind. Wenn **dwCategory** **WM \_ DRM LICENSE STATE COUNT \_ FROM UNTIL \_ \_ \_ \_ ist** und **datetime** ein Datumspaar enthält, enthält **dwCount** ein Element. Wenn **datetime** zwei Datumspaare (vier Elemente) enthält, sollte **dwCount** zwei Elemente enthalten, eines für jedes Datumspaar.

In einigen Fällen wurden Benutzern möglicherweise mehrere Lizenzen für eine Datei ausgestellt. Beispielsweise haben sie möglicherweise eine Lizenz erworben, die fünf Spiele bis zum Ende des Monats erlaubt hat, und später eine zweite Lizenz für unbegrenzte Rechte erworben. In einem solchen Fall wird das FLAG DRM \_ LICENSE STATE DATA ALGORITHM in \_ \_ \_ **dwVague** ( ) festgelegt, und die `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` DRM-Komponente verwendet einen Algorithmus, um den wahrscheinlichsten Satz von Rechten zu bestimmen, die angewendet wurden. Wenn eine Lizenz abläuft, überprüft die DRM-Komponente die verbleibenden Lizenzen und so weiter, bis alle Lizenzen abgelaufen sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





