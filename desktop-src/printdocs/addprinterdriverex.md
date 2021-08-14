---
description: Die AddPrinterDriverEx-Funktion installiert einen lokalen oder Remotedruckertreiber und verknüpft die Konfigurations-, Daten- und Treiberdateien.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: AddPrinterDriverEx-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 00bd65ad415a97bbab825e4a13c8ad985d1d7f9b79d7b46e3f8f7ea6b5e5f0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868809"
---
# <a name="addprinterdriverex-function"></a>AddPrinterDriverEx-Funktion

Die **AddPrinterDriverEx-Funktion** installiert einen lokalen oder Remotedruckertreiber und verknüpft die Konfigurations-, Daten- und Treiberdateien. Neben den Funktionen von [**AddPrinterDriver**](addprinterdriver.md)verfügt es auch über Optionen, die ein striktes Upgrade, ein striktes Downgrade, nur das Kopieren neuerer Dateien und das Kopieren aller Dateien (unabhängig von Dateizeitstempeln) ermöglichen.

> [!Note]  
> Das Installieren eines Druckertreibers ohne Treiberpaket wird nicht mehr empfohlen. Verwenden [**Sie stattdessen InstallPrinterDriverFromPackage.**](installprinterdriverfrompackage.md)

 

## <a name="syntax"></a>Syntax


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Servers angibt, auf dem der Treiber installiert werden soll. Wenn dieser Parameter **NULL ist,** installiert die Funktion den Treiber auf dem lokalen Computer.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Version der -Struktur, auf die *pDriverInfo* verweist. Dieser Wert kann 2, 3, 4, 6 oder 8 sein.

</dd> <dt>

*pDriverInfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine -Struktur, die Druckertreiberinformationen enthält. Dies kann eine der folgenden Sein.



| Wert von Level                                                                                       | DRIVER \_ \_ \* INFO-Struktur                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 8**](driver-info-8.md)<br/> |



 

Wenn der **pEnvironment-Member** der Struktur, auf die *von pDriverInfo* verwiesen wird, **NULL** ist, verwendet die Funktion die aktuelle Umgebung des Aufrufers/Clients, nicht die Umgebung des Ziels/Servers.

</dd> <dt>

*dwFileCopyFlags* \[ In\]
</dt> <dd>

Die Optionen zum Kopieren der Treiberdateien. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**\_APD– KOPIEREN \_ ALLER \_ DATEIEN**</dt> </dl>                | Fügen Sie den Druckertreiber hinzu, und kopieren Sie alle Dateien im Verzeichnis printer-driver. Die Dateizeitstempel werden mit dieser Option ignoriert.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ COPY \_ FROM \_ DIRECTORY**</dt> </dl> | Fügen Sie den Druckertreiber mithilfe der vollqualifizierten Dateinamen hinzu, die in der [**DRIVER \_ INFO \_ 6-Struktur angegeben**](driver-info-6.md) sind. Dieses Flag wird in Verbindung mit einem der anderen Kopierflags ORed verwendet. Wenn dieses Flag festgelegt ist, kann **AddPrinterDriverEx** nicht verwendet werden, wenn die Dateien nicht dort vorhanden sind, wo sie von der **DRIVER INFO \_ \_ 6-Struktur als** vorhanden angegeben werden. Die Dateien müssen nicht in das Druckertreiberverzeichnis des Systems kopiert werden. Weitere Informationen finden Sie in den Anmerkungen.<br/> **Windows 2000:** Dieses Flag wird nicht unterstützt.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**\_APD: KOPIEREN \_ NEUER \_ DATEIEN**</dt> </dl>                | Fügen Sie den Druckertreiber hinzu, und kopieren Sie die Dateien im Druckertreiberverzeichnis, die neuer sind als alle entsprechenden Dateien, die derzeit verwendet werden. Dieses Flag emuliert das Verhalten von [**AddPrinterDriver**](addprinterdriver.md).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**APD \_ STRICT \_ DOWNGRADE**</dt> </dl>           | Fügen Sie den Druckertreiber nur hinzu, wenn alle Dateien im Verzeichnis printer-driver älter sind als die entsprechenden dateien, die derzeit verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**APD \_ STRICT \_ UPGRADE**</dt> </dl>                 | Fügen Sie den Druckertreiber nur hinzu, wenn alle Dateien im Druckertreiberverzeichnis neuer sind als alle entsprechenden dateien, die derzeit verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Wenn bekannt ist, dass der Druckertreiber Probleme beim Arbeiten mit dem Betriebssystem hat, tritt bei **AddPrinterDriverEx** ein Fehler mit einem der folgenden Fehlercodes auf:



| Fehlercode                      | Bedeutung                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLER: \_ \_ DRUCKERTREIBER \_ BLOCKIERT | Der Treiber funktioniert unter dem Betriebssystem nicht.                                                                                                         |
| FEHLER: \_ \_ DRUCKERTREIBER \_ GEWARNT  | Der Treiber ist vom Betriebssystem unzuverlässig. Wenn jedoch APD INSTALL WARNING DRIVER angegeben ist, wird der Treiber \_ \_ \_ installiert, und es wird keine Warnung angezeigt. |



 

Weitere Informationen finden Sie in den Hinweisen.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu kommen, dass die Anwendung nicht reagiert.

 

Der Aufrufer muss über [seLoadDriverPrivilege verfügen.](/windows/desktop/SecAuthZ/authorization-constants)

Vor dem Aufrufen **der AddPrinterDriverEx-Funktion** müssen alle vom Treiber benötigten Dateien in das Druckertreiberverzeichnis des Systems kopiert werden. Rufen Sie die [**GetPrinterDriverDirectory-Funktion**](getprinterdriverdirectory.md) auf, um den Namen dieses Verzeichnisses abzurufen.

Um zu bestimmen, welche Druckertreiber derzeit installiert sind, rufen Sie die [**EnumPrinterDrivers-Funktion**](enumprinterdrivers.md) auf.

Wenn der Druckertreiber erfolgreich hinzugefügt wurde, ruft die Funktion die Funktion DrvDriverEvent (DRIVER \_ EVENT \_ INITIALIZE, Level, DRIVER \_ INFO , \_ \* lparam ) auf, damit der Treiber alle Initialisierungen ausführen kann, die während der Installation eines Druckertreibers erforderlich sind. Weitere Informationen zu **DrvDriverEvent finden** Sie im Microsoft Windows Driver Development Kit (DDK).

Der Treiber sollte während des Aufrufs von **DrvDriverEvent keinen Benutzeroberflächenaufruf verwenden.** Für benutzeroberflächenbezogene Aufträge sollte das Installationsprogramm entweder den Eintrag VendorSetup in der INF-Datei des Druckers verwenden oder für Plug & Play-Geräte ein gerätespezifisches Co-Installationsprogramm verwenden. Weitere Informationen zu VendorSetup finden Sie im DDK.

Die Dateien, auf die in der [**DRIVER \_ INFO \_ 6-Struktur**](driver-info-6.md) verwiesen wird, müssen lokal auf dem Computer sein, von dem aus der Aufruf erfolgt. Ein Dateiname kann ein UNC-Name sein, solange der UNC-Name der lokale Computer ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrinterDriverExW** (Unicode) und **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

