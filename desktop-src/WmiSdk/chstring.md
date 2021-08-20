---
description: In der folgenden Tabelle sind die CHString-Methoden aufgeführt.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: CHString-Klasse (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 4da0ee10493931c46da0879caf39ce5a1ac186cbb11dc4379343ea21120fac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109188"
---
# <a name="chstring-class"></a>CHString-Klasse

\[Die **CHString-Klasse** ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

In der folgenden Tabelle sind die **CHString-Methoden** aufgeführt.

## <a name="members"></a>Member

Die **CHString-Klasse** verfügt über folgende Typen von Membern:

-   [Konstruktoren](#constructors)
-   [Methoden](#methods)
-   [Operatoren](#operators)

### <a name="constructors"></a>Konstruktoren

Die **CHString-Klasse** verfügt über diese Konstruktoren.



| Konstruktor                           | BESCHREIBUNG                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Erstellt **CHString-Zeichenfolgen** auf verschiedene Weise.<br/> |



 

### <a name="methods"></a>Methoden

Die **CHString-Klasse** verfügt über diese Methoden.



| Methode                                                    | Beschreibung                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Ordnet einen BSTR aus **CHString-Daten** zu.<br/>                                                            |
| [**Sortieren**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Vergleicht zwei Zeichenfolgen (Groß-/Kleinschreibung wird beachtet; verwendet gebietsschemaspezifische Informationen).<br/>                            |
| [**Vergleich**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Vergleicht zwei Zeichenfolgen (Groß-/Kleinschreibung wird beachtet).<br/>                                                              |
| [**CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Vergleicht zwei Zeichenfolgen (Groß-/Kleinschreibung wird nicht beachtet).<br/>                                                            |
| [**Leer**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Erzwingt, dass eine Zeichenfolge eine Länge von 0 (null) hat.<br/>                                                            |
| [**Suchen**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Überladen. Sucht ein Zeichen oder eine Teilzeichenfolge innerhalb einer größeren Zeichenfolge.<br/>                                  |
| [**FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Sucht das erste übereinstimmende Zeichen aus einem Satz.<br/>                                                      |
| [**Format**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Überladen. Formatiert die Zeichenfolge wie **sprintf.**<br/>                                                 |
| [**FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Überladen. Formatiert eine Meldungszeichenfolge.<br/>                                                               |
| [**FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Formatiert die Zeichenfolge wie **vsprintf.**<br/>                                                            |
| [**FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Entfernt jeglichen Mehraufwand für diese Zeichenfolge, indem zusätzlicher Speicher freigegeben wird, der der Zeichenfolge zuvor zugeordnet wurde.<br/> |
| [**GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Gibt die Größe des Zeichenfolgenpuffers zurück.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Überladen. Gibt das Zeichen an einer angegebenen Position zurück.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Gibt einen Zeiger auf die Zeichen in der **CHString-Zeichenfolge** zurück.<br/>                                     |
| [**GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Gibt einen Zeiger auf die Zeichen in der **CHString-Zeichenfolge** zurück, der auf die angegebene Länge abgeschnitten wird.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Gibt einen Zeiger auf die Daten in der **CHString-Zeichenfolge** zurück.<br/>                                           |
| [**Getlength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Gibt die Anzahl der Unicode-Zeichen in einer **CHString-Zeichenfolge** zurück.<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Testet, ob eine **CHString-Zeichenfolge** keine Zeichen enthält.<br/>                                         |
| [**Links**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Extrahiert den linken Teil einer Zeichenfolge (z. B. die **Left$-Funktion** basic).<br/>                             |
| [**LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Lädt eine vorhandene **CHString-Zeichenfolge** aus einer Ressourcendatei.<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Deaktiviert die Verweiszählung und schützt die Zeichenfolge im Puffer.<br/>                                  |
| [**MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Konvertiert alle Zeichen in dieser Zeichenfolge in Kleinbuchstaben.<br/>                              |
| [**MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Kehrt die Zeichen in dieser Zeichenfolge um.<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Konvertiert alle Zeichen in dieser Zeichenfolge in Großbuchstaben.<br/>                              |
| [**Mitte**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Überladen. Extrahiert den mittleren Teil einer Zeichenfolge (z. B. die **MID$-Funktion** Basic).<br/>                |
| [**ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Gibt die Steuerung des von [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)zurückgegebenen Puffers frei.<br/>                 |
| [**ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Sucht ein Zeichen in einer größeren Zeichenfolge. beginnt am Ende.<br/>                                      |
| [**Richting**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Extrahiert den rechten Teil einer Zeichenfolge (z. B. die **Right$-Funktion** basic).<br/>                           |
| [**Setat**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Legt ein Zeichen an einer angegebenen Position fest.<br/>                                                               |
| [**SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Extrahiert eine Teilzeichenfolge, die nur die Zeichen enthält, die nicht im Satz enthalten sind.<br/>                     |
| [**SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Extrahiert eine Teilzeichenfolge, die nur die Zeichen in einem Satz enthält.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Entfernt führende Leerzeichen aus der Zeichenfolge.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Entfernt nachfolgende Leerzeichen aus der Zeichenfolge.<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Aktiviert die Verweiszählung und gibt die Zeichenfolge im Puffer frei.<br/>                                   |



 

### <a name="operators"></a>Operatoren
`
The **CHString** class has these operators.`



| Operator                                                                                            | Beschreibung                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**operator != (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Vergleicht zwei **CHStrings** auf Ungleichheit.<br/>                                                             |
| [**operator != (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Vergleicht einen **CHString** mit einem **LPCWSTR** auf Ungleichheit.<br/>                                             |
| [**Operator \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Gibt das Zeichen an einer angegebenen Positionsoperatorersetzung für [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))zurück.<br/> |
| [**Operator +**](chstring--operator-plus.md)                                                       | Verkettet zwei Zeichenfolgen und gibt eine neue Zeichenfolge zurück.<br/>                                                     |
| [**Operator +=**](chstring--operator-plus-equal.md)                                                | Verkettet eine neue Zeichenfolge am Ende einer vorhandenen Zeichenfolge.<br/>                                            |
| [**operator < (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Vergleicht einen **CHString** mit einem **LPCWSTR.**<br/>                                                            |
| [**operator < (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Vergleicht zwei **CHStrings.**<br/>                                                                            |
| [**operator <= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Vergleicht zwei **CHStrings.**<br/>                                                                            |
| [**operator <= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Vergleicht einen **CHString** mit einem **LPCWSTR.**<br/>                                                            |
| [**operator =**](chstring--operator-equal.md)                                                      | Weist einer **CHString-Zeichenfolge** einen neuen Wert zu.<br/>                                                          |
| [**operator == (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Vergleicht zwei **CHStrings** auf Gleichheit.<br/>                                                               |
| [**operator == (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Vergleicht einen **CHString** mit einem **LPCWSTR** auf Gleichheit.<br/>                                               |
| [**operator > (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Vergleicht zwei **CHStrings.**<br/>                                                                            |
| [**operator > (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Vergleicht einen **CHString** mit einem **LPCWSTR.**<br/>                                                            |
| [**operator >= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Vergleicht zwei **CHStrings.**<br/>                                                                            |
| [**operator >= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Vergleicht einen **CHString** mit einem **LPCWSTR.**<br/>                                                            |
| [**Operator LPCWSTR**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Greift direkt auf Zeichen zu, die in einer **CHString-Zeichenfolge** als Zeichenfolge im C-Format gespeichert sind.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Der Destruktor für die -Klasse ist **CHString::~CHString**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChString.h (include FwCommon.h)</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



