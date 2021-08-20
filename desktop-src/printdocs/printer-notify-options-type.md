---
description: Die \_ PRINTER NOTIFY \_ OPTIONS \_ TYPE-Struktur gibt die Gruppe von Drucker- oder Auftragsinformationsfeldern an, die von einem Druckeränderungsbenachrichtigungsobjekt überwacht werden sollen. Ein Aufruf der FindFirstPrinterChangeNotification-Funktion gibt eine PRINTER \_ NOTIFY \_ OPTIONS-Struktur an, die ein Array von \_ PRINTER NOTIFY OPTIONS \_ \_ TYPE-Strukturen enthält.
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: PRINTER_NOTIFY_OPTIONS_TYPE-Struktur (Winspool.h)
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
ms.openlocfilehash: 2b593a502a668345cdd0206b4f1363cf160074b6c9aa26696427b5b42a0fbdc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056277"
---
# <a name="printer_notify_options_type-structure"></a>\_STRUKTUR DES TYPS "DRUCKERBENACHRICHTIGUNGSOPTIONEN" \_ \_

Die **PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE-Struktur** gibt die Gruppe von Drucker- oder Auftragsinformationsfeldern an, die von einem Druckeränderungsbenachrichtigungsobjekt überwacht werden sollen.

Ein Aufruf der [**FindFirstPrinterChangeNotification-Funktion**](findfirstprinterchangenotification.md) gibt eine [**PRINTER NOTIFY \_ \_ OPTIONS-Struktur**](printer-notify-options.md) an, die ein Array von **PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE-Strukturen** enthält.

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

**Typ**
</dt> <dd>

Der Typ, der überwacht werden soll. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                      | Bedeutung                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**JOB \_ NOTIFY \_ TYPE**</dt> <dt>0x01</dt> </dl>             | Gibt an, dass die im **pFields-Array angegebenen** Felder JOB \_ NOTIFY \_ \_ \* FIELD-Konstanten sind.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**DRUCKER \_ NOTIFY \_ TYPE**</dt> <dt>0x00</dt> </dl> | Gibt an, dass die im **pFields-Array angegebenen** Felder PRINTER \_ NOTIFY \_ \_ \* FIELD-Konstanten sind.<br/> |



 

</dd> <dt>

**Reserviert 0**
</dt> <dd>

Reserviert.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reserviert.

</dd> <dt>

**Reserviert 2**
</dt> <dd>

Reserviert.

</dd> <dt>

**Count**
</dt> <dd>

Die Anzahl der Elemente im **pFields-Array.**

</dd> <dt>

**pFields**
</dt> <dd>

Ein Zeiger auf ein Array von Werten. Jedes Element des Arrays gibt ein gewünschtes Auftrags- oder Druckerinformationsfeld an. Eine Liste der unterstützten Drucker- und Auftragsinformationsfelder finden Sie in der Struktur [**PRINTER \_ NOTIFY INFO \_ \_ DATA.**](printer-notify-info-data.md)

</dd> </dl>

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

[**INFODATEN \_ FÜR DRUCKERBENACHRICHTIGUNGEN \_ \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_OPTIONEN FÜR \_ DRUCKERBENACHRICHTIGUNGEN**](printer-notify-options.md)
</dt> </dl>

 

 




