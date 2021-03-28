---
description: Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.
title: Funktion "f mextensionproc" (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993687"
---
# <a name="fmextensionproc-callback-function"></a>Funktion "f mextensionproc"

Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Typ: **HWND**

Ein Fenster Handle für den Datei-Manager. Eine Erweiterung verwendet dieses Handle, um das übergeordnete Fenster für ein beliebiges Dialogfeld oder Meldungs Feld anzugeben, das angezeigt werden muss, und zum Senden von Abfrage Nachrichten an den Datei-Manager.

</dd> <dt>

*wmsg* 
</dt> <dd>

Typ: **Word**

Eine der folgenden Datei-Manager-Meldungen.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 bis 99**


</dt> <dd>

Der Benutzer hat ein Element aus dem von der Erweiterung bereitgestellten Menü ausgewählt. Der Wert ist der Bezeichner des ausgewählten Menü Elements.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**"helpmenuitem" für "f" \_**


</dt> <dd>

Benutzer hat F1 gedrückt, während ein Erweiterungs Menü oder ein Symbolleisten-Befehls Element ausgewählt wurde. Gibt an, dass die Erweiterung **WinHelp** entsprechend für das Befehls Element aufruft.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**-HelpString für "f" \_**


</dt> <dd>

Der Benutzer hat ein Erweiterungs Menü oder ein Symbolleisten-Befehls Element ausgewählt. Gibt an, dass die Erweiterung eine Hilfe Zeichenfolge bereitstellen soll.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**Datei " \_ InitMenu"**


</dt> <dd>

Der Benutzer hat das Menü der Erweiterung ausgewählt. Die Erweiterung sollte Elemente im Menü initialisieren.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**Laden von "f" \_**


</dt> <dd>

Der Datei-Manager lädt die Erweiterungs-DLL und fordert die dll zur Eingabe von Informationen über das Menü an, das die dll bereitstellt.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**"schabvent \_ selChange"**


</dt> <dd>

Die Auswahl im Verzeichnis Fenster des **Datei-Managers** oder im Fenster " **Suchergebnisse** " wurde geändert.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**"Tool barload" von "f" \_**


</dt> <dd>

Der Datei-Manager erstellt die Symbolleiste und fordert die Erweiterungs-DLL zur Eingabe von Informationen über alle Schaltflächen auf, die die dll der Symbolleiste hinzufügt.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**Entladen von "f" \_**


</dt> <dd>

Die Erweiterungs-DLL wird vom Datei-Manager entladen.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_Benutzer Aktualisierung für "Benutzer" \_**


</dt> <dd>

Der Benutzer hat den Befehl " **Aktualisieren** " im Menü " **Fenster** " ausgewählt. Die Erweiterung sollte bei Bedarf Elemente im Menü aktualisieren.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Type: **Long**

Meldungs spezifischer Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: **Long**

Gibt einen Wert zurück, der von der *wmsg* -Parameter Nachricht abhängt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | " **F** " (Unicode)<br/>                                          |



 

 




