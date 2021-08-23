---
description: Die PRINTER \_ NOTIFY \_ OPTIONS-Struktur gibt Optionen für ein Änderungsbenachrichtigungsobjekt an, das einen Drucker oder Druckerserver überwacht.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: PRINTER_NOTIFY_OPTIONS -Struktur (Winspool.h)
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
ms.openlocfilehash: 57b95717e7873f0b73b66d450849d92a2c2ed7053d6d387286cc58144c772ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731132"
---
# <a name="printer_notify_options-structure"></a>PRINTER \_ NOTIFY \_ OPTIONS-Struktur

Die **PRINTER \_ NOTIFY \_ OPTIONS-Struktur** gibt Optionen für ein Änderungsbenachrichtigungsobjekt an, das einen Drucker oder Druckerserver überwacht.

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

Die Version dieser -Struktur. Legen Sie diesen Member auf 2 fest.

</dd> <dt>

**Flags**
</dt> <dd>

Ein Bitflag. Wenn Sie das FLAG PRINTER NOTIFY OPTIONS REFRESH in einem Aufruf der \_ \_ \_ [**FindNextPrinterChangeNotification-Funktion**](findnextprinterchangenotification.md) festlegen, stellt die Funktion aktuelle Daten für alle überwachten Druckerinformationsfelder zur Verfügung. Die [**FindFirstPrinterChangeNotification-Funktion**](findfirstprinterchangenotification.md) ignoriert den **Flags-Member.**

</dd> <dt>

**Count**
</dt> <dd>

Die Anzahl der Elemente im **pTypes-Array.**

</dd> <dt>

**pTypes**
</dt> <dd>

Ein Zeiger auf ein Array von [**PRINTER \_ NOTIFY OPTIONS \_ \_ TYPE-Strukturen.**](printer-notify-options-type.md) Verwenden Sie ein Element dieses Arrays, um die zu überwachenden Druckerinformationsfelder anzugeben, und ein Element, um die zu überwachenden Auftragsinformationsfelder anzugeben. Sie können Druckerinformationen, Auftragsinformationen oder beides überwachen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Struktur mit der [**FindFirstPrinterChangeNotification-Funktion,**](findfirstprinterchangenotification.md) um den Satz von Drucker- oder Auftragsinformationsfeldern anzugeben, die auf Änderungen überwacht werden.

Verwenden Sie diese Struktur mit der [**FindNextPrinterChangeNotification-Funktion,**](findnextprinterchangenotification.md) um die aktuellen Daten für alle überwachten Drucker- und Auftragsinformationsfelder an fordern. In diesem Fall gibt das **Flags-Element** das PRINTER NOTIFY OPTIONS REFRESH-Flag an, und die Funktion \_ ignoriert die anderen \_ \_ Strukturmitglieder.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_ \_ DRUCKERBENACHRICHTIGUNGSOPTIONENTYP \_**](printer-notify-options-type.md)
</dt> </dl>

 

 




