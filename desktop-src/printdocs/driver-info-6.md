---
description: Die DRIVER \_ INFO \_ 6-Struktur enthält Druckertreiberinformationen.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: DRIVER_INFO_6 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: fd90794fe4c6f41f8704cb626ddfcf9487c89da01afb8a2f8b1fddfe0efea43a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092070"
---
# <a name="driver_info_6-structure"></a>DRIVER \_ INFO \_ 6-Struktur

Die **DRIVER \_ INFO \_ 6-Struktur** enthält Druckertreiberinformationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a>Member

<dl> <dt>

**cVersion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Treibers angibt (z. B. QMS 810).

</dd> <dt>

**pUmgebung**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. B. Windows NT x86, Windows IA64 und Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. B. C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Zeiger auf eine auf NULL terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiberdaten enthält (z. B. C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Dynamic Link-Konfigurationsbibliothek des Gerätetreibers angibt (z. B. C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt (z. B. C: \\ DRIVERS \\ Pscrptui.hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von auf NULL beendeten Zeichenfolgen enthält. Jede auf NULL beendete Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängig ist. Die Sequenz von Zeichenfolgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet. Wenn **pDependentFiles** nicht **NULL** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichenfolgen zeigen.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die einen Sprachmonitor angibt (z. B. "PJL-Monitor"). Dieser Member kann **NULL sein und** sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation verwenden können.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Ein Zeiger auf eine auf NULL terminierte Zeichenfolge, die den Standarddatentyp des Druckauftrags angibt (z. B. "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die vorherige Druckertreibernamen angibt, die mit diesem Treiber kompatibel sind. Beispiel: OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Das Datum des Treiberpakets, wie in den Treiberdateien codiert.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Versionsnummer des Treibers. Dies stammt aus der Versionsstruktur des Treibers.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Herstellers angibt.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die die URL für den Hersteller angibt.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die die Hardware-ID für den Druckertreiber angibt.

</dd> <dt>

**pszProvider**
</dt> <dd>

Zeiger auf eine nullbeendte Zeichenfolge, die den Anbieter des Druckertreibers angibt (z. B. "Microsoft Windows 2000").

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Zeichenfolgen für diese Member sind in der INF-Datei enthalten, die zum Hinzufügen des Treibers verwendet wird.

Wenn Sie [**AddPrinterDriver oder**](addprinterdriver.md) [**AddPrinterDriverEx mit**](addprinterdriverex.md) einer Ebene aufrufen, *die* nicht gleich 6 ist, und  dann rufen Sie [**GetPrinterDriver**](getprinterdriver.md) oder [**EnumPrinterDrivers**](enumprinterdrivers.md) mit der Ebene 6 auf, die **DRIVER INFO \_ \_ 6-Struktur** wird mit **pszMfgName,** **pszOEMUrl,** **pszHardwareID** und **pszProvider** zurückgegeben, die auf **NULL** festgelegt sind, **dwlDriverVersion** auf 0 und **ftDriverDate** auf (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DRIVER \_ INFO \_ 6W** (Unicode) und **\_ DRIVER INFO \_ \_ 6A** (ANSI)<br/>                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




