---
description: Die Treiber \_ Info \_ 4-Struktur enthält Druckertreiber Informationen.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: DRIVER_INFO_4 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215856"
---
# <a name="driver_info_4-structure"></a>Treiber \_ Info \_ 4-Struktur

Die **Treiber \_ Info \_ 4** -Struktur enthält Druckertreiber Informationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a>Member

<dl> <dt>

**cversion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Treibers angibt (z. b. "QMS 810").

</dd> <dt>

**nach-oben**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).

</dd> <dt>

**pdriverpath**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).

</dd> <dt>

**pdatafile**
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).

</dd> <dt>

**pconfigfile**
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).

</dd> <dt>

**phelpfile**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt.

</dd> <dt>

**pdependentfiles**
</dt> <dd>

Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von null-terminierten Zeichen folgen enthält. Jede mit NULL endenden Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt. Die Sequenz von Zeichen folgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet. Wenn **pdependentfiles** nicht **null** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichen folgen angezeigt.

</dd> <dt>

**pmonitorname**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen sprach Monitor angibt (z. b. PJL-Monitor). Dieser Member kann **null** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation unterstützen.

</dd> <dt>

**pdefaultdatatype**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standard Datentyp des Druckauftrags angibt (z. b. EMF).

</dd> <dt>

**pszzpreviousnames**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die vorherige Druckertreiber Namen angibt, die mit diesem Treiber kompatibel sind. Beispiel: OldName1 \\ 0oldname2 \\ 0 \\ 0.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Treiber \_ Info \_ 4W** (Unicode) und **\_ Treiber \_ Info \_ 4a** (ANSI)<br/>                             |



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

 

 




