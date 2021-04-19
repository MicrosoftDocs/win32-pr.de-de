---
description: Die Treiber \_ Info \_ 5-Struktur enthält Druckertreiber Informationen.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: DRIVER_INFO_5 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355381"
---
# <a name="driver_info_5-structure"></a>Treiber \_ Info \_ 5-Struktur

Die **Treiber \_ Info \_ 5** -Struktur enthält Druckertreiber Informationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a>Member

<dl> <dt>

**cversion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Treibers angibt (z. b. QMS 810).

</dd> <dt>

**nach-oben**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).

</dd> <dt>

**pdriverpath**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).

</dd> <dt>

**pdatafile**
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).

</dd> <dt>

**pconfigfile**
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).

</dd> <dt>

**dwdriverattribute**
</dt> <dd>

Treiber Attribute, wie z. b. umpd/kmpd.

</dd> <dt>

**dwconfigversion**
</dt> <dd>

Gibt an, wie oft die Konfigurationsdatei für diesen Treiber seit dem letzten Neustart des Spoolers aktualisiert oder herabgestuft wurde.

</dd> <dt>

**dwdriverversion**
</dt> <dd>

Gibt an, wie oft die Treiberdatei für diesen Treiber seit dem letzten Neustart des Spoolers aktualisiert oder herabgestuft wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Treiber \_ Info \_ 5W** (Unicode) und **\_ Treiber \_ Info \_ 5A** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

 




