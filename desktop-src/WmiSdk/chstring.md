---
description: In der folgenden Tabelle sind die chstring-Methoden aufgeführt.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: Chstring-Klasse (chstring. h)
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
ms.openlocfilehash: 0c94fcd89a41e610d039afe17f4b56e58cb117bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362650"
---
# <a name="chstring-class"></a>Chstring-Klasse

\[Die **chstring** -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

In der folgenden Tabelle sind die **chstring** -Methoden aufgeführt.

## <a name="members"></a>Member

Die **chstring** -Klasse verfügt über diese Typen von Membern:

-   [Konstruktoren](#constructors)
-   [Methoden](#methods)
-   [Operatoren](#operators)

### <a name="constructors"></a>Konstruktoren

Die **chstring** -Klasse verfügt über diese Konstruktoren.



| Konstruktor                           | BESCHREIBUNG                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**Zeichenfolge**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Erstellt **chstring-Zeichen** folgen auf verschiedene Weise.<br/> |



 

### <a name="methods"></a>Methoden

Die **chstring** -Klasse verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**"Zugeordcsysstring"**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Ordnet ein BSTR aus den **chstring** -Daten zu.<br/>                                                            |
| [**COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Vergleicht zwei Zeichen folgen (Groß-/Kleinschreibung beachten; verwendet Gebiets Schema spezifische Informationen).<br/>                            |
| [**Vergleich**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Vergleicht zwei Zeichen folgen (Groß-/Kleinschreibung beachten)<br/>                                                              |
| [**Comparoocase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Vergleicht zwei Zeichen folgen (Groß-/Kleinschreibung nicht beachtet<br/>                                                            |
| [**Leer**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Erzwingt eine Zeichenfolge mit einer Länge von 0 (null).<br/>                                                            |
| [**Sich**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Überladen. Sucht ein Zeichen oder eine Teil Zeichenfolge in einer größeren Zeichenfolge.<br/>                                  |
| [**Findoneof**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Sucht das erste übereinstimmende Zeichen aus einer Menge.<br/>                                                      |
| [**Ges**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Überladen. Formatiert die Zeichenfolge als **sprintf** .<br/>                                                 |
| [**Formatmessagew**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Überladen. Formatiert eine Nachrichten Zeichenfolge.<br/>                                                               |
| [**Formatv**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Formatiert die Zeichenfolge wie **vsprintf** .<br/>                                                            |
| [**"Freextra"**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Entfernt den zusätzlichen Aufwand dieser Zeichenfolge, indem zusätzlicher Arbeitsspeicher freigegeben wird, der zuvor der Zeichenfolge zugewiesen wurde.<br/> |
| [**Getalloclength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Gibt die Größe des Zeichen folgen Puffers zurück.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Überladen. Gibt das Zeichen an der angegebenen Position zurück.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Gibt einen Zeiger auf die Zeichen **in der Zeichenfolge Zeichen** Folge zurück.<br/>                                     |
| [**Getbuffersetlength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Gibt einen Zeiger auf die Zeichen **in der Zeichenfolge Zeichen** Folge zurück, wobei die angegebene Länge abgeschnitten wird.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Gibt einen Zeiger auf die Daten **in der Zeichenfolge Zeichen** Folge zurück.<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Gibt die Anzahl von Unicode-Zeichen in **einer Zeichen** folgen Zeichenfolge zurück.<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Testet, ob **eine Zeichen** Folge der Zeichenfolge keine Zeichen enthält.<br/>                                         |
| [**Linken**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Extrahiert den linken Teil einer Zeichenfolge (wie z. b. die grundlegende **left $** -Funktion).<br/>                             |
| [**Loadstringw**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Lädt **eine vorhandene Zeichen** folgen Zeichenfolge aus einer Ressourcen Datei.<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Deaktiviert die Verweis Zählung und schützt die Zeichenfolge im Puffer.<br/>                                  |
| [**Makelower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Konvertiert alle Zeichen in dieser Zeichenfolge in Kleinbuchstaben.<br/>                              |
| [**Makereverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Kehrt die Zeichen in dieser Zeichenfolge um.<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Konvertiert alle Zeichen in dieser Zeichenfolge in Großbuchstaben.<br/>                              |
| [**Mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Überladen. Extrahiert den mittleren Teil einer Zeichenfolge (wie z. b. die grundlegende **Mid $** -Funktion).<br/>                |
| [**ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Gibt die Steuerung des von [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)zurückgegebenen Puffers frei.<br/>                 |
| [**Reverstellen suchen**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Findet ein Zeichen innerhalb einer größeren Zeichenfolge; beginnt am Ende.<br/>                                      |
| [**Richting**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Extrahiert den rechten Teil einer Zeichenfolge (wie z. b. die Basic **right $** -Funktion).<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Legt ein Zeichen an der angegebenen Position fest.<br/>                                                               |
| [**Spannen Ausschluss**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Extrahiert eine Teil Zeichenfolge, die nur die Zeichen enthält, die nicht in der Menge enthalten sind.<br/>                     |
| [**Mit spannen**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Extrahiert eine Teil Zeichenfolge, die nur die Zeichen in einer Menge enthält.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Entfernt führende Leerzeichen aus der Zeichenfolge.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Entfernt nachfolgende Leerzeichen aus der Zeichenfolge.<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Aktiviert die Verweis Zählung und gibt die Zeichenfolge im Puffer frei.<br/>                                   |



 

### <a name="operators"></a>Operatoren
`
The **CHString** class has these operators.`



| Operator                                                                                            | BESCHREIBUNG                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**Operator! = (chstring, chstring)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Vergleicht zwei **Zeichen** folgen auf Ungleichheit.<br/>                                                             |
| [**Operator! = (chstring, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Vergleicht eine **Zeichen** Folge mit einem **LPCWSTR** auf Ungleichheit.<br/>                                             |
| [**KOM \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Gibt das Zeichen an einer angegebenen Positions Operator Ersetzung für [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))zurück.<br/> |
| [**Operator +**](chstring--operator-plus.md)                                                       | Verkettet zwei Zeichen folgen und gibt eine neue Zeichenfolge zurück.<br/>                                                     |
| [**Operator + =**](chstring--operator-plus-equal.md)                                                | Verkettet eine neue Zeichenfolge am Ende einer vorhandenen Zeichenfolge.<br/>                                            |
| [**Operator < (chstring, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Vergleicht eine **Zeichenfolge** mit einem **LPCWSTR**.<br/>                                                            |
| [**Operator < (chstring, chstring)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Vergleicht zwei **Zeichen** folgen.<br/>                                                                            |
| [**Operator <= (chstring, chstring)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Vergleicht zwei **Zeichen** folgen.<br/>                                                                            |
| [**Operator <= (chstring, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Vergleicht eine **Zeichenfolge** mit einem **LPCWSTR**.<br/>                                                            |
| [**Operator =**](chstring--operator-equal.md)                                                      | Weist **einer Zeichen folgen Zeichenfolge** einen neuen Wert zu.<br/>                                                          |
| [**Operator = = (chstring, chstring)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Vergleicht zwei **Zeichen** folgen auf Gleichheit.<br/>                                                               |
| [**Operator = = (chstring, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Vergleicht eine **Zeichen** Folge mit einem **LPCWSTR** auf Gleichheit.<br/>                                               |
| [**Operator > (chstring, chstring)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Vergleicht zwei **Zeichen** folgen.<br/>                                                                            |
| [**Operator > (chstring, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Vergleicht eine **Zeichenfolge** mit einem **LPCWSTR**.<br/>                                                            |
| [**Operator >= (chstring, chstring)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Vergleicht zwei **Zeichen** folgen.<br/>                                                                            |
| [**Operator >= (chstring, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Vergleicht eine **Zeichenfolge** mit einem **LPCWSTR**.<br/>                                                            |
| [**Operator LPCWSTR**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Greift direkt auf Zeichen zu, die **in einer Zeichenfolge als** Zeichenfolge im C-Format gespeichert sind.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Der Dekonstruktor für die Klasse ist " **chstring:: ~ chstring**".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Chstring. h (Include-Datei "f")</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>Framedyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



