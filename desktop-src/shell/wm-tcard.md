---
description: Wird an eine Anwendung gesendet, die eine Schulungs Karte mit der Windows-Hilfe initiiert hat.
title: WM_TCARD Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215928"
---
# <a name="wm_tcard-message"></a>WM- \_ TCard-Nachricht

Wird an eine Anwendung gesendet, die eine Schulungs Karte mit der Windows-Hilfe initiiert hat. Die Meldung informiert die Anwendung, wenn der Benutzer auf eine Schaltfläche zum autorierbaren Klicken klickt. Eine Anwendung initiiert eine Schulungs Karte, indem Sie den Help \_ TCard-Befehl in einem aufzurufenden Befehl der [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion angibt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*idaction* 
</dt> <dd>

Ein-Wert, der die Aktion angibt, die der Benutzer ausgeführt hat. Dies kann einer der folgenden Werte sein:

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**Idabort**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare **Abbruch** Schaltfläche geklickt.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare Schaltfläche **Abbrechen** geklickt.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**Idclose**


</dt> <dd>

Der Benutzer hat die Schulungs Karte geschlossen.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

Der Benutzer hat auf eine autorisierte Windows- **Hilfe** Schaltfläche geklickt.

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare Schaltfläche **ignorieren** geklickt.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare Schaltfläche **OK** geklickt.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare **No** -Schaltfläche geklickt.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**Idretry**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare **Wiederholungs** Schaltfläche geklickt.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**Unterstützung von \_ TCard- \_ Daten**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare Schaltfläche geklickt. Der *dwaktiondata* -Parameter enthält eine lange Ganzzahl, die vom Hilfe Autor angegeben wird.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**Help \_ TCard \_ other \_ Caller**


</dt> <dd>

Eine andere Anwendung hat Trainingskarten angefordert.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**Idylle**


</dt> <dd>

Der Benutzer hat auf eine autorilier Bare **Ja** -Schaltfläche geklickt.

</dd> </dl> </dd> <dt>

*dwaktiondata* 
</dt> <dd>

Wenn *idaction* Hilfe- \_ TCard- \_ Daten angibt, wird dieser Parameter vom Hilfe Autor **lange** angegeben. Andernfalls ist dieser Parameter gleich 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert. NULL verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 




