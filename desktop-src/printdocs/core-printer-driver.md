---
description: Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängig sind.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: CORE_PRINTER_DRIVER Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356149"
---
# <a name="core_printer_driver-structure"></a>Struktur des Kern \_ Drucker \_ Treibers

Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängig sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>Member

<dl> <dt>

**Coredriverguid**
</dt> <dd>

Die GUID des Haupt Druckertreibers.

</dd> <dt>

**ftdriverdate**
</dt> <dd>

Das Datum und die Uhrzeit der neuesten Version des Haupt Druckertreibers.

</dd> <dt>

**dwldriverversion**
</dt> <dd>

Die Versions-ID der neuesten Version des Haupt Druckertreibers.

</dd> <dt>

**szpackageid, \[ maximaler \_ Pfad\]**
</dt> <dd>

Der Pfad zum Treiber Paket, das den Kern Druckertreiber enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur kann den Basis Treiber eines Herstellers darstellen, von dem die Treiber für verschiedene Druckermodelle abhängig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Core \_ Printer \_ driverw** (Unicode) und **\_ Core \_ Printer \_ drivera** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




