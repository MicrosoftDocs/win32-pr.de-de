---
description: Enthält Druckertreiber Informationen.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: DRIVER_INFO_8 Struktur (winspool. h)
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
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349089"
---
# <a name="driver_info_8-structure"></a>Treiber \_ Info \_ 8-Struktur

Enthält Druckertreiber Informationen.

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

**cversion**
</dt> <dd>

Die Betriebssystemversion, für die der Treiber geschrieben wurde. Der unterstützte Wert ist 3.

</dd> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Treibers angibt (z. b. QMS 810).

</dd> <dt>

**nach-oben**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).

</dd> <dt>

**pdriverpath**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).

</dd> <dt>

**pdatafile**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).

</dd> <dt>

**pconfigfile**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).

</dd> <dt>

**phelpfile**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt (z. b. C: \\ Drivers \\ PSCRPTUI. hlp).

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

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Herstellers angibt.

</dd> <dt>

**pszoemurl**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die URL für den Hersteller angibt.

</dd> <dt>

**pszhardwareid**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Hardware-ID für den Druckertreiber angibt.

</dd> <dt>

**pszprovider**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Anbieter des Druckertreibers angibt (z. b. "Microsoft Windows 2000").

</dd> <dt>

**pszprintprocessor**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Druck Prozessor angibt (z. b. "WinPrint").

</dd> <dt>

**pszvendorsetup**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Treiber-Setup-DLL und den Einstiegspunkt des Anbieters angibt.

</dd> <dt>

**pszzcolorprofiles**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Farbprofile angibt, die dem Treiber zugeordnet sind.

</dd> <dt>

**pszinfpath**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Pfad zur INF-Datei des Treibers im Treiber Speicher angibt. (Siehe Hinweise.) Dieser Wert muss **null** sein, wenn die Treiber \_ Informationen \_ 8 an [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md)übermittelt werden.

</dd> <dt>

**dwprinterdriverattribute**
</dt> <dd>

Attributflags für Druckertreiber. Dieser Wert muss 0 sein, wenn die Treiber \_ Informationen \_ 8 an [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md)übermittelt werden. Andernfalls kann es sich um eine beliebige Kombination der folgenden Flags handeln:



| FlagName/-Wert                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                             | Minimaler Betriebssystem                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Drucker \_ Treiber \_ Paket \_<br/> 0x00000001<br/>        | Der Druckertreiber ist Teil eines Treiber Pakets.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| Drucker \_ Treiber- \_ XPS<br/> 0x00000002<br/>                   | Der Druckertreiber unterstützt das Microsoft XPS-Format, das in [XML Paper Specification: Overview (Übersicht](/previous-versions/windows/hardware/design/dn641615(v=vs.85))) und auch in [Product Behavior, Abschnitt <27>beschrieben wird ](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| Drucker \_ Treiber- \_ Sandkasten \_ aktiviert<br/> 0x00000004<br/>      | Der Druckertreiber ist mit der [Druckertreiber Isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)kompatibel. Weitere Informationen finden Sie unter [Product Behavior, Section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| Drucker \_ Treiber \_ Klasse<br/> 0x00000008<br/>                 | Der Druckertreiber ist ein [Klassen Druckertreiber](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ abgeleiteter Druckertreiber<br/> 0x00000010<br/>               | Der Druckertreiber ist ein [abgeleiteter Druckertreiber](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| Drucker \_ Treiber \_ nicht \_ share fähig<br/> 0x00000020<br/>        | Drucker, die diesen Druckertreiber verwenden, können nicht freigegeben werden.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| Drucker \_ Treiber \_ Kategorie \_ Fax<br/> 0x00000040<br/>         | Der Druckertreiber ist für die Verwendung mit [Faxdruckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| Drucker \_ Treiber \_ - \_ kategoriedatei<br/> 0x00000080<br/>        | Der Druckertreiber ist für die Verwendung mit [Datei Druckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| Drucker \_ Treiber \_ Kategorie \_ virtuell<br/> 0x00000100<br/>     | Der Druckertreiber ist für die Verwendung mit [virtuellen Druckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ Kategorie \_ Dienst für Druckertreiber<br/> 0x00000200<br/>     | Der Druckertreiber ist für die Verwendung mit [Dienst Druckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| Drucker \_ Treiber- \_ Soft \_ Reset \_ erforderlich<br/> 0x00000400<br/> | Drucker, die diesen Druckertreiber verwenden, sollten den in der Definition der USB-Geräteklasse beschriebenen Richtlinien folgen. Weitere Informationen finden Sie unter [Product Behavior, Section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzcoredriverdependen**
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Multizeichenfolge, die alle Kern Druckertreiber angibt, von denen der Treiber abhängt. Dieser Wert muss **null** sein, wenn die **Treiber \_ Informationen \_ 8** an [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md)übermittelt werden.

</dd> <dt>

**ftmininboxdriververdate**
</dt> <dd>

Das früheste zulässige Datum aller Treiber, die mit Windows ausgeliefert wurden und von denen dieser Treiber abhängig ist.

</dd> <dt>

**dwlmininboxdriververversion**
</dt> <dd>

Die früheste zulässige Version aller Treiber, die mit Windows ausgeliefert wurden und von denen dieser Treiber abhängig ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Zeichen folgen für diese Member sind in der INF-Datei enthalten, die verwendet wird, um den Treiber hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Treiber \_ Info \_ 8W** (Unicode) und **\_ Treiber \_ Info \_ 8a** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Addprinterdriverex**](addprinterdriverex.md)
</dt> </dl>

 

