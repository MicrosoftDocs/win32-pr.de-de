---
description: Die Property-Eigenschaft des SummaryInfo-Objekts legt den Wert für die angegebene Eigenschaft im Zusammenfassungsinformationsstream fest oder ruft sie ab.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo.Property-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3b8635d081b44adfad3b3e869cb7fab96ee3d81107a8d962153f1caa5a14ac72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624092"
---
# <a name="summaryinfoproperty-property"></a>SummaryInfo.Property-Eigenschaft

Die **Property-Eigenschaft** des [**SummaryInfo-Objekts**](summaryinfo-object.md) legt den Wert für die angegebene Eigenschaft im Zusammenfassungsinformationsstream fest oder ruft sie ab. Die Eigenschaften werden gelesen, wenn das [**SummaryInfo-Objekt**](summaryinfo-object.md) erstellt wird, aber sie werden erst geschrieben, wenn die [**Persist-Methode**](summaryinfo-persist.md) aufgerufen wird. Wenn eine Eigenschaft auf Leer festgelegt wird, wird sie entfernt. Ebenso gibt das Anfordern einer nicht vorhandenen Eigenschaft einen leeren Wert zurück. Andernfalls können Werte als Zeichenfolgen, ganze Zahlen oder Datumstypen (Datum/Uhrzeit) übertragen werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Eigenschaften-ID einer der Zusammenfassungseigenschaften.

## <a name="remarks"></a>Hinweise

**Standard-Zusammenfassungseigenschaften-IDs**

(keine Enumeration)



| Parametername     | Wert | Beschreibung                                       |
|--------------------|-------|---------------------------------------------------|
| PID \_ DICTIONARY    | 0     | Spezielles Format, nicht unterstützt vom SummaryInfo-Objekt |
| PID \_ CODEPAGE      | 1     | VT \_ I2                                            |
| PID \_ TITLE         | 2     | VT \_ LPSTR                                         |
| \_PID-BETREFF       | 3     | VT \_ LPSTR                                         |
| PID \_ AUTHOR        | 4     | VT \_ LPSTR                                         |
| \_PID-SCHLÜSSELWÖRTER      | 5     | VT \_ LPSTR                                         |
| \_PID-KOMMENTARE      | 6     | VT \_ LPSTR                                         |
| \_PID-VORLAGE      | 7     | VT \_ LPSTR                                         |
| PID \_ LASTAUTHOR    | 8     | VT \_ LPSTR                                         |
| PID \_ REVNUMBER     | 9     | VT \_ LPSTR                                         |
| PID \_ EDITTIME      | 10    | VT \_ FILETIME                                      |
| PID \_ LASTPRINTED   | 11    | VT \_ FILETIME                                      |
| PID \_ CREATE \_ PIC   | 12    | VT \_ FILETIME                                      |
| PID \_ LASTSAVE \_ PNR | 13    | VT \_ FILETIME                                      |
| PID \_ PAGECOUNT     | 14    | VT \_ I4                                            |
| PID \_ WORDCOUNT     | 15    | VT \_ I4                                            |
| PID \_ CHARCOUNT     | 16    | VT \_ I4                                            |
| \_PID-MINIATURANSICHT     | 17    | VT \_ CF (nicht unterstützt)                            |
| PID \_ APPNAME       | 18    | VT \_ LPSTR                                         |
| \_PID-SICHERHEIT      | 19    | VT \_ I4                                            |



 

**Datentypen von Eigenschaften**

(keine Enumeration)



| Parametername | Wert | Beschreibung                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| VT \_ I2         | 2     | 16-Bit-Ganzzahl                                                                           |
| VT \_ I4         | 3     | 32-bit integer                                                                           |
| VT \_ LPSTR      | 30    | String                                                                                   |
| VT \_ FILETIME   | 64    | Datum/Uhrzeit (FILETIME, konvertiert in Variant-Zeit)                                          |
| VT \_ CF         | 71    | Zwischenablageformat + Daten, nicht vom [**SummaryInfo-Objekt**](summaryinfo-object.md) verarbeitet |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo ist als 000C109B-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




