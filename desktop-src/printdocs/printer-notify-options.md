---
description: Die Struktur der Drucker \_ \_ Benachrichtigungs Optionen gibt Optionen für ein Änderungs Benachrichtigungs Objekt an, das einen Drucker oder Druckserver überwacht.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: PRINTER_NOTIFY_OPTIONS Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362294"
---
# <a name="printer_notify_options-structure"></a>Struktur der Drucker \_ Benachrichtigungs \_ Optionen

Die Struktur der **Drucker \_ Benachrichtigungs \_ Optionen** gibt Optionen für ein Änderungs Benachrichtigungs Objekt an, das einen Drucker oder Druckserver überwacht.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser-Struktur. Legen Sie diesen Member auf 2 fest.

</dd> <dt>

**Flags**
</dt> <dd>

Ein Bitflag. Wenn Sie \_ \_ in einem aufzurufenden Befehl die Funktion " \_ [**findnextprinterchangenotifi"**](findnextprinterchangenotification.md) das Aktualisierungs Flag für Drucker Benachrichtigen festlegen, stellt die Funktion aktuelle Daten für alle überwachten Drucker Informationsfelder bereit. Die [**findfirstprinterchangenotifi-**](findfirstprinterchangenotification.md) Funktion ignoriert den **Flags** -Member.

</dd> <dt>

**Count**
</dt> <dd>

Die Anzahl der Elemente im **ptypes** -Array.

</dd> <dt>

**ptypes**
</dt> <dd>

Ein Zeiger auf ein Array von [**Optionen für den \_ druckerbenachrichtigungs- \_ \_ Typ**](printer-notify-options-type.md) . Verwenden Sie ein Element dieses Arrays, um die zu überwachenden Drucker Informationsfelder anzugeben, und ein Element, um die zu überwachenden Felder der Auftrags Informationen anzugeben. Sie können entweder Drucker Informationen, Auftrags Informationen oder beides überwachen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Struktur mit der [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) , um die Gruppe der Drucker-oder Auftrags Informationsfelder anzugeben, die auf Änderungen überwacht werden sollen.

Verwenden Sie diese Struktur mit der [**findnextprinterchangenotifizierungsfunktion**](findnextprinterchangenotification.md) , um die aktuellen Daten für alle überwachten Drucker-und Auftrags Informationsfelder anzufordern. In diesem Fall gibt das **Flags** -Element das \_ Aktualisierungs Flag für Drucker Benachrichtigungen an \_ \_ , und die Funktion ignoriert die anderen Strukturmember.

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

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> <dt>

[**Typ der Drucker \_ Benachrichtigungs \_ Optionen \_**](printer-notify-options-type.md)
</dt> </dl>

 

 




