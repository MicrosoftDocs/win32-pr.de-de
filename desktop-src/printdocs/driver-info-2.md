---
description: Die Treiber \_ Info \_ 2-Struktur identifiziert einen Druckertreiber, die Treiber Versionsnummer, die Umgebung, für die der Treiber geschrieben wurde, den Namen der Datei, in der der Treiber gespeichert ist, usw.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: DRIVER_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350201"
---
# <a name="driver_info_2-structure"></a>Struktur der Treiber \_ Info \_ 2

Die **Treiber \_ Info \_ 2** -Struktur identifiziert einen Druckertreiber, die Treiber Versionsnummer, die Umgebung, für die der Treiber geschrieben wurde, den Namen der Datei, in der der Treiber gespeichert ist, usw.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**cversion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Treibers angibt (z. b. "QMS 810").

</dd> <dt>

**nach-oben**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).

</dd> <dt>

**pdriverpath**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen, einen vollständigen Pfad und einen Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. "c: \\ Drivers \\pscript.dll").

</dd> <dt>

**pdatafile**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. "c: \\ Drivers \\ Qms810. PPD").

</dd> <dt>

**pconfigfile**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Configuration. dll des Gerätetreibers angibt (z. b. "c: \\ Drivers \\Pscrptui.dll").

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Treiber \_ Informationen \_ 2W** (Unicode) und **\_ Treiber \_ Info \_ 2a** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

 




