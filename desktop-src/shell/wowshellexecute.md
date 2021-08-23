---
description: Führt einen Vorgang für eine angegebene Datei aus.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 4389c348a06b7c54dc899da8114eee09e740681f043084bb0c32ab9f7163772e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591830"
---
# <a name="wowshellexecute-function"></a>WOWShellExecute-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Führt einen Vorgang für eine angegebene Datei aus. **WOWShellExecute** ist nur für die Verwendung mit dem virtuellen MICROSOFT WINDOWS-DOS-Computer (Ntvdm.exe) vorhanden, der die Ausführung von Datenträgerbetriebssystem (DISK OPERATING SYSTEM, DOS) und 16-Bit-Software auf einem Windows-System ermöglicht und nicht von anderen Benutzern verwendet werden sollte. Verwenden [**Sie stattdessen ShellExecute.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)

## <a name="syntax"></a>Syntax


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das Besitzerfenster, das zum Anzeigen einer Benutzeroberfläche oder von Fehlermeldungen verwendet wird. Dieser Wert kann NULL **sein,** wenn der Vorgang nicht einem Fenster zugeordnet ist.

</dd> <dt>

*lpOperation* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf eine mit **NULL** beendete Zeichenfolge, die in diesem Fall als Verb bezeichnet wird und die durchzuführende Aktion angibt.  Der Satz der verfügbaren Verben hängt von der jeweiligen Datei oder dem Jeweiligen Ordner ab. Im Allgemeinen sind die aktionen, die über das Kontextmenü eines Objekts verfügbar sind, Verben verfügbar. Weitere Informationen zu Verben und deren Verfügbarkeit finden Sie im Abschnitt *Objektverben* unter [Starten von Anwendungen.](launch.md) Weitere [Informationen zu Kontextmenüs](context.md) finden Sie unter Erweitern von Kontextmenüs. Die folgenden Verben werden häufig verwendet.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**Bearbeiten**


</dt> <dd>

Startet einen Editor und öffnet das Dokument zur Bearbeitung. Wenn *lpFile* keine Dokumentdatei ist, kann die Funktion nicht verwendet werden.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**Erkunden**


</dt> <dd>

Untersucht den durch *lpFile angegebenen Ordner.*

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**Finden**


</dt> <dd>

Initiiert eine Suche ab dem angegebenen Verzeichnis.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**Öffnen**


</dt> <dd>

Öffnet die durch den *lpFile-Parameter angegebene* Datei. Die Datei kann eine ausführbare Datei, eine Dokumentdatei oder ein Ordner sein.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**Drucken**


</dt> <dd>

Gibt die durch lpFile angegebene *Dokumentdatei aus.* Wenn *lpFile* keine Dokumentdatei ist, kann die Funktion nicht verwendet werden.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**Null**


</dt> <dd>

Bei Systemen vor Windows 2000 wird das Standardverb verwendet, wenn es gültig und in der Registrierung verfügbar ist. Wenn nicht, wird das Verb "open" verwendet.

Für Windows 2000- und höher-Systeme wird das Standardverb verwendet, falls verfügbar. Wenn nicht, wird das Verb "open" verwendet. Wenn kein Verb verfügbar ist, verwendet das System das erste verb, das in der Registrierung aufgeführt ist.

</dd> </dl> </dd> <dt>

*lpFile* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf eine mit **NULL beendete** Zeichenfolge, die die Datei oder das Objekt angibt, für die bzw. das das angegebene Verb ausgeführt werden soll. Um ein Shell-Namespaceobjekt anzugeben, übergeben Sie den vollqualifizierten Analysenamen. Beachten Sie, dass nicht alle Verben für alle Objekte unterstützt werden. Beispielsweise unterstützen nicht alle Dokumenttypen das Verb "print".

</dd> <dt>

*lpParameters* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Wenn der *lpFile-Parameter* eine ausführbare Datei angibt, *ist lpParameters* ein Zeiger auf eine mit **NULL** beendete Zeichenfolge, die die Parameter angibt, die an die Anwendung übergeben werden sollen. Das Format dieser Zeichenfolge wird durch das Verb bestimmt, das aufgerufen werden soll. Wenn *lpFile* eine Dokumentdatei angibt, *sollte lpParameters* NULL **sein.**

</dd> <dt>

*lpDirectory* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf eine mit **NULL beendete** Zeichenfolge, die das Standardverzeichnis angibt.

</dd> <dt>

*nShowCmd* \[ In\]
</dt> <dd>

Typ: **INT**

