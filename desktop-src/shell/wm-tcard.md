---
description: Wird mit Windows Hilfe an eine Anwendung gesendet, die eine Trainingskarte initiiert hat.
title: WM_TCARD Nachricht (Winuser.h)
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
ms.openlocfilehash: 85435c5674ad6a2ac4e05edaa5d450dc61de9eac6dae05d3b19662aec91a61f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856985"
---
# <a name="wm_tcard-message"></a>\_WM-TCARD-Nachricht

Wird mit Windows Hilfe an eine Anwendung gesendet, die eine Trainingskarte initiiert hat. Die Meldung informiert die Anwendung, wenn der Benutzer auf eine beschreibbare Schaltfläche klickt. Eine Anwendung initiiert eine Trainingskarte, indem sie den HELP \_ TCARD-Befehl in einem Aufruf der [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) angibt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*idAction* 
</dt> <dd>

Ein -Wert, der die Aktion angibt, die der Benutzer ausgeführt hat. Dies kann einer der folgenden Werte sein.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

Der Benutzer hat auf  eine beschreibbare Abbruchschaltfläche geklickt.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**Idcancel**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare Schaltfläche **Abbrechen** geklickt.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

Der Benutzer hat die Trainingskarte geschlossen.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare Windows **Schaltfläche Hilfe** geklickt.

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare Schaltfläche **Ignorieren** geklickt.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**Idok**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare SCHALTFLÄCHE **OK** geklickt.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare Schaltfläche **Nein** geklickt.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

Der Benutzer hat auf  eine beschreibbare Wiederholungsschaltfläche geklickt.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**\_HILFE-TCARDDATEN \_**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare Schaltfläche geklickt. Der *dwActionData-Parameter* enthält eine lange ganze Zahl, die vom Hilfeautor angegeben wird.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP \_ TCARD \_ OTHER \_ CALLER**


</dt> <dd>

Eine andere Anwendung hat Trainingskarten angefordert.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

Der Benutzer hat auf eine beschreibbare **Ja-Schaltfläche** geklickt.

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Wenn *idAction* HELP \_ TCARD DATA angibt, ist dieser Parameter \_ vom Autor der Hilfe **lange** angegeben. Andernfalls ist dieser Parameter 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert. verwenden Sie 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

 




