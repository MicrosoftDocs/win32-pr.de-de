---
description: Die \_ DRIVER INFO \_ 4-Struktur enthält Druckertreiberinformationen.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: DRIVER_INFO_4-Struktur (Winspool.h)
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
ms.openlocfilehash: d42f74ce58c126130bd28820283c0b4262d3e3ce6b05106ae9ff74bc280ae234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353930"
---
# <a name="driver_info_4-structure"></a>DRIVER \_ INFO \_ 4-Struktur

Die **DRIVER \_ INFO \_ 4-Struktur** enthält Druckertreiberinformationen.

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

**cVersion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Treibers angibt (z. B. "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. B. Windows x86, Windows IA64 und Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. B. C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiberdaten enthält (z. B. C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Dynamic Link-Bibliothek des Gerätetreibers angibt (z. B. C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt.

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von auf NULL endende Zeichenfolgen enthält. Jede auf NULL endende Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt. Die Zeichenfolgensequenz wird durch eine leere Zeichenfolge der Länge 0 (null) beendet. Wenn **pDependentFiles** nicht **NULL** ist und keine Dateinamen enthält, verweist es auf einen Puffer, der zwei leere Zeichenfolgen enthält.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Sprachmonitor angibt (z. B. PJL-Monitor). Dieser Member kann **NULL** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation ermöglichen.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Standarddatentyp des Druckauftrags angibt (z. B. EMF).

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die vorherige Druckertreibernamen angibt, die mit diesem Treiber kompatibel sind. Beispiel: OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DRIVER \_ INFO \_ 4W** (Unicode) und **\_ DRIVER INFO \_ \_ 4A** (ANSI)<br/>                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




