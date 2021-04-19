---
description: Die Drucker \_ Benachrichtigungs \_ Struktur enthält Drucker Informationen, die von der findnextprinterchangenotifi-Funktion zurückgegeben werden. Die Funktion gibt diese Informationen zurück, nachdem ein warte Vorgang für ein Benachrichtigungs Objekt für Drucker Änderungen abgeschlossen wurde.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: PRINTER_NOTIFY_INFO Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348668"
---
# <a name="printer_notify_info-structure"></a>Drucker \_ Benachrichtigungs \_ Struktur

Die **Drucker \_ Benachrichtigungs \_** Struktur enthält Drucker Informationen, die von der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion zurückgegeben werden. Die Funktion gibt diese Informationen zurück, nachdem ein warte Vorgang für ein Benachrichtigungs Objekt für Drucker Änderungen abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser-Struktur. Legen Sie diesen Member auf 2 fest.

</dd> <dt>

**Flags**
</dt> <dd>

Ein Bitflag, das den Zustand der Benachrichtigungs Struktur angibt. Wenn das \_ \_ \_ verworfene Bit der Drucker Benachrichtigung festgelegt ist, weist dies darauf hin, dass einige Benachrichtigungen verworfen werden mussten.

</dd> <dt>

**Count**
</dt> <dd>

Die Anzahl der [**Drucker \_ Benachrichtigungs \_ \_ Daten**](printer-notify-info-data.md) Elemente im **ADATA** -Array.

</dd> <dt>

**ADATA**
</dt> <dd>

Ein Array von [**Drucker \_ \_ Informationen- \_ Daten**](printer-notify-info-data.md) Strukturen, die benachrichtigt werden. Jedes Element des Arrays identifiziert ein einzelnes Auftrags-oder Drucker Informationsfeld und stellt die aktuellen Daten für dieses Feld bereit.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn für den **Flags** -Member der Wert für das \_ verworfene druckerbenachrichtigungs \_ \_ -Bit festgelegt ist, weist dies darauf hin, dass ein Überlauf oder Fehler aufgetreten ist In diesem Fall müssen Sie " [**findnextprinterchangenotifi"**](findnextprinterchangenotification.md) aufrufen und das \_ \_ Aktualisierungs Flag für Drucker Benachrichtigungs Optionen angeben \_ , um alle aktuellen Informationen abzurufen. Bis Sie diesen Aktualisierungs Vorgang anfordern, sendet das System keine weiteren Benachrichtigungen für dieses Änderungs Benachrichtigungs Objekt.

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

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_ \_ Info \_ Daten für Drucker Benachrichtigen**](printer-notify-info-data.md)
</dt> </dl>

 

 




