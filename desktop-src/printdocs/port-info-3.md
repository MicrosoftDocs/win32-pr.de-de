---
description: Die PORT \_ INFO \_ 3-Struktur gibt den Statuswert eines Druckerports an.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: PORT_INFO_3 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cdd7f2fd931c7f503d566cdfc4ab38c5f595b51cea23d0cdf2fb326811cf7748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033968"
---
# <a name="port_info_3-structure"></a>PORT \_ INFO \_ 3-Struktur

Die **PORT \_ INFO \_ 3-Struktur** gibt den Statuswert eines Druckerports an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a>Member

<dl> <dt>

**dwStatus**
</dt> <dd>

Der neue Portstatuswert. Dieser Wert wird nur verwendet, wenn **der pszStatus-Member** **NULL ist.**

Dieser Member kann einer der folgenden Werte sein.



| Wert                            | Bedeutung                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Entfernt den Druckerportstatus.                     |
| PORTSTATUS \_ \_ OFFLINE            | Der Drucker des Anschlusses ist offline.                      |
| \_ \_ PAPIERSTAU FÜR \_ PORTSTATUS         | Der Drucker des Anschlusses verfügt über einen Papierstau.                 |
| PAPIER \_ ZUM \_ \_ PORTSTATUS         | Der Drucker des Anschlusses ist ohne Papier.                 |
| PORT \_ STATUS \_ OUTPUT \_ BIN \_ FULL  | Der Ausgabebehälter des Druckers des Anschlusses ist voll.            |
| PROBLEM MIT \_ DEM \_ \_ PORTSTATUSDOKUMENT     | Der Drucker des Anschlusses hat ein Papierproblem.             |
| PORTSTATUS \_ \_ KEIN \_ TONER          | Der Drucker des Anschlusses ist nicht mehr toner.                 |
| PORT \_ STATUS \_ DOOR \_ OPEN         | Die Tür des Druckers des Anschlusses ist geöffnet.             |
| \_PORTSTATUS \_ \_ BENUTZEREINGRIFF | Der Drucker des Anschlusses erfordert einen Benutzereingriff.      |
| PORTSTATUS \_ \_ NICHT GENÜGEND \_ \_ ARBEITSSPEICHER    | Der Drucker des Anschlusses verfügt nicht über genügend Arbeitsspeicher.                |
| PORTSTATUS \_ \_ TONER \_ LOW         | Der Drucker des Anschlusses verfügt über wenig Toner.                 |
| PORTSTATUS \_ \_ NACH \_ OBEN        | Der Drucker des Anschlusses wird aufwärmt.                   |
| PORTSTATUS \_ \_ – \_ STROMSPAREN        | Der Drucker des Anschlusses befindet sich im Energiemodus. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Zeiger auf eine neue Zeichenfolge für den Druckerportstatus, die festgelegt werden soll. Verwenden Sie diesen Member, wenn unter den für dwStatus aufgeführten kein geeigneter **Statuswert enthalten ist.**

</dd> <dt>

**dwSeverity**
</dt> <dd>

Der Schweregrad des Portstatuswerts.

Dieser Member kann einer der folgenden Werte sein.



| Wert                       | Bedeutung                                   |
|-----------------------------|-------------------------------------------|
| \_ \_ \_ PORTSTATUSTYPFEHLER   | Der Portstatuswert gibt einen Fehler an. |
| \_ \_ \_ PORTSTATUSTYPWARNUNG | Der Portstatuswert ist eine Warnung.       |
| INFORMATIONEN ZUM \_ \_ \_ PORTSTATUSTYP    | Der Portstatuswert ist informationell.   |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie einen Druckerportstatuswert mit dem Schweregrad PORT STATUS TYPE ERROR festlegen, beendet der Druckspooler das Senden von Aufträgen \_ \_ an den \_ Port. Der Druckspooler setzt das Senden von Aufträgen an den Port erst dann wieder auf, wenn ein weiterer [**SetPort-Aufruf**](setport.md) erfolgt, um den Status zu löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PORT \_ INFO \_ 3W** (Unicode) und **\_ PORT INFO \_ \_ 3A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




