---
description: Startet Windows Hilfe (Winhelp.exe) und übergibt zusätzliche Daten, die die Art der von der Anwendung angeforderten Hilfe angibt.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: MLWinHelp-Funktion
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
ms.openlocfilehash: a6c109f39107ba3cfd1800cca8db516d0033a2f3c32b9784e4359b3c6c50655d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968899"
---
# <a name="mlwinhelp-function"></a>MLWinHelp-Funktion

\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Startet Windows Hilfe (Winhelp.exe) und übergibt zusätzliche Daten, die die Art der von der Anwendung angeforderten Hilfe angibt.

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

*hWndMain* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das Fenster, das Hilfe an fordert. Die **MLWinHelp-Funktion** verwendet dieses Handle, um zu verfolgen, welche Anwendungen Hilfe angefordert haben. Wenn der *uCommand-Parameter* HELP CONTEXTMENU oder HELP WM HELP angibt, identifiziert \_ \_ \_ *hWndMain* das Steuerelement, das Hilfe angibt.

</dd> <dt>

*lpszHelp* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Die Adresse einer auf NULL beendeten Zeichenfolge, die bei Bedarf den Pfad und den Namen der Hilfedatei enthält, die **MLWinHelp** anzeigen soll.

Auf den Dateinamen kann eine eckige Klammer (>) und der Name eines sekundären Fensters folgen, wenn das Thema in einem sekundären Fenster und nicht im primären Fenster angezeigt werden soll. Sie müssen den Namen des sekundären Fensters im Windows-Abschnitt der Hilfeprojektdatei \[ \] (.hpj) definieren.

</dd> <dt>

*uCommand* \[ In\]
</dt> <dd>

Typ: **UINT**

Der Angeforderte Hilfetyp. Eine Liste der möglichen Werte und deren Auswirkungen auf den Wert, der im *dwData-Parameter* gespeichert werden soll, finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*dwData* \[ In\]
</dt> <dd>

Typ: **DWORD \_ PTR**

Zusätzliche Daten. Der verwendete Wert hängt vom Wert des *uCommand-Parameters* ab. Eine Liste der möglichen *dwData-Werte* finden Sie im Abschnitt Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einer Headerdatei enthalten und muss mit der Ordnungszahl 395 für **MLWinHelpA** und 397 für **MLWinHelpW aufgerufen werden.**

