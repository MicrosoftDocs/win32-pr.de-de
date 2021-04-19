---
description: Die Funktion addprinterdriverex installiert einen lokalen oder Remote Druckertreiber und verknüpft die Konfigurations-, Daten-und Treiberdateien.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Addprinterdriverex-Funktion (winspool. h)
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
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359016"
---
# <a name="addprinterdriverex-function"></a>Addprinterdriverex-Funktion

Die Funktion **addprinterdriverex** installiert einen lokalen oder Remote Druckertreiber und verknüpft die Konfigurations-, Daten-und Treiberdateien. Neben den Funktionen von [**addprinterdriver**](addprinterdriver.md)bietet es auch Optionen, die das strikte Upgrade, das strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von Dateizeitstempeln) ermöglichen.

> [!Note]  
> Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen. Verwenden Sie stattdessen " [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md) ".

 

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

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Treiber installiert werden soll. Wenn dieser Parameter **null** ist, wird der Treiber von der Funktion auf dem lokalen Computer installiert.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der-Struktur, auf die *pdriverinfo* verweist. Dieser Wert kann 2, 3, 4, 6 oder 8 sein.

</dd> <dt>

*pdriverinfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die Druckertreiber Informationen enthält. Dies kann einer der folgenden sein:



| Wert der Ebene                                                                                       | Treiber \_ Informations \_ \* Struktur                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Treiber \_ Informationen \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Treiber \_ Info \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**Treiber \_ Info \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Treiber \_ Info \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Treiber \_ Informationen \_ 8**](driver-info-8.md)<br/> |



 

Wenn der " **pvironment** "-Member der Struktur, auf die von *pdriverinfo* verwiesen wird, **null** ist, verwendet die Funktion die aktuelle Umgebung des Aufrufers bzw. des Clients, nicht die Umgebung des Ziels bzw. des Servers.

</dd> <dt>

*dwfilecopyflags* \[ in\]
</dt> <dd>

Die Optionen zum Kopieren der Treiberdateien. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ \_ alle \_ Dateien kopieren**</dt> </dl>                | Fügen Sie den Druckertreiber hinzu, und kopieren Sie alle Dateien im Druckertreiber Verzeichnis. Die Zeitstempel der Datei werden bei dieser Option ignoriert.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD- \_ Kopie \_ aus \_ Verzeichnis**</dt> </dl> | Fügen Sie den Druckertreiber mit den voll qualifizierten Dateinamen hinzu, die in der [**Treiber \_ Info \_ 6**](driver-info-6.md) -Struktur angegeben sind. Dieses Flag wird in Verbindung mit einem der anderen kopierflags angezeigt. Wenn dieses Flag festgelegt ist, schlägt **addprinterdriverex** fehl, wenn die Dateien nicht vorhanden sind, wenn Sie in der **\_ Information \_ 6** -Struktur des Treibers vorhanden sind. Die Dateien müssen nicht in das Druckertreiber Verzeichnis des Systems kopiert werden. Siehe Hinweise.<br/> **Windows 2000:** Dieses Flag wird nicht unterstützt.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ \_ neue \_ Dateien kopieren**</dt> </dl>                | Fügen Sie den Druckertreiber hinzu, und kopieren Sie die Dateien in das Druckertreiber Verzeichnis, das neuer ist als alle entsprechenden Dateien, die zurzeit verwendet werden. Dieses Flag emuliert das Verhalten von [**addprinterdriver**](addprinterdriver.md).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**APD \_ Strict \_ Downgrade**</dt> </dl>           | Fügen Sie den Druckertreiber nur hinzu, wenn alle Dateien im Druckertreiber Verzeichnis älter sind als alle derzeit verwendeten Dateien.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**APD \_ Strict- \_ Upgrade**</dt> </dl>                 | Fügen Sie den Druckertreiber nur hinzu, wenn alle Dateien im Druckertreiber Verzeichnis neuer als alle entsprechenden Dateien sind, die zurzeit verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Wenn der Druckertreiber Probleme beim Arbeiten mit dem Betriebssystem hat, schlägt **addprinterdriverex** mit einem der folgenden Fehlercodes fehl:



| Fehlercode                      | Bedeutung                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler \_ Drucker \_ Treiber \_ blockiert | Der Treiber funktioniert nicht auf dem Betriebssystem.                                                                                                         |
| Fehler \_ Drucker \_ Treiber \_ gewarnt  | Der Treiber ist auf dem Betriebssystem unzuverlässig. Wenn jedoch \_ \_ der angemahnte Treiber für die APD-Installation \_ angegeben ist, wird der Treiber installiert, und es wird keine Warnung ausgegeben. |



 

Weitere Informationen finden Sie in den Hinweisen.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

Vor dem Aufrufen der **addprinterdriverex** -Funktion müssen alle Dateien, die für den Treiber erforderlich sind, in das Druckertreiber Verzeichnis des Systems kopiert werden. Um den Namen dieses Verzeichnisses abzurufen, rufen Sie die [**getprinterdriverdirectory**](getprinterdriverdirectory.md) -Funktion auf.

Um zu ermitteln, welche Druckertreiber derzeit installiert sind, müssen Sie die Funktion " [**enumprinterdrivers**](enumprinterdrivers.md) " aufzurufen.

Wenn der Druckertreiber erfolgreich hinzugefügt wurde, ruft die Funktion die drvdriverevent (Treiber \_ Ereignis \_ Initialize, Level, Driver \_ Info \_ \* , LPARAM)-Funktion auf, damit der Treiber alle während der Installation eines Druckertreibers erforderlichen Initialisierungen ausführen kann. Weitere Informationen zu **drvdriverevent** finden Sie im Microsoft Windows Driver Development Kit (DDK).

Der Treiber sollte während des Aufrufes **drvdriverevent** keinen UI-Befehl verwenden. Zum Ausführen von UI-bezogenen Aufträgen sollte das Installationsprogramm entweder den vendorsetup-Eintrag in der INF-Datei des Druckers verwenden, oder für Plug & Play Geräte kann das Installationsprogramm einen gerätespezifischen Co-Installer verwenden. Weitere Informationen zu vendorsetup finden Sie unter DDK.

Die Dateien, auf die in der [**Driver \_ Info \_ 6**](driver-info-6.md) -Struktur verwiesen wird, müssen sich lokal auf dem Computer befinden, von dem aus der-Befehl aufgerufen wird. Ein Dateiname kann ein UNC-Name sein, solange der UNC-Name der lokale Computer ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addprinterdriverexw** (Unicode) und **addprinterdriverexa** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Treiber \_ Informationen \_ 2**](driver-info-2.md)
</dt> <dt>

[**Treiber \_ Info \_ 3**](driver-info-3.md)
</dt> <dt>

[**Treiber \_ Info \_ 4**](driver-info-4.md)
</dt> <dt>

[**Treiber \_ Info \_ 6**](driver-info-6.md)
</dt> <dt>

[**Deleteprinterdriverex**](deleteprinterdriverex.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriverdirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

