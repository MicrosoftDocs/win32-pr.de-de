---
description: Zeigt ein Hilfefenster an, das der aktuellen Einstellung der Benutzeroberflächensprache entspricht.
title: MLHtmlHelp-Funktion
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
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841211"
---
# <a name="mlhtmlhelp-function"></a>MLHtmlHelp-Funktion

\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]

Zeigt ein Hilfefenster an, das der aktuellen Einstellung der Benutzeroberflächensprache entspricht.

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

*hwndCaller* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das übergeordnete Fenster, das diese Funktion aufruft.

</dd> <dt>

*pszFile* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf einen Puffer, der den vollqualifizierten Pfad einer kompilierten Hilfedatei (.chm) oder eine Themendatei in einer angegebenen Hilfedatei enthält.

</dd> <dt>

*uCommand* \[ In\]
</dt> <dd>

Typ: **UINT**

Der auszuführende Befehl. Diese Funktion unterstützt nur [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) und [HH \_ DISPLAY TEXT \_ \_ POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command)direkt. Bei einem anderen Befehl wird der Aufruf ohne den *dwCrossCodePage-Wert* an [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api)weitergeleitet.

</dd> <dt>

*dwData* \[ In\]
</dt> <dd>

Typ: **DWORD \_ PTR**

Alle daten, die erforderlich sein können, basierend auf dem Wert des *uCommand-Parameters.*

</dd> <dt>

*dwCrossCodePage* \[ In\]
</dt> <dd>

Typ: **DWORD**

Der **DWORD-Wert,** der die Codepage der aktuellen Ui-Spracheinstellung angibt, z. B. CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HWND**

Abhängig vom angegebenen *uCommand* und dem Ergebnis gibt **MLHtmlHelp** eine oder beide der folgenden Punkte zurück:

-   Das Handle (hwnd) des Hilfefensters.
-   **NULL.** In einigen Fällen gibt **NULL einen** Fehler an. in anderen Fällen gibt **NULL** an, dass das Hilfefenster noch nicht erstellt wurde.

## <a name="remarks"></a>Hinweise

Wenn ein Problem mit dem Pfad der Hilfedatei für die aktuelle Sprache auftritt, wird der Aufruf zur Standardbehandlung an [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) weitergeleitet.

Wenn das Hilfefenster geschlossen ist, kehrt der Fokus zum Besitzer zurück, es sei denn, der Besitzer ist der Desktop. Wenn *hwndCaller* der Desktop ist, bestimmt das Betriebssystem, wo der Fokus zurückgegeben wird.

Wenn **MLHtmlHelp** darüber hinaus Benachrichtigungsmeldungen aus dem Hilfefenster sendet, werden die Nachrichten an [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) *hwndCaller* gesendet, solange Sie die Nachverfolgung von Benachrichtigungsmeldungen in der Hilfefensterdefinition aktiviert haben.

## <a name="examples"></a>Beispiele

Das folgende Beispiel ruft den [Befehl HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) auf, um die Hilfedatei mit dem Namen Help.chm zu öffnen und ihr Standardthema im Hilfefenster mit dem Namen `Mainwin` anzuzeigen. Im Allgemeinen ist das in diesem Befehl angegebene Hilfefenster ein standardmäßiger [HTML Help Viewer.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Legen Sie bei Verwendung dieser Funktion die Stapelgröße der ausführbaren Hostdatei auf mindestens 100.000 fest. Wenn die definierte Stapelgröße zu klein ist, wird der Thread, der zum Ausführen der HTML-Hilfe erstellt wurde, ebenfalls mit dieser Stapelgröße erstellt, und der Vorgang kann fehlschlagen. Optional können Sie /STACK aus der Linkbefehlszeile entfernen und auch alle STACK-Einstellungen in der DEF-Datei der ausführbaren Datei entfernen (in diesem Fall ist die Standardstapelgröße 1 MB). Sie können die Stapelgröße auch mit dem Compilerbefehl /Fnumber festlegen (der Compiler über gibt diese als /STACK an den Linker weiter).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **MLHtmlHelpW** (Unicode) und **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
