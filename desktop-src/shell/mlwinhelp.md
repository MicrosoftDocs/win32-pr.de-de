---
description: Startet die Windows-Hilfe (Winhelp.exe) und übergibt zusätzliche Daten, mit denen die Art der von der Anwendung angeforderten Hilfe angegeben wird.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: Mlwinhelp-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLWinHelp
- MLWinHelpA
- MLWinHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: badfeb599fd24fd255eb064bbaf6d99a3b758bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977888"
---
# <a name="mlwinhelp-function"></a>Mlwinhelp-Funktion

\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Startet die Windows-Hilfe (Winhelp.exe) und übergibt zusätzliche Daten, mit denen die Art der von der Anwendung angeforderten Hilfe angegeben wird.

## <a name="syntax"></a>Syntax


```C++
BOOL MLWinHelp(
  _In_ HWND      hWndMain,
  _In_ LPCTSTR   lpszHelp,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndmain* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das Fenster, das die Hilfe anfordert. Die **mlwinhelp** -Funktion verwendet dieses Handle, um nachzuverfolgen, welche Anwendungen die Hilfe angefordert haben. Wenn der *ucommand* -Parameter Hilfe \_ Kontextmenü oder Hilfe \_ WM- \_ Hilfe angibt, identifiziert *hwndmain* das Steuerelement, das die Hilfe anfordert.

</dd> <dt>

*lpszhelp* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Die Adresse einer auf NULL endenden Zeichenfolge, die den Pfad enthält, falls erforderlich, und den Namen der Hilfedatei, die von **mlwinhelp** angezeigt werden soll.

Auf den Dateinamen kann eine Spitze Klammer (>) und der Name eines sekundären Fensters folgen, wenn das Thema in einem sekundären Fenster anstelle des primären Fensters angezeigt werden soll. Sie müssen den Namen des sekundären Fensters im Windows- \[ \] Abschnitt der Hilfeprojekt Datei (. hpj) definieren.

</dd> <dt>

*ucommand* \[ in\]
</dt> <dd>

Typ: **uint**

Der Typ der angeforderten Hilfe. Eine Liste der möglichen Werte und deren Auswirkung auf den Wert, der im *dwdata* -Parameter zu platzieren ist, finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*dwdata* \[ in\]
</dt> <dd>

Typ: **DWORD \_ ptr**

Weitere Daten. Der verwendete Wert hängt vom Wert des *ucommand* -Parameters ab. Eine Liste der möglichen *dwdata* -Werte finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einer Header Datei enthalten und muss von Ordnungszahl 395 für **mlwinhelpa** und 397 für **mlwinhelpw** aufgerufen werden.

**Mlwinhelp** ist im Grunde ein Wrapper für [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Es wird versucht, den Pfad zur Hilfedatei abzurufen, die der aktuellen Einstellung der Benutzeroberflächen Sprache entspricht, bevor **WinHelp** aufgerufen wird. Wenn Sie erfolgreich ist, übergibt Sie diesen Pfad. Wenn ein Fehler auftritt, übergibt er den Pfad, auf den von *lpszhelp* verwiesen wird.

Diese Funktion schlägt fehl, wenn Sie von einem beliebigen Kontext, aber vom aktuellen Benutzer aufgerufen wird.

Vor dem Schließen des Fensters, das die Hilfe angefordert hat, muss die Anwendung **mlwinhelp** aufrufen, wobei der *ucommand* -Parameter zum Beenden der Hilfe festgelegt ist \_ . Bis alle Anwendungen diesen Vorgang abgeschlossen haben, wird die Windows-Hilfe nicht beendet. Beachten Sie, dass das Aufrufen der Windows-Hilfe mit dem \_ Befehl Hilfe Quit nicht erforderlich ist, wenn Sie die Windows-Hilfe mithilfe des \_ Befehls Help contextpopup gestartet haben.

In der folgenden Tabelle werden die möglichen Werte für den *ucommand* -Parameter und die entsprechenden Formate des *dwdata* -Parameters angezeigt.



| *ucommand*          | Action                                                                                                                                                                                                                                                               | *dwdata*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hilfe \_ Befehl       | Führt ein Hilfe Makro oder eine Makro Zeichenfolge aus.                                                                                                                                                                                                                               | Die Adresse einer Zeichenfolge, die den Namen der zu testenden Hilfe Makros angibt. Wenn die Zeichenfolge mehrere Makronamen angibt, müssen die Namen durch Semikolons getrennt werden. Sie müssen für einige Makros die Kurzform des Makro namens verwenden, da der lange Name von der Windows-Hilfe nicht unterstützt wird.                         |
| Hilfe \_ Inhalte      | Zeigt das von der Option Inhalt angegebene Thema im \[ Abschnitt Optionen \] der HPJ-Datei an. Dieser Befehl dient der Abwärtskompatibilität. Neue Anwendungen sollten eine CNT-Datei bereitstellen und den Help \_ Finder-Befehl verwenden.                                           | Erten Legen Sie auf 0 fest.                                                                                                                                                                                                                                                                                           |
| Hilfe \_ Kontext       | Zeigt das Thema an, das durch den angegebenen Kontext Bezeichner identifiziert wird, der im \[ Karten \] Abschnitt der HPJ-Datei definiert ist.                                                                                                                                                   | Enthält den Kontext Bezeichner für das Thema.                                                                                                                                                                                                                                                               |
| Hilfe ( \_ Kontextmenü)   | Zeigt das Menü **Hilfe** für das ausgewählte Fenster an und zeigt das Thema für das ausgewählte Steuerelement in einem Popup Fenster an.                                                                                                                                             | Die Adresse eines Arrays von **DWORD** -Paaren. Das erste **DWORD** in jedem Paar ist der Steuerelement Bezeichner, der zweite ist der Kontext Bezeichner für das Thema. Das Array muss durch ein paar Nullen beendet werden {0,0} . Wenn Sie einem bestimmten Steuerelement keine Hilfe hinzufügen möchten, legen Sie seinen Kontext Bezeichner auf-1 fest. |
| Hilfe \_ contextpopup  | Zeigt das Thema an, das durch den angegebenen Kontext Bezeichner identifiziert wird, der im \[ Karten \] Abschnitt der HPJ-Datei in einem Popup Fenster definiert ist.                                                                                                                                | Enthält den Kontext Bezeichner für ein Thema.                                                                                                                                                                                                                                                                 |
| Hilfe- \_ Finder        | Zeigt das Dialogfeld **Hilfe Themen** an.                                                                                                                                                                                                                             | Erten Legen Sie auf 0 fest.                                                                                                                                                                                                                                                                                           |
| Hilfe für \_ forcefile     | Stellt sicher, dass in der Windows-Hilfe die richtige Hilfedatei angezeigt wird. Wenn die falsche Hilfedatei angezeigt wird, öffnet die Windows-Hilfe die richtige. Andernfalls gibt es keine Aktion.                                                                                     | Erten Legen Sie auf 0 fest.                                                                                                                                                                                                                                                                                           |
| Hilfe \_ helponhelp    | Zeigt Hilfe zur Verwendung der Windows-Hilfe an, wenn die WinHlp32. HLP-Datei verfügbar ist.                                                                                                                                                                                     | Erten Legen Sie auf 0 fest.                                                                                                                                                                                                                                                                                           |
| Hilfe \_ Index         | Zeigt das von der Option Inhalt angegebene Thema im \[ Abschnitt Optionen \] der HPJ-Datei an. Dieser Befehl dient der Abwärtskompatibilität. Neue Anwendungen sollten den Help \_ Finder-Befehl verwenden.                                                                   | Erten Legen Sie auf 0 fest.                                                                                                                                                                                                                                                                                           |
| Hilfe \_ Taste           | Zeigt das Thema in der Schlüsselwort Tabelle an, das dem angegebenen Schlüsselwort entspricht, wenn eine genaue Übereinstimmung vorliegt. Wenn mehrere Übereinstimmungen vorhanden sind, wird der Index mit den Themen angezeigt, die im Listenfeld **Themen gefunden** werden.                                                 | Adresse einer Schlüsselwort Zeichenfolge. Mehrere Schlüsselwörter müssen durch Semikolons getrennt werden.                                                                                                                                                                                                                              |
| Hilfe- \_ multikey      | Zeigt das Thema an, das durch ein Schlüsselwort in einer alternativen Schlüsselwort Tabelle angegeben wird.                                                                                                                                                                                           | Adresse einer [**multikeyhelp**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) -Struktur, die ein Tabellen fußnotiz-Zeichen und ein Schlüsselwort angibt.                                                                                                                                                                                     |
| Hilfe \_ partialkey    | Zeigt das Thema in der Schlüsselwort Tabelle an, das dem angegebenen Schlüsselwort entspricht, wenn eine genaue Übereinstimmung vorliegt. Wenn mehrere Übereinstimmungen vorhanden sind, wird das Dialogfeld **gefundene Themen** angezeigt. Um den Index ohne Übergabe eines Schlüssel Worts anzuzeigen, verwenden Sie einen Zeiger auf eine leere Zeichenfolge. | Adresse einer Schlüsselwort Zeichenfolge. Mehrere Schlüsselwörter müssen durch Semikolons getrennt werden.                                                                                                                                                                                                                              |
| Hilfe \_ Beenden          | Teilt der Windows-Hilfe mit, dass Sie nicht mehr benötigt wird. Wenn keine anderen Anwendungen nach Hilfe gefragt wurden, schließt Windows die Windows-Hilfe.                                                                                                                                         | Erten Legen Sie auf 0 fest.                                                                                                                                                                                                                                                                                           |
| Hilfe \_ setContent   | Gibt das Inhalts Thema an. In der Windows-Hilfe wird dieses Thema angezeigt, wenn der Benutzer auf die Schaltfläche **Inhalt** klickt, wenn der Hilfedatei keine CNT-Datei zugeordnet ist.                                                                                                  | Enthält den Kontext Bezeichner für das Inhalts Thema.                                                                                                                                                                                                                                                      |
| Hilfe \_ setpopup Torys \_ | Legt die Position des nachfolgenden Popup Fensters fest.                                                                                                                                                                                                                   | Enthält die Positionsdaten. Verwenden Sie das [**makelong**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) -Makro, um die horizontalen und vertikalen Koordinaten zu einem einzelnen Wert zu verketten. Das Popup Fenster wird so positioniert, als ob sich der Mauszeiger am angegebenen Punkt befand, als das Popup Fenster aufgerufen wurde.                                 |
| Hilfe- \_ setwinpos     | Zeigt das Windows-Hilfefenster an, wenn es minimiert ist oder im Arbeitsspeicher vorhanden ist, und legt seine Größe und Position wie angegeben fest.                                                                                                                                                      | Die Adresse einer [**helpwininfo**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) -Struktur, die die Größe und Position eines primären oder sekundären Hilfe Fensters angibt.                                                                                                                                                             |
| Hilfe- \_ TCard         | Gibt an, dass ein Befehl für eine Schulungs Karten Instanz der Windows-Hilfe ist. Kombinieren Sie diesen Befehl mit anderen Befehlen, indem Sie den bitweisen OR-Operator verwenden.                                                                                                                    | Hängt von dem Befehl ab, mit dem dieser Befehl kombiniert wird.                                                                                                                                                                                                                                                  |
| Hilfe \_ WM- \_ Hilfe      | Zeigt das Thema für das Steuerelement an, das durch den *hwndmain* -Parameter in einem Popup Fenster identifiziert wird.                                                                                                                                                                        | Die Adresse eines Arrays von **DWORD** -Paaren. Das erste **DWORD** in jedem Paar ist ein Steuerelement Bezeichner, und der zweite ist ein Kontext Bezeichner für ein Thema. Das Array muss durch ein paar Nullen beendet werden {0,0} . Wenn Sie einem bestimmten Steuerelement keine Hilfe hinzufügen möchten, legen Sie seinen Kontext Bezeichner auf-1 fest.       |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Mlwinhelpw** (Unicode) und **mlwinhelpa** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Helpwininfo**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**Multikeyhelp**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
