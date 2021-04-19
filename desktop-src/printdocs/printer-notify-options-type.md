---
description: Die \_ Typstruktur der druckerbenachrichtigungsoptionen \_ \_ gibt den Satz von Druckern oder Auftrags Informationsfeldern an, die von einem Benachrichtigungs Objekt für Drucker Änderungen überwacht werden sollen. Ein aufzurufende "findfirstprinterchangenotifi"-Funktion gibt eine Drucker \_ Benachrichtigungs \_ Optionen-Struktur an, die ein Array von Optionen für die \_ \_ Typstrukturen der Drucker Benachrichtigung enthält \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: PRINTER_NOTIFY_OPTIONS_TYPE Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353534"
---
# <a name="printer_notify_options_type-structure"></a>Drucker \_ Benachrichtigungs \_ Optionen \_ Typstruktur

Die **\_ \_ \_ Typstruktur der druckerbenachrichtigungsoptionen** gibt den Satz von Druckern oder Auftrags Informationsfeldern an, die von einem Benachrichtigungs Objekt für Drucker Änderungen überwacht werden sollen.

Ein aufzurufende " [**findfirstprinterchangenotifi"**](findfirstprinterchangenotification.md) -Funktion gibt eine [**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md) -Struktur an, die ein Array von Optionen für die **\_ \_ \_ Typstrukturen der Drucker Benachrichtigung** enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a>Member

<dl> <dt>

**Type**
</dt> <dd>

Der Typ, der überwacht werden soll. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                      | Bedeutung                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Auftrag \_ Benachrichtigen von \_ Typ**</dt> <dt>0x01</dt> </dl>             | Gibt an, dass die im **pfields** -Array angegebenen Felder Auftrags \_ Benachrichtigungs \_ Feld \_ \* Konstanten sind.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Drucker \_ Benachrichtigen von \_ Typ**</dt> <dt>0x00</dt> </dl> | Gibt an, dass die im **pfields** -Array angegebenen Felder Drucker \_ Benachrichtigungs \_ Feld \_ \* Konstanten sind.<br/> |



 

</dd> <dt>

**Reserved0**
</dt> <dd>

Reserviert.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reserviert.

</dd> <dt>

**"Reserved2"**
</dt> <dd>

Reserviert.

</dd> <dt>

**Count**
</dt> <dd>

Die Anzahl der Elemente im **pfields** -Array.

</dd> <dt>

**pfields**
</dt> <dd>

Ein Zeiger auf ein Array von-Werten. Jedes Element des Arrays gibt das gewünschte Feld für Aufträge oder Drucker Informationen an. Eine Liste der unterstützten Felder für Drucker und Auftrags Informationen finden Sie in der [**\_ \_ \_ Daten**](printer-notify-info-data.md) Struktur zum Benachrichtigen von Drucker Informationen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_ \_ Info \_ Daten für Drucker Benachrichtigen**](printer-notify-info-data.md)
</dt> <dt>

[**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md)
</dt> </dl>

 

 




