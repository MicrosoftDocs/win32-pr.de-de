---
description: Enthält Druckertreiberinformationen.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: DRIVER_INFO_8-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 753b05b9d59bb98742d5c49102b604cc0a499a4dcdc6c624489d261400279297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234839"
---
# <a name="driver_info_8-structure"></a>DRIVER \_ INFO \_ 8-Struktur

Enthält Druckertreiberinformationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a>Member

<dl> <dt>

**cVersion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Treibers angibt (z. B. QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. B. Windows x86, Windows IA64 und Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. B. C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiberdaten enthält (z. B. C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Dynamic Link-Bibliothek der Konfiguration des Gerätetreibers angibt (z. B. C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt (z. B. C: \\ DRIVERS \\ Pscrptui.hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von auf NULL endende Zeichenfolgen enthält. Jede auf NULL endende Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt. Die Zeichenfolgensequenz wird durch eine leere Zeichenfolge der Länge 0 (null) beendet. Wenn **pDependentFiles** nicht **NULL** ist und keine Dateinamen enthält, verweist es auf einen Puffer, der zwei leere Zeichenfolgen enthält.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die einen Sprachmonitor angibt (z.B. "PJL-Monitor"). Dieser Member kann **NULL** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation ermöglichen.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Standarddatentyp des Druckauftrags angibt (z. B. "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die vorherige Druckertreibernamen angibt, die mit diesem Treiber kompatibel sind. Beispiel: OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Das Datum des Treiberpakets, wie in den Treiberdateien codiert.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Die Versionsnummer des Treibers. Dies ergibt sich aus der Versionsstruktur des Treibers.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Herstellers angibt.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die URL für den Hersteller angibt.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Hardware-ID für den Druckertreiber angibt.

</dd> <dt>

**pszProvider**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Anbieter des Druckertreibers angibt (z. B. "Microsoft Windows 2000").

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Druckprozessor angibt (z. B. "WinPrint").

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Treibereinrichtungs-DLL und den Einstiegspunkt des Herstellers angibt.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die dem Treiber zugeordneten Farbprofile angibt.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Pfad zur INF-Datei des Treibers im Treiberspeicher angibt. (Siehe Hinweise.) Dies muss **NULL** sein, wenn DRIVER \_ INFO \_ 8 an [**AddPrinterDriver**](addprinterdriver.md) oder [**AddPrinterDriverEx**](addprinterdriverex.md)übergeben wird.

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Attributflags für Druckertreiber. Dies muss 0 sein, wenn DRIVER \_ INFO \_ 8 an [**AddPrinterDriver**](addprinterdriver.md) oder [**AddPrinterDriverEx**](addprinterdriverex.md)übergeben wird. Andernfalls kann dies eine beliebige Kombination der folgenden Flags sein:



| Flagname/-wert                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                             | Mindestbetriebssystem                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| \_PAKETFÄHIGES \_ DRUCKERTREIBERPAKET \_<br/> 0x00000001<br/>        | Der Druckertreiber ist Teil eines Treiberpakets.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| DRUCKERTREIBER \_ \_ XPS<br/> 0x00000002<br/>                   | Der Druckertreiber unterstützt das im [XML Paper Specification: Übersicht](/previous-versions/windows/hardware/design/dn641615(v=vs.85))beschriebene Microsoft XPS-Format sowie im [Abschnitt Produktverhalten <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ DRUCKERTREIBER-SANDBOX \_ AKTIVIERT<br/> 0x00000004<br/>      | Der Druckertreiber ist mit [der Druckertreiberisolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)kompatibel. Weitere Informationen finden Sie im [Abschnitt Produktverhalten <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| \_ \_ DRUCKERTREIBERKLASSE<br/> 0x00000008<br/>                 | Der Druckertreiber ist ein [Klassendruckertreiber.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ DRUCKERTREIBER ABGELEITET<br/> 0x00000010<br/>               | Der Druckertreiber ist ein [abgeleiteter Druckertreiber.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| DRUCKERTREIBER \_ \_ KANN NICHT FREIGEGEBEN \_ WERDEN<br/> 0x00000020<br/>        | Drucker, die diesen Druckertreiber verwenden, können nicht freigegeben werden.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ DRUCKERTREIBERKATEGORIE \_ FAX<br/> 0x00000040<br/>         | Der Druckertreiber ist für die Verwendung mit [Faxdruckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ \_ DRUCKERTREIBERKATEGORIEDATEI<br/> 0x00000080<br/>        | Der Druckertreiber ist für die Verwendung mit [Dateidruckern vorgesehen.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ DRUCKERTREIBERKATEGORIE \_ VIRTUAL<br/> 0x00000100<br/>     | Der Druckertreiber ist für die Verwendung mit virtuellen [Druckern vorgesehen.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ \_ DRUCKERTREIBERKATEGORIEDIENST<br/> 0x00000200<br/>     | Der Druckertreiber ist für die Verwendung mit [Dienstdruckern vorgesehen.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_DRUCKERTREIBER– \_ SOFT RESET \_ \_ ERFORDERLICH<br/> 0x00000400<br/> | Drucker, die diesen Druckertreiber verwenden, sollten die In der Definition der USB-Geräteklasse beschriebenen Richtlinien befolgen. Weitere Informationen finden Sie unter [Produktverhalten, Abschnitt <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete mehrfache Zeichenfolge, die alle Hauptdruckertreiber angibt, von denen der Treiber abhängt. Dieser Wert muss **NULL sein,** **wenn DRIVER INFO \_ \_ 8** an [**AddPrinterDriver**](addprinterdriver.md) oder [**AddPrinterDriverEx übergeben wird.**](addprinterdriverex.md)

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

Das früheste zulässige Datum aller Treiber, die mit Windows geliefert wurden und von denen dieser Treiber abhängt.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

Die früheste zulässige Version aller Treiber, die im Lieferumfang Windows und von denen dieser Treiber abhängt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Zeichenfolgen für diese Member sind in der INF-Datei enthalten, die zum Hinzufügen des Treibers verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DRIVER \_ INFO \_ 8W** (Unicode) und **\_ DRIVER INFO \_ \_ 8A** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

