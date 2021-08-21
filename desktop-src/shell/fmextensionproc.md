---
description: Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, um mit einer Datei-Manager-Erweiterung zu kommunizieren.
title: FMExtensionProc-Rückruffunktion (Wfext.h)
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
ms.openlocfilehash: 7cd13fe534f3bb121a4056f67ceff47ddfa71fa5506c2020a243ab340768ce35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032658"
---
# <a name="fmextensionproc-callback-function"></a>FMExtensionProc-Rückruffunktion

Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, um mit einer Datei-Manager-Erweiterung zu kommunizieren.

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

*Hwnd* 
</dt> <dd>

Typ: **HWND**

Ein Fensterhandle für den Datei-Manager. Eine Erweiterung verwendet dieses Handle, um das übergeordnete Fenster für jedes Dialogfeld oder Meldungsfeld anzugeben, das angezeigt werden muss, und um Abfragemeldungen an den Datei-Manager zu senden.

</dd> <dt>

*wMsg* 
</dt> <dd>

Typ: **WORD**

Eine der folgenden Datei-Manager-Meldungen.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 bis 99**


</dt> <dd>

Der Benutzer hat im durch die Erweiterung bereitgestellten Menü ein Element ausgewählt. Der Wert ist der Bezeichner des ausgewählten Menüelements.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

Der Benutzer hat F1 gedrückt, während er ein Erweiterungsmenü oder ein Symbolleistenbefehlselement ausgewählt hat. Gibt an, dass die Erweiterung **WinHelp** entsprechend für das Befehlselement aufrufen soll.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**


</dt> <dd>

Der Benutzer hat ein Erweiterungsmenü oder ein Symbolleistenbefehlselement ausgewählt. Gibt an, dass die Erweiterung eine Hilfezeichenfolge bereitstellen soll.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

Der Benutzer hat das Menü der Erweiterung ausgewählt. Die Erweiterung sollte Elemente im Menü initialisieren.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**


</dt> <dd>

Der Datei-Manager lädt die Erweiterungs-DLL und fordert die DLL zur Eingabe von Informationen über das von der DLL bereitgestellte Menü auf.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

Die Auswahl im **Datei-Manager-Verzeichnisfenster** oder im Fenster **Suchergebnisse** wurde geändert.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

Der Datei-Manager erstellt die Symbolleiste und fordert die Erweiterungs-DLL zur Eingabe von Informationen zu allen Schaltflächen auf, die die DLL der Symbolleiste hinzufügt.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**


</dt> <dd>

Der Datei-Manager entlädt die Erweiterungs-DLL.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_FMEVENT-BENUTZERAKTUALISIERUNG \_**


</dt> <dd>

Der Benutzer hat im Menü **Fenster** den Befehl **Aktualisieren** ausgewählt. Die Erweiterung sollte bei Bedarf Elemente im Menü aktualisieren.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Typ: **LONG**

Nachrichtenspezifischer Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LONG**

Gibt einen Wert *zurück,* der von der wMsg-Parametermeldung abhängig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




