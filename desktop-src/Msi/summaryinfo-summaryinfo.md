---
description: Die Property-Eigenschaft des SummaryInfo-Objekts legt den Wert für die angegebene Eigenschaft im Zusammenfassungs Informationsdaten Strom fest oder ruft diesen ab.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo. Property (Eigenschaft)
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
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354135"
---
# <a name="summaryinfoproperty-property"></a>SummaryInfo. Property (Eigenschaft)

Die **Property** -Eigenschaft des [**SummaryInfo**](summaryinfo-object.md) -Objekts legt den Wert für die angegebene Eigenschaft im Zusammenfassungs Informationsdaten Strom fest oder ruft diesen ab. Die Eigenschaften werden gelesen, wenn das [**SummaryInfo**](summaryinfo-object.md) -Objekt erstellt wird, aber Sie werden erst geschrieben, wenn die [**Persistenzmethode**](summaryinfo-persist.md) aufgerufen wird. Das Festlegen einer Eigenschaft auf "leer" bewirkt, dass entfernt wird. Ebenso gibt das Anfordern einer nicht vorhandenen Eigenschaft einen leeren Wert zurück. Andernfalls können Werte als Zeichen folgen, ganze Zahlen oder Datums-/Uhrzeittypen übertragen werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche eigen schafts-ID einer der Zusammenfassungs Eigenschaften.

## <a name="remarks"></a>Bemerkungen

**Standard mäßige Zusammenfassungs Eigenschaften-IDs**

(keine Enumeration)



| Parametername     | Wert | BESCHREIBUNG                                       |
|--------------------|-------|---------------------------------------------------|
| PID- \_ Wörterbuch    | 0     | Sonderformat, nicht Unterstützung durch das SummaryInfo-Objekt |
| PID- \_ Codepage      | 1     | VT \_ I2                                            |
| PID- \_ Titel         | 2     | VT \_ LPSTR                                         |
| PID- \_ Betreff       | 3     | VT \_ LPSTR                                         |
| PID- \_ Autor        | 4     | VT \_ LPSTR                                         |
| PID- \_ Schlüsselwörter      | 5     | VT \_ LPSTR                                         |
| PID- \_ Kommentare      | 6     | VT \_ LPSTR                                         |
| PID- \_ Vorlage      | 7     | VT \_ LPSTR                                         |
| PID \_ lastauthor    | 8     | VT \_ LPSTR                                         |
| PID- \_ revnumber     | 9     | VT \_ LPSTR                                         |
| PID- \_ EditTime      | 10    | VT \_ FILETIME                                      |
| PID \_ lastprint   | 11    | VT \_ FILETIME                                      |
| PID \_ Erstellen von \_ DTM   | 12    | VT \_ FILETIME                                      |
| PID \_ lastsave \_ DTM | 13    | VT \_ FILETIME                                      |
| PID- \_ PageCount     | 14    | VT \_ I4                                            |
| PID- \_ WordCount     | 15    | VT \_ I4                                            |
| PID- \_ Anzahl     | 16    | VT \_ I4                                            |
| PID- \_ Miniaturansicht     | 17    | VT \_ CF (nicht unterstützt)                            |
| PID- \_ appname       | 18    | VT \_ LPSTR                                         |
| PID- \_ Sicherheit      | 19    | VT \_ I4                                            |



 

**Datentypen von Eigenschaften**

(keine Enumeration)



| Parametername | Wert | BESCHREIBUNG                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| VT \_ I2         | 2     | 16-Bit-Ganzzahl                                                                           |
| VT \_ I4         | 3     | 32-bit integer                                                                           |
| VT \_ LPSTR      | 30    | String                                                                                   |
| VT \_ FILETIME   | 64    | Datum/Uhrzeit (FILETIME, konvertiert in Variant-Zeit)                                          |
| VT \_ CF         | 71    | Zwischenablage Format + Daten, nicht vom [**SummaryInfo**](summaryinfo-object.md) -Objekt behandelt |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ isummaryinfo ist definiert als 000c109b-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msisummaryinfosetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**Msisummaryinfogetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




