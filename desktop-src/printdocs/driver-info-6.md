---
description: Die Treiber \_ Info \_ 6-Struktur enthält Druckertreiber Informationen.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: DRIVER_INFO_6 Struktur (winspool. h)
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
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348588"
---
# <a name="driver_info_6-structure"></a>Treiber \_ Info \_ 6-Struktur

Die **Treiber \_ Info \_ 6** -Struktur enthält Druckertreiber Informationen.

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

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows NT x86, Windows ia64 und Windows x64).

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

**phelpfile**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt (z. b. C: \\ Drivers \\ PSCRPTUI. hlp).

</dd> <dt>

**pdependentfiles**
</dt> <dd>

Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von null-terminierten Zeichen folgen enthält. Jede mit NULL endenden Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt. Die Sequenz von Zeichen folgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet. Wenn **pdependentfiles** nicht **null** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichen folgen angezeigt.

</dd> <dt>

**pmonitorname**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen sprach Monitor angibt (z. b. "PJL-Monitor"). Dieser Member kann **null** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation unterstützen.

</dd> <dt>

**pdefaultdatatype**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standard Datentyp des Druckauftrags angibt (z. b. "EMF").

</dd> <dt>

**pszzpreviousnames**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die vorherige Druckertreiber Namen angibt, die mit diesem Treiber kompatibel sind. Beispiel: OldName1 \\ 0oldname2 \\ 0 \\ 0.

</dd> <dt>

**ftdriverdate**
</dt> <dd>

Das Datum des Treiber Pakets, das in den Treiberdateien codiert ist.

</dd> <dt>

**dwldriverversion**
</dt> <dd>

Die Versionsnummer des Treibers. Dies ergibt sich aus der Versions Struktur des Treibers.

</dd> <dt>

**pszmf-Name**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Herstellers angibt.

</dd> <dt>

**pszoemurl**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die URL für den Hersteller angibt.

</dd> <dt>

**pszhardwareid**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Hardware-ID für den Druckertreiber angibt.

</dd> <dt>

**pszprovider**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Anbieter des Druckertreibers angibt (z. b. "Microsoft Windows 2000")

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Zeichen folgen für diese Member sind in der INF-Datei enthalten, die verwendet wird, um den Treiber hinzuzufügen.

Wenn Sie [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md) aufrufen, bei dem die *Ebene* nicht gleich 6 ist, wenn Sie [**getprinterdriver**](getprinterdriver.md) oder [**enumprinterdrivers**](enumprinterdrivers.md) mit einer *Ebene* gleich 6 aufrufen, wird die **Driver \_ Info \_ 6** -Struktur mit **pszmfgname**, **pszoemurl**, **pszhardwareid** und **pszprovider** auf **null**, **dwldriverversion** auf 0 und **ftdriverdate** auf (0,0) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Treiber \_ Info \_ 6W** (Unicode) und **\_ Treiber \_ Info \_ 6a** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Addprinterdriverex**](addprinterdriverex.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

 




