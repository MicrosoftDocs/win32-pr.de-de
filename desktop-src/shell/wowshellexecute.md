---
description: Führt einen Vorgang für eine angegebene Datei aus.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Wowshellexecute-Funktion
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
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368281"
---
# <a name="wowshellexecute-function"></a>Wowshellexecute-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Führt einen Vorgang für eine angegebene Datei aus. **Wowshellexecute** ist nur für die Verwendung mit dem Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe) vorhanden, mit dem Betriebssystem-und 16-Bit-Software auf einem Windows-System ausgeführt werden kann und von keinem anderen Benutzer verwendet werden darf. Verwenden Sie stattdessen [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

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

*HWND* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das Besitzer Fenster, das für die Anzeige einer Benutzeroberfläche oder von Fehlermeldungen verwendet wird. Dieser Wert kann **null** sein, wenn der Vorgang keinem Fenster zugeordnet ist.

</dd> <dt>

*lpoperation* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf eine mit **null** endende Zeichenfolge, die in diesem Fall als *Verb* bezeichnet wird und die auszuführende Aktion angibt. Der Satz der verfügbaren Verben hängt von der jeweiligen Datei bzw. dem Ordner ab. Im Allgemeinen sind die im Kontextmenü eines Objekts verfügbaren Aktionen verfügbare Verben. Weitere Informationen zu Verben und deren Verfügbarkeit finden Sie im Abschnitt *Objekt Verben* unter [Starten von Anwendungen](launch.md). Weitere Erörterung von Kontextmenüs finden Sie unter Erweitern von Kontext [Menüs](context.md) . Die folgenden Verben werden häufig verwendet.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**Bearbeiten**


</dt> <dd>

Öffnet einen Editor und öffnet das Dokument zum Bearbeiten. Wenn *lpfile* keine Dokument Datei ist, tritt bei der Funktion ein Fehler auf.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**Entdecken**


</dt> <dd>

Untersucht den von *lpfile* angegebenen Ordner.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**sich**


</dt> <dd>

Initiiert eine Suche beginnend mit dem angegebenen Verzeichnis.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**eren**


</dt> <dd>

Öffnet die Datei, die durch den *lpfile* -Parameter angegeben wird. Bei der Datei kann es sich um eine ausführbare Datei, eine Dokument Datei oder einen Ordner handeln.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**gedruck**


</dt> <dd>

Druckt die von *lpfile* angegebene Dokument Datei. Wenn *lpfile* keine Dokument Datei ist, tritt bei der Funktion ein Fehler auf.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**Normal**


</dt> <dd>

Für Systeme vor Windows 2000 wird das Standardverb verwendet, wenn es gültig und in der Registrierung verfügbar ist. Wenn dies nicht der Wert ist, wird das Verb "Öffnen" verwendet.

Für Windows 2000-Systeme und spätere Systeme wird das Standardverb verwendet, falls verfügbar. Wenn dies nicht der Wert ist, wird das Verb "Öffnen" verwendet. Wenn keines der beiden Verb verfügbar ist, verwendet das System das erste Verb, das in der Registrierung aufgeführt ist.

</dd> </dl> </dd> <dt>

*lpfile* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die die Datei oder das Objekt angibt, für das das angegebene Verb ausgeführt werden soll. Übergeben Sie zum Angeben eines Shell-Namespace Objekts den voll qualifizierten Namen der Analyse. Beachten Sie, dass nicht alle Verben für alle Objekte unterstützt werden. Beispielsweise unterstützen nicht alle Dokumenttypen das Verb "Drucken".

</dd> <dt>

*lpparameters* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Wenn der *lpfile* -Parameter eine ausführbare Datei angibt, ist *lpparameters* ein Zeiger auf eine auf **null** endende Zeichenfolge, die die Parameter angibt, die an die Anwendung übergeben werden sollen. Das Format dieser Zeichenfolge wird durch das Verb bestimmt, das aufgerufen werden soll. Wenn die *lpfile-Datei* eine Dokument Datei angibt, sollten *lpparameters* **null** sein.

</dd> <dt>

*lpdirectory* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die das Standardverzeichnis angibt.

</dd> <dt>

*nshowcmd* \[ in\]
</dt> <dd>

Typ: **int**

