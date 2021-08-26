---
description: Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängen.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: CORE_PRINTER_DRIVER-Struktur (Winspool.h)
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
ms.openlocfilehash: 18ac3dba88d9cf781393b01b6594777426b7195e6f68afa0fd00a5bddb01f129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950400"
---
# <a name="core_printer_driver-structure"></a>CORE \_ PRINTER \_ DRIVER-Struktur

Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängen.

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

**CoreDriverGUID**
</dt> <dd>

Die GUID des Kerndruckertreibers.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Datum und Uhrzeit der neuesten Version des Kerndruckertreibers.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Die Versions-ID der neuesten Version des Kerndruckertreibers.

</dd> <dt>

**szPackageID \[ MAX \_ PATH\]**
</dt> <dd>

Der Pfad zum Treiberpaket, das den Kerndruckertreiber enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur kann den Basistreiber eines Herstellers darstellen, von dem die Treiber für verschiedene Druckermodelle abhängig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ CORE \_ PRINTER \_ DRIVERW** (Unicode) und **\_ CORE PRINTER \_ \_ DRIVERA** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