Die Flags, die angeben, wie eine Anwendung beim Öffnen angezeigt werden soll. Wenn *lpFile* eine Dokumentdatei angibt, wird das Flag einfach an die zugeordnete Anwendung übergeben. Es liegt an der Anwendung, zu entscheiden, wie sie damit umgegangen werden soll. Dies kann einer der Werte sein, die im *nCmdShow-Parameter* für die [ShowWindow-Funktion angegeben werden](/windows/desktop/api/winuser/nf-winuser-showwindow) können.

</dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Typ: **\* void**

Rückruffunktion zum Aufrufen von [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) im 16-Bit-Kernel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HINSTANCE**

Gibt bei Erfolg einen Wert größer als 32 oder andernfalls einen Fehlerwert zurück, der kleiner oder gleich 32 ist. In der folgenden Tabelle sind die Fehlerwerte aufgeführt. Der Rückgabewert wird aus Gründen der Abwärtskompatibilität mit 16-Bit-Windows in HINSTANCE-Windows werden. Es handelt sich jedoch nicht um eine echte HINSTANCE. Die zurückgegebene HINSTANCE kann nur verwendet werden, um sie **in einen int-Wert** zu casten und mit dem Wert 32 oder einem der folgenden Fehlercodes zu vergleichen.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | Der Arbeitsspeicher oder die Ressourcen des Betriebssystems sind nicht verfügbar.<br/>                                                                                                           |
| <dl> <dt>**FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>  | Die angegebene Datei wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>  | Der angegebene Pfad wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**FEHLER: \_ \_ FEHLERHAFTES FORMAT**</dt> </dl>       | Die .exe ist ungültig (Nicht-Win32-.exe oder Fehler in .exe Image).<br/>                                                                                             |
| <dl> <dt>**\_SE ERR \_ ACCESSDENIED**</dt> </dl>    | Das Betriebssystem hat den Zugriff auf die angegebene Datei verweigert.<br/>                                                                                                     |
| <dl> <dt>**\_SE ERR \_ ASSOCINCOMPLETE**</dt> </dl> | Die Dateinamensassoz ist unvollständig oder ungültig.<br/>                                                                                                           |
| <dl> <dt>**\_SE ERR \_ DDEBUSY**</dt> </dl>         | Die DDE-Transaktion konnte nicht abgeschlossen werden, da andere DDE-Transaktionen verarbeitet wurden.<br/>                                                               |
| <dl> <dt>**\_SE ERR \_ DDEFAIL**</dt> </dl>         | Fehler bei der DDE-Transaktion.<br/>                                                                                                                                   |
| <dl> <dt>**\_SE ERR \_ DDETIMEOUT**</dt> </dl>      | Die DDE-Transaktion konnte nicht abgeschlossen werden, da bei der Anforderung ein Time out auftlog.<br/>                                                                                     |
| <dl> <dt>**\_SE ERR \_ DLLNOTFOUND**</dt> </dl>     | Die angegebene DLL wurde nicht gefunden.<br/>                                                                                                                              |
| <dl> <dt>**\_SE \_ERR-FNF**</dt> </dl>             | Die angegebene Datei wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**\_SE ERR \_ NOASSOC**</dt> </dl>         | Der angegebenen Dateierweiterung ist keine Anwendung zugeordnet. Dieser Fehler wird auch zurückgegeben, wenn Sie versuchen, eine datei zu drucken, die nicht druckbar ist.<br/> |
| <dl> <dt>**\_SE ERR \_ OOM**</dt> </dl>             | Es war nicht genügend Arbeitsspeicher vorhanden, um den Vorgang abschließen zu können.<br/>                                                                                                        |
| <dl> <dt>**\_SE ERR \_ PNF**</dt> </dl>             | Der angegebene Pfad wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**\_SE \_ERR-FREIGABE**</dt> </dl>           | Ein Freigabeverstoß ist aufgetreten.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

**WOWShellExecute** ist nicht in einer Header- oder LIB-Datei enthalten. Es wird nach Namen aus Shell32.dll exportiert.

Mit dieser Methode können Sie befehle im Kontextmenü eines Ordners ausführen oder in der Registrierung gespeichert werden.

Wenn *lpOperation* NULL **ist,** öffnet die Funktion die durch lpFile angegebene *Datei.* Wenn *lpOperation* "open" oder "explore" ist, versucht die Funktion, den Ordner zu öffnen oder zu untersuchen.

Um Informationen über die Anwendung zu erhalten, die als Ergebnis des Aufrufs von **WOWShellExecute gestartet** wird, verwenden Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> Die **Einstellung Ordner starten in einem separaten Prozess** unter Ordneroptionen wirkt sich auf **WOWShellExecute aus.** Wenn diese Option deaktiviert ist (Standardeinstellung), verwendet **WOWShellExecute** ein geöffnetes Explorer-Fenster, anstatt ein neues zu starten. Wenn kein Explorer-Fenster geöffnet ist, **startet WOWShellExecute** ein neues.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
