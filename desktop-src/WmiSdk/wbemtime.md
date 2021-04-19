---
description: Die wbemtime-Klasse vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten. Weitere Informationen finden Sie unter wbemtimespan Class Methods.
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
ms.openlocfilehash: 5d2f06b06db998dc18a876e0e5534e1d86c6ae89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349700"
---
# <a name="wbemtime-class"></a>Wbemtime-Klasse

\[Die **wbemtime** -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **wbemtime** -Klasse vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten. Weitere Informationen finden Sie unter [**wbemtimespan Class Methods**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Member

Die **wbemtime** -Klasse verfügt über diese Typen von Membern:

-   [Konstruktoren](#constructors)
-   [Methoden](#methods)

### <a name="constructors"></a>Konstruktoren

Die **wbemtime** -Klasse verfügt über diese Konstruktoren.



| Konstruktor                           | BESCHREIBUNG                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Wbemtime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Konstruktor, der Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten erleichtert.<br/> |



 

### <a name="methods"></a>Methoden

Die **wbemtime** -Klasse verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Klartext**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Legt die Zeit im **wbemtime** -Objekt auf eine ungültige Zeit fest.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Zeigt die Uhrzeit als **BSTR** -Wert an.<br/>                                                                                      |
| [**Getdmtf**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Ruft die Zeit als **BSTR** -Wert im CIM-DateTime-Format ab.<br/>                                                                   |
| [**Getdmtf nonntfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Ruft ein DMTF-Datum ab, das auf einem FAT-oder [Datums-und Uhrzeit Format](date-and-time-format.md) basiert, bei dem die UTC nicht bekannt ist.<br/> |
| [**' GetFileTime '**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Ruft die Zeit als MFC- **FILETIME** -Struktur ab.<br/>                                                                             |
| [**Getlocaloffsetfordate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Überladen. Gibt den Offset in Minuten (+ oder-) zwischen GMT und Ortszeit für die im Argument angegebene Zeit zurück.<br/>         |
| [**Getstructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Ruft die Zeit als ANSI C-Laufzeitstruktur- **TM** -Struktur ab.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Ruft die Zeit als MFC- **Systemzeit** -Struktur ab.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Ruft die Zeit als 64-Bit-Ganzzahl ab.<br/>                                                                                          |
| [**GetTime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Ruft die Zeit als ANSI C-Lauf Zeitvariable ab \_ .<br/>                                                                       |
| [**IsOK**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Gibt an, ob das **wbemtime** -Objekt eine gültige Zeit darstellt.<br/>                                                          |
| [**Setdmtf**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Legt die Zeit im **wbemtime** -Objekt im CIM-DateTime-Format fest.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Überladene wbemtime

Das **wbemtime** -Objekt definiert die folgenden überladenen Operatoren.



| Überladene wbemtime                                                                                                                                                                                                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Operator =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | Der *Zuweisungs* Operator vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten.                           |
| [**Operator +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | Der *Additions Operator erhöht* die Zeit eines Objekts um eine Zeitspanne. Das Ergebnis wird in einem neuen **wbemtime** -Objekt zurückgegeben.              |
| [**Operator + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | Der Operator zum *Hinzufügen und zuweisen* erhöht die Zeit eines Objekts um eine Zeitspanne.                                                             |
| [**KOM**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *Subtraktions* Operator dekrementert die Zeit eines Objekts um die Zeit eines anderen Objekts. Das Ergebnis wird in einem neuen **wbemtime** -Objekt zurückgegeben. |
| [**Operator-=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | Der *Subtract-Operator und der Assign-* Operator dekrementierungen die Zeit eines Objekts um eine Zeitspanne.                                                        |
| [**Operator = =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)-[**Operator! =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**Operator >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**Operator >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**Operator <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**Operator <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Vergleichs Operatoren vergleichen zwei **wbemtime** -Objekte.                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Wbemtime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