**MLWinHelp** ist im Wesentlichen ein Wrapper für [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Es wird versucht, den Pfad zur Hilfedatei zu erhalten, die der aktuellen Einstellung der Benutzeroberflächensprache entspricht, bevor **WinHelp aufruft.** Wenn dies erfolgreich ist, wird dieser Pfad übergibt. Wenn ein Fehler auftritt, wird der Pfad übergibt, auf den *lpszHelp zeigt.*

Diese Funktion schlägt fehl, wenn sie aus einem beliebigen Kontext aufgerufen wird, jedoch vom aktuellen Benutzer.

Vor dem Schließen des Fensters, in dem Hilfe angefordert wurde, muss die Anwendung **MLWinHelp** aufrufen, und der *uCommand-Parameter* muss auf HELP \_ QUIT festgelegt sein. Bis alle Anwendungen dies getan haben, Windows die Hilfe nicht beendet. Beachten Sie, dass Windows Hilfe mit dem Befehl HELP QUIT nicht erforderlich ist, wenn Sie den \_ Befehl HELP CONTEXTPOPUP verwendet haben, um die Windows \_ starten.

Die folgende Tabelle zeigt die möglichen Werte für den *uCommand-Parameter* und die entsprechenden Formate des *dwData-Parameters.*



| *uCommand*          | Aktion                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_HELP-BEFEHL       | Führt ein Hilfemakro oder eine Makrozeichenfolge aus.                                                                                                                                                                                                                               | Adresse einer Zeichenfolge, die den Namen der ausgeführten Hilfemakros angibt. Wenn die Zeichenfolge mehrere Makronamen angibt, müssen die Namen durch Semikolons getrennt werden. Sie müssen die Kurzform des Makronamens für einige Makros verwenden, da Windows Hilfe den langen Namen nicht unterstützt.                         |
| \_HILFEINHALTE      | Zeigt das thema an, das durch die Option Inhalt im \[ Abschnitt OPTIONS \] der HPJ-Datei angegeben wird. Dieser Befehl ist aus Gründen der Abwärtskompatibilität. Neue Anwendungen sollten eine CNT-Datei bereitstellen und den Befehl HELP \_ FINDER verwenden.                                           | Ignoriert; auf 0 festgelegt.                                                                                                                                                                                                                                                                                           |
| \_HILFEKONTEXT       | Zeigt das Thema an, das durch den angegebenen Kontextbezeichner identifiziert wird, der im \[ \] MAP-Abschnitt der HPJ-Datei definiert ist.                                                                                                                                                   | Enthält den Kontextbezeichner für das Thema.                                                                                                                                                                                                                                                               |
| \_HILFEKONTEXTMENÜ   | Zeigt das **Menü Hilfe** für das ausgewählte Fenster an und zeigt dann das Thema für das ausgewählte Steuerelement in einem Popupfenster an.                                                                                                                                             | Adresse eines Arrays von **DWORD-Paaren.** Das erste **DWORD** in jedem Paar ist der Steuerelementbezeichner, und das zweite ist der Kontextbezeichner für das Thema. Das Array muss durch ein Paar von Nullen beendet {0,0} werden. Wenn Sie einem bestimmten Steuerelement keine Hilfe hinzufügen möchten, legen Sie dessen Kontextbezeichner auf -1 fest. |
| \_HILFEKONTEXTPOPUP  | Zeigt das Thema an, das durch den angegebenen Kontextbezeichner identifiziert wird, der im \[ MAP-Abschnitt \] der HPJ-Datei in einem Popupfenster definiert ist.                                                                                                                                | Enthält den Kontextbezeichner für ein Thema.                                                                                                                                                                                                                                                                 |
| \_HILFE-FINDER        | Zeigt das **Dialogfeld Hilfethemen** an.                                                                                                                                                                                                                             | Ignoriert; auf 0 festgelegt.                                                                                                                                                                                                                                                                                           |
| HELP \_ FORCEFILE     | Stellt sicher Windows dass in der Hilfe die richtige Hilfedatei angezeigt wird. Wenn die falsche Hilfedatei angezeigt wird, wird Windows Hilfe die richtige geöffnet. Andernfalls gibt es keine Aktion.                                                                                     | Ignoriert; auf 0 festgelegt.                                                                                                                                                                                                                                                                                           |
| HELP \_ HELPONHELP    | Zeigt Hilfe zur Verwendung von Windows Hilfe an, wenn die Datei Winhlp32.hlp verfügbar ist.                                                                                                                                                                                     | Ignoriert; auf 0 festgelegt.                                                                                                                                                                                                                                                                                           |
| HELP \_ INDEX         | Zeigt das thema an, das durch die Option Inhalt im \[ Abschnitt OPTIONS \] der HPJ-Datei angegeben wird. Dieser Befehl ist aus Gründen der Abwärtskompatibilität. Neue Anwendungen sollten den Befehl HELP \_ FINDER verwenden.                                                                   | Ignoriert; auf 0 festgelegt.                                                                                                                                                                                                                                                                                           |
| \_HILFESCHLÜSSEL           | Zeigt das Thema in der Schlüsselworttabelle an, das dem angegebenen Schlüsselwort entspricht, wenn eine genaue Übereinstimmung vor liegt. Wenn mehrere Übereinstimmungen gefunden werden, wird der Index mit den Themen angezeigt, die im **Listenfeld Themen gefunden** aufgeführt sind.                                                 | Adresse einer Schlüsselwortzeichenfolge. Mehrere Schlüsselwörter müssen durch Semikolons getrennt werden.                                                                                                                                                                                                                              |
| HELP \_ MULTIKEY      | Zeigt das durch ein Schlüsselwort angegebene Thema in einer alternativen Schlüsselworttabelle an.                                                                                                                                                                                           | Adresse einer [**MULTIKEYHELP-Struktur,**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) die ein Tabellennotezeichen und ein Schlüsselwort angibt.                                                                                                                                                                                     |
| HELP \_ PARTIALKEY    | Zeigt das Thema in der Schlüsselworttabelle an, das dem angegebenen Schlüsselwort entspricht, wenn eine genaue Übereinstimmung vor liegt. Wenn mehrere Übereinstimmungen gefunden wurden, wird das **Dialogfeld Themen gefunden** angezeigt. Um den Index anzuzeigen, ohne ein Schlüsselwort zu übergeben, verwenden Sie einen Zeiger auf eine leere Zeichenfolge. | Adresse einer Schlüsselwortzeichenfolge. Mehrere Schlüsselwörter müssen durch Semikolons getrennt werden.                                                                                                                                                                                                                              |
| HELP \_ QUIT          | Informiert Windows Hilfe darüber, dass sie nicht mehr benötigt wird. Wenn keine anderen Anwendungen um Hilfe gebeten haben, Windows sie Windows Hilfe.                                                                                                                                         | Ignoriert; auf 0 festgelegt.                                                                                                                                                                                                                                                                                           |
| HELP \_ SETCONTENTS   | Gibt das Thema Inhalt an. Windows In der Hilfe wird dieses Thema angezeigt, wenn der Benutzer auf die Schaltfläche **Inhalt** klickt, wenn der Hilfedatei keine CNT-Datei zugeordnet ist.                                                                                                  | Enthält den Kontextbezeichner für das Thema Inhalt.                                                                                                                                                                                                                                                      |
| HELP \_ SETPOPUP \_ POS | Legt die Position des nachfolgenden Popupfensters fest.                                                                                                                                                                                                                   | Enthält die Positionsdaten. Verwenden Sie das [**MAKELONG-Makro,**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) um die horizontalen und vertikalen Koordinaten zu einem einzelnen Wert zu verketten. Das Popupfenster wird so positioniert, als ob sich der Mauszeiger an dem angegebenen Punkt befand, an dem das Popupfenster aufgerufen wurde.                                 |
| HELP \_ SETWINPOS     | Zeigt das Windows Hilfefenster an, wenn es minimiert oder im Arbeitsspeicher ist, und legt dessen Größe und Position wie angegeben fest.                                                                                                                                                      | Adresse einer [**HELPWININFO-Struktur,**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) die die Größe und Position eines primären oder sekundären Hilfefensters angibt.                                                                                                                                                             |
| \_HILFE-TCARD         | Gibt an, dass ein Befehl für eine Trainingskarteninstanz von Windows Hilfe vorgesehen ist. Kombinieren Sie diesen Befehl mit anderen Befehlen, indem Sie den bitweisen OR-Operator verwenden.                                                                                                                    | Hängt vom Befehl ab, mit dem dieser Befehl kombiniert wird.                                                                                                                                                                                                                                                  |
| HILFE \_ \_ WM-HILFE      | Zeigt das Thema für das Steuerelement an, das durch den *hWndMain-Parameter* in einem Popupfenster identifiziert wird.                                                                                                                                                                        | Adresse eines Arrays von **DWORD-Paaren.** Das erste **DWORD** in jedem Paar ist ein Steuerelementbezeichner, und das zweite ist ein Kontextbezeichner für ein Thema. Das Array muss durch ein Paar von Nullen beendet {0,0} werden. Wenn Sie einem bestimmten Steuerelement keine Hilfe hinzufügen möchten, legen Sie dessen Kontextbezeichner auf -1 fest.       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **MLWinHelpW** (Unicode) und **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