Die Flags, die angeben, wie eine Anwendung beim Öffnen angezeigt werden soll. Wenn *lpfile* eine Dokument Datei angibt, wird das Flag einfach an die zugehörige Anwendung übergeben. Es liegt an der Anwendung, zu entscheiden, wie Sie behandelt werden soll. Dabei kann es sich um einen beliebigen Wert handeln, der im *nCmdShow* -Parameter für die [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion angegeben werden kann.

</dd> <dt>

*lpfncbwinexec* 
</dt> <dd>

Typ: **void \***

Rückruffunktion, die verwendet wird, um " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " im 16-Bit-Kernel aufzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HINSTANCE**

Gibt einen Wert zurück, der größer als 32 ist, wenn erfolgreich, oder einen Fehlerwert, der kleiner oder gleich 32 ist, andernfalls. In der folgenden Tabelle sind die Fehler Werte aufgeführt. Der Rückgabewert wird als HINSTANCE für die Abwärtskompatibilität mit 16-Bit-Windows-Anwendungen umgewandelt. Es handelt sich jedoch nicht um eine echte HINSTANCE. Das einzige, was mit der zurückgegebenen HINSTANCE erreicht werden kann, ist die Umwandlung in einen **int** -Wert und das Vergleichen mit dem Wert 32 oder einem der unten angegebenen Fehlercodes.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | Das Betriebssystem verfügt nicht über genügend Arbeitsspeicher oder Ressourcen.<br/>                                                                                                           |
| <dl> <dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt> </dl>  | Die angegebene Datei wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**der Fehler \_ Pfad wurde \_ nicht \_ gefunden.**</dt> </dl>  | Der angegebene Pfad wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**fehlerhaftes \_ \_ Format**</dt> </dl>       | Die exe-Datei ist ungültig (keine Win32. exe-Datei oder Fehler im exe-Image).<br/>                                                                                             |
| <dl> <dt>**SE \_ Err \_ AccessDenied**</dt> </dl>    | Das Betriebssystem hat den Zugriff auf die angegebene Datei verweigert.<br/>                                                                                                     |
| <dl> <dt>**SE \_ Err \_ associncomplete**</dt> </dl> | Die Dateinamen Zuordnung ist unvollständig oder ungültig.<br/>                                                                                                           |
| <dl> <dt>**SE \_ Err \_ DDE ausgelastet**</dt> </dl>         | Die DDE-Transaktion konnte nicht abgeschlossen werden, da andere DDE-Transaktionen verarbeitet wurden.<br/>                                                               |
| <dl> <dt>**SE \_ Err \_ dmissfail**</dt> </dl>         | Fehler bei DDE-Transaktion.<br/>                                                                                                                                   |
| <dl> <dt>**SE \_ Err \_ ddetimeout**</dt> </dl>      | Die DDE-Transaktion konnte nicht abgeschlossen werden, da die Anforderung abgelaufen ist.<br/>                                                                                     |
| <dl> <dt>**SE \_ Err \_ dllnotfound**</dt> </dl>     | Die angegebene DLL wurde nicht gefunden.<br/>                                                                                                                              |
| <dl> <dt>**SE \_ Err \_ FNF**</dt> </dl>             | Die angegebene Datei wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**SE \_ Err \_ noassoc**</dt> </dl>         | Der angegebenen Dateinamenerweiterung ist keine Anwendung zugeordnet. Dieser Fehler wird auch zurückgegeben, wenn Sie versuchen, eine nicht druckbare Datei zu drucken.<br/> |
| <dl> <dt>**SE \_ Err \_ OOM**</dt> </dl>             | Es war nicht genügend Arbeitsspeicher vorhanden, um den Vorgang abzuschließen.<br/>                                                                                                        |
| <dl> <dt>**SE \_ Err \_ PNF**</dt> </dl>             | Der angegebene Pfad wurde nicht gefunden.<br/>                                                                                                                             |
| <dl> <dt>**SE \_ Err- \_ Freigabe**</dt> </dl>           | Eine Freigabe Verletzung ist aufgetreten.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

**Wowshellexecute** ist nicht in einer Header-oder LIB-Datei enthalten. Sie wird aus Shell32.dll nach Namen exportiert.

Mit dieser Methode können Sie beliebige Befehle im Kontextmenü eines Ordners ausführen oder in der Registrierung speichern.

Wenn *lpoperation* den Wert **null** hat, öffnet die Funktion die von *lpfile* angegebene Datei. Wenn *lpoperation* "Open" oder "Explore" ist, versucht die Funktion, den Ordner zu öffnen oder zu durchsuchen.

Zum Abrufen von Informationen über die Anwendung, die als Ergebnis des Aufrufs von **wowshellexecute** gestartet wird, verwenden Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> Die Einstellung **Ordner Fenster in einem separaten Prozess** in Ordneroptionen starten wirkt sich auf **wowshellexecute** aus. Wenn diese Option deaktiviert ist (Standardeinstellung), verwendet **wowshellexecute** ein geöffnetes Explorer-Fenster, anstatt ein neues zu starten. Wenn kein Explorer-Fenster geöffnet ist, wird von **wowshellexecute** ein neues gestartet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
