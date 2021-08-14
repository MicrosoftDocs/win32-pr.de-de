---
description: Die \_ DRIVER INFO \_ 2-Struktur identifiziert einen Druckertreiber, die Versionsnummer des Treibers, die Umgebung, für die der Treiber geschrieben wurde, den Namen der Datei, in der der Treiber gespeichert ist usw.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: DRIVER_INFO_2-Struktur (Winspool.h)
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
ms.openlocfilehash: dcb65f066286b5f5cd2fec935fb2223c25cf87fcc64d17de274b9b182a372440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732858"
---
# <a name="driver_info_2-structure"></a>DRIVER \_ INFO \_ 2-Struktur

Die **DRIVER \_ INFO \_ 2-Struktur** identifiziert einen Druckertreiber, die Versionsnummer des Treibers, die Umgebung, für die der Treiber geschrieben wurde, den Namen der Datei, in der der Treiber gespeichert ist usw.

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

**cVersion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Treibers angibt (z. B. "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. B. Windows x86, Windows IA64 und Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. B. "c: \\ drivers \\pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiberdaten enthält (z. B. "c: \\ drivers \\ Qms810.ppd").

</dd> <dt>

**pConfigFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfiguration des Gerätetreibers .dll angibt (z. B. "c: \\ drivers \\Pscrptui.dll").

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DRIVER \_ INFO \_ 2W** (Unicode) und **\_ DRIVER INFO \_ \_ 2A** (ANSI)<br/>                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




