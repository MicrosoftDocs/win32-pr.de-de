---
description: Die Port \_ Info \_ 3-Struktur gibt den Statuswert eines Drucker Anschlusses an.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: PORT_INFO_3 Struktur (winspool. h)
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
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363456"
---
# <a name="port_info_3-structure"></a>Port \_ Info \_ 3-Struktur

Die **Port \_ Info \_ 3** -Struktur gibt den Statuswert eines Drucker Anschlusses an.

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

Der neue Port Statuswert. Dieser Wert wird nur verwendet, wenn der **pszstatus** -Member **null** ist.

Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                            | Bedeutung                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Löscht den Status des Drucker Anschlusses.                     |
| Port \_ Status \_ Offline            | Der Drucker des Ports ist offline.                      |
| Port \_ Status \_ Papier \_ Marmelade         | Der Drucker des Ports hat eine Papier Marmelade.                 |
| Port \_ Status \_ Papier \_ out         | Der Drucker des Ports ist nicht mehr im Papier.                 |
| Port \_ Status- \_ Ausgabe \_ bin \_ voll  | Der Ausgabe Korb des Ports ist voll.            |
| Problem mit dem Port \_ Status \_ Papier \_     | Der Drucker des Ports hat ein Papier Problem.             |
| Port \_ Status \_ kein \_ Toner          | Der Drucker des Ports ist nicht mehr Toner.                 |
| Port \_ Status- \_ Tür \_ geöffnet         | Die Tür des Drucker des Ports ist offen.             |
| Port \_ Status \_ Benutzer \_ Eingriff | Der Drucker des Ports erfordert einen Benutzereingriff.      |
| Port \_ Status \_ nicht genügend Arbeits \_ \_ Speicher    | Der Drucker des Ports weist nicht genügend Arbeitsspeicher auf.                |
| Port \_ Status- \_ Toner \_ niedrig         | Der Drucker des Ports ist auf dem Toner niedrig.                 |
| \_ \_ Anwärm Status des Ports \_        | Der Drucker des Ports wird erwärmt.                   |
| \_ \_ Energiespar Status des Port Status \_        | Der Drucker des Ports befindet sich in einem Energiesparmodus. |



 

</dd> <dt>

**pszstatus**
</dt> <dd>

Zeiger auf eine neue festzulegende Wert Zeichenfolge für den Drucker Anschluss. Verwenden Sie dieses Mitglied, wenn es keinen geeigneten Statuswert für den **dwStatus**-Wert gibt.

</dd> <dt>

**dwschwere Grad**
</dt> <dd>

Der Schweregrad des Port Status Werts.

Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                       | Bedeutung                                   |
|-----------------------------|-------------------------------------------|
| \_Fehler beim \_ Porttyp. \_   | Der Wert für den Port Status weist auf einen Fehler hin. |
| Port \_ Status \_ \_ Warnung | Der Wert für den Port Status ist eine Warnung.       |
| Informationen zum Port \_ Status- \_ Typ \_    | Der Port Statuswert ist "Information".   |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen druckerportstatuswert mit dem Wert " \_ \_ Fehler beim Porttyp" festlegen \_ , beendet der Druck Spooler das Senden von Aufträgen an den Port. Der Druck Spooler setzt das Senden von Aufträgen an den Port erst fort, wenn ein anderer [**setPort**](setport.md) -Rückruf zum Löschen des Status erfolgt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Port \_ Info \_ 3W** (Unicode) und **\_ Port \_ Info \_ 3a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




