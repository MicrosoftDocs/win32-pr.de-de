---
description: Zeigt ein Hilfefenster an, das der aktuellen UI-Spracheinstellung entspricht.
title: Mlhtmlhelp-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993799"
---
# <a name="mlhtmlhelp-function"></a>Mlhtmlhelp-Funktion

\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Zeigt ein Hilfefenster an, das der aktuellen UI-Spracheinstellung entspricht.

## <a name="syntax"></a>Syntax


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndcaller* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das übergeordnete Fenster, das diese Funktion aufruft.

</dd> <dt>

*pszFile* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf einen Puffer, der den voll qualifizierten Pfad einer kompilierten Hilfedatei (. chm) oder eine themendatei in einer angegebenen Hilfedatei enthält.

</dd> <dt>

*ucommand* \[ in\]
</dt> <dd>

Typ: **uint**

Der Befehl, der ausgeführt werden soll. Diese Funktion unterstützt direkt nur das [HH- \_ Anzeige \_ Thema](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) und das [HH- \_ Anzeige \_ \_ TextPopup](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command). Bei einem beliebigen anderen Befehl wird der-Befehl ohne den *dwcrosscodepage* -Wert an [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api)weitergeleitet.

</dd> <dt>

*dwdata* \[ in\]
</dt> <dd>

Typ: **DWORD \_ ptr**

Alle Daten, die möglicherweise erforderlich sind, basierend auf dem Wert des *ucommand* -Parameters.

</dd> <dt>

*dwcrosscodepage* \[ in\]
</dt> <dd>

Typ: **DWORD**

Der **DWORD** -Wert, der die Codepage der aktuellen UI-Spracheinstellung angibt, z \_ . b. CP ACP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HWND**

Abhängig vom angegebenen *ucommand* und dem Ergebnis gibt **mlhtmlhelp** einen oder beide der folgenden zurück:

-   Das Handle (HWND) des Hilfe Fensters.
-   **Null**. In einigen Fällen weist **null** auf einen Fehler hin. in anderen Fällen gibt **null** an, dass das Hilfefenster noch nicht erstellt wurde.

## <a name="remarks"></a>Bemerkungen

Wenn ein Problem mit dem Pfad der Hilfedatei für die aktuelle Sprache auftritt, wird der-Befehl zur Standardbehandlung an [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) weitergeleitet.

Wenn das Hilfefenster geschlossen wird, wird der Fokus an den Besitzer zurückgegeben, es sei denn, der Besitzer ist der Desktop. Wenn *hwndcaller* der Desktop ist, bestimmt das Betriebssystem, wohin der Fokus zurückgegeben wird.

Wenn **mlhtmlhelp** Benachrichtigungs Meldungen aus dem Hilfefenster sendet, werden die Nachrichten außerdem an *hwndcaller* gesendet, solange Sie die Nachverfolgung von [Benachrichtigungs](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) Meldungen in der Hilfefenster Definition aktiviert haben.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der Befehl [HH \_ Display \_ Topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) aufgerufen, um die Hilfedatei mit dem Namen Help. chm zu öffnen und das Standardthema im Hilfefenster mit dem Namen anzuzeigen `Mainwin` . Im Allgemeinen handelt es sich bei dem in diesem Befehl angegebenen Hilfefenster um einen HTML-Standard [Hilfe Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Wenn Sie diese Funktion verwenden, legen Sie die Stapelgröße der ausführbaren Hostingdatei auf mindestens 100K fest. Wenn die definierte Stapelgröße zu klein ist, wird der zum Ausführen der HTML-Hilfe erstellte Thread ebenfalls mit dieser Stapelgröße erstellt, und der Vorgang kann fehlschlagen. Optional können Sie/Stack aus der Link Befehlszeile entfernen und auch beliebige Stapel Einstellungen in der DEF-Datei der ausführbaren Datei entfernen (in diesem Fall ist die Standard Stapelgröße 1 MB). Sie können auch die Stapelgröße mit dem/fnumber-Compilerbefehl festlegen (der Compiler übergibt dies als/Stack an den Linker).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Mlhtmlhelpw** (Unicode) und **mlhtmlhelpa** (ANSI)<br/>                                               |



 

 
