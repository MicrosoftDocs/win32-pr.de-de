---
description: Die WBEMTime-Klasse ermöglicht Konvertierungen zwischen verschiedenen Windows und ANSI C-Laufzeitformaten. Weitere Informationen finden Sie auch unter WBEMTimeSpan-Klassenmethoden.
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: WBEMTime-Klasse (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 16b4e8933113386e877aec23313f74695b321f932c10f0e2730bcf5888675cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553246"
---
# <a name="wbemtime-class"></a>WBEMTime-Klasse

\[Die **WBEMTime-Klasse** ist Teil des WMI-Anbieterframework, das jetzt als endgültig betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken ausdrungen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **WBEMTime-Klasse** ermöglicht Konvertierungen zwischen verschiedenen Windows und ANSI C-Laufzeitformaten. Weitere Informationen finden Sie auch unter [**WBEMTimeSpan-Klassenmethoden.**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)

## <a name="members"></a>Member

Die **WBEMTime-Klasse** verfügt über die folgenden Membertypen:

-   [Konstruktoren](#constructors)
-   [Methoden](#methods)

### <a name="constructors"></a>Konstruktoren

Die **WBEMTime-Klasse** verfügt über diese Konstruktoren.



| Konstruktor                           | BESCHREIBUNG                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Konstruktor, der Konvertierungen zwischen verschiedenen Windows und ANSI C-Laufzeitformaten ermöglicht.<br/> |



 

### <a name="methods"></a>Methoden

Die **WBEMTime-Klasse** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Klar**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Legt die Zeit im **WBEMTime-Objekt** auf eine ungültige Zeit fest.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Stellt die Uhrzeit als **BSTR-Wert** vor.<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Ruft die Uhrzeit als **BSTR-Wert** im CIM-DateTime-Format ab.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Ruft ein DMTF-Datum ab, das auf einem FAT-Format oder einem Datums- und [Uhrzeitformat](date-and-time-format.md) basiert, bei dem die UTC nicht bekannt ist.<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Ruft die Uhrzeit als **MFC-FILETIME-Struktur** ab.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Überladen. Gibt den Offset in Minuten (+ oder -) zwischen GMT und Ortszeit für die im -Argument angegebene Zeit zurück.<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Ruft die Zeit als ANSI C-Laufzeitstruktur **tm-Struktur** ab.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Ruft die Uhrzeit als **MFC-SYSTEMTIME-Struktur** ab.<br/>                                                                           |
| [**Gettime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Ruft die Uhrzeit als 64-Bit-Ganzzahl ab.<br/>                                                                                          |
| [**Gettime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Ruft die Zeit als ANSI C-Laufzeitvariable \_ t ab.<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Gibt an, ob **das WBEMTime-Objekt** eine gültige Zeit darstellt.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Legt die Uhrzeit im **WBEMTime-Objekt** im CIM-DateTime-Format fest.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Überladene WBEMTime-Operatoren

Das **WBEMTime-Objekt** definiert die folgenden überladenen Operatoren.



| Überladene WBEMTime-Operatoren                                                                                                                                                                                                                                                                                                                                                                                                                                        | Beschreibung                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operator =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *Der* Zuweisungsoperator ermöglicht Konvertierungen zwischen Windows und ANSI C-Laufzeitformaten.                           |
| [**Operator +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | *Der* Additionsoperator erhöht die Zeit eines Objekts um eine Zeitspanne. Das Ergebnis wird in einem neuen **WBEMTime-Objekt** zurückgegeben.              |
| [**operator +=**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | *Der Add-and-Assign-Operator* erhöht die Zeit eines Objekts um eine Zeitspanne.                                                             |
| [**Operator :**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *Der Subtraktionsoperator* dekrementiert die Zeit eines Objekts um die Zeit eines anderen Objekts. Das Ergebnis wird in einem neuen **WBEMTime-Objekt** zurückgegeben. |
| [**operator -=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | *Der Subtract-and-Assign-Operator* dekrementiert die Zeit eines Objekts um eine Zeitspanne.                                                        |
| [**operator ==**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**operator !=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**Operator >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**operator >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**Operator <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**operator <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Vergleichsoperatoren vergleichen zwei **WBEMTime-Objekte.**                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

