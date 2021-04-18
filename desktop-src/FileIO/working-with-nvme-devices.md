---
description: Erfahren Sie, wie Sie in Ihrer Windows-Anwendung mit hoch Geschwindigkeits basierten nvme-Geräten arbeiten.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Arbeiten mit nvme-Laufwerken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357449"
---
# <a name="working-with-nvme-drives"></a>Arbeiten mit nvme-Laufwerken

**Anwendungsbereich:**

-   Windows 10
-   Windows Server 2016

Erfahren Sie, wie Sie in Ihrer Windows-Anwendung mit hoch Geschwindigkeits basierten nvme-Geräten arbeiten. Der Gerätezugriff wird über **StorNVMe.sys** aktiviert, der in Windows Server 2012 R2 und Windows 8.1 eingeführte in-Box-Treiber. Sie steht auch für Windows 7-Geräte über eine KB-Hotfix zur Verfügung. In Windows 10 wurden mehrere neue Features eingeführt, einschließlich eines Pass-Through-Mechanismus für herstellerspezifische nvme-Befehle und Aktualisierungen vorhandener IOCTLs.

Dieses Thema bietet einen Überblick über allgemeine Verwendungs-APIs, mit denen Sie auf nvme-Laufwerke in Windows 10 zugreifen können. Außerdem wird Folgendes beschrieben:

-   Senden eines herstellerspezifischen nvme-Befehls mit [Pass-Through](#pass-through-mechanism)
-   [Senden eines Befehls zum identifizieren, Anzeigen von Funktionen oder zum Senden von Protokoll Seiten](#protocol-specific-queries) an das nvme-Laufwerk
-   Abrufen von [Temperatur Informationen](#temperature-queries) von einem nvme-Laufwerk
-   So führen Sie Verhaltens Wechsel Befehle aus, z. b. das [Festlegen von Temperaturschwellen Werten](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>APIs für die Arbeit mit nvme-Laufwerken

Sie können die folgenden allgemeinen APIs verwenden, um auf nvme-Laufwerke in Windows 10 zuzugreifen. Diese APIs finden Sie in **winioctl. h** für Benutzermodusanwendungen und **ntddstor. h** für Kernelmodustreiber. Weitere Informationen zu Header Dateien finden Sie unter [Header Dateien](#header-files).

-   [**IOCTL \_ Storage- \_ Protokoll \_ Befehl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Verwenden Sie diese IOCTL mit der **Speicher Protokoll- \_ \_ Befehls** Struktur, um nvme-Befehle auszugeben. Diese IOCTL ermöglicht die nvme-Weiterleitung und unterstützt das Befehls Effekt Protokoll in nvme. Sie können Sie mit anbieterspezifischen Befehlen verwenden. Weitere Informationen finden Sie unter [Pass-Through-Mechanismus](#pass-through-mechanism).

-   [**Speicher \_ Protokoll \_ Befehl**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : Diese Eingabepuffer Struktur enthält ein **ReturnStatus** -Feld, das verwendet werden kann, um die folgenden Statuswerte zu melden.
    -   **Status des Speicher \_ Protokolls steht \_ \_ aus.**
    -   **Status des Speicher \_ Protokolls war \_ \_ erfolgreich.**
    -   **Fehler beim Speicher \_ Protokoll \_ Status \_**
    -   **\_ \_ \_ ungültige Anforderung für Speicher Protokoll Status \_**
    -   **Speicher \_ Protokoll \_ Status " \_ kein \_ Gerät"**
    -   **der Speicher \_ Protokoll \_ Status ist \_ ausgelastet.**
    -   **\_ \_ Status \_ Daten \_ Überlauf des Speicher Protokolls**
    -   **Speicher \_ Protokoll \_ Status \_ unzureichende \_ Ressourcen**
    -   **Speicher \_ Protokoll \_ Status \_ \_ wird nicht unterstützt.**
-   [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Verwenden Sie diese IOCTL mit der **Speicher \_ Eigenschafts \_ Abfrage** -Struktur, um Geräteinformationen abzurufen. Weitere Informationen finden Sie unter [Protokoll spezifische Abfragen](#protocol-specific-queries) und [Temperatur Abfragen](#temperature-queries).

-   [**Speicher \_ Eigenschaften \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : Diese Struktur enthält die Felder **PropertyId** und **AdditionalParameters** , um die Daten anzugeben, die abgefragt werden sollen. Verwenden Sie in der erfasste **PropertyId** die **Speicher eigen \_ schafts- \_ ID** -Enumeration, um den Datentyp anzugeben. Verwenden Sie das **AdditionalParameters** -Feld, um je nach Datentyp weitere Details anzugeben. Verwenden Sie für Protokoll spezifische Daten die **Speicher \_ Protokoll \_ spezifische \_ Daten** Struktur im Feld **AdditionalParameters** . Verwenden Sie für Temperaturdaten die Struktur der **Speicher \_ Temperatur \_ Informationen** im Feld **AdditionalParameters** .
-   [**Speicher \_ Eigen schafts- \_ ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : Diese Enumeration enthält neue Werte, mit denen die **IOCTL- \_ Speicher \_ Abfrage \_ Eigenschaft** Protokoll spezifische und Temperatur Informationen abrufen kann.

    -   **Storageadapterprotocolspecificproperty**
    -   **Storagedeviceprotocolspecificproperty**

    Verwenden Sie eine dieser Protokoll spezifischen Eigenschaften-IDs in Kombination mit **Speicher \_ Protokoll \_ spezifischen \_ Daten** , um Protokoll spezifische Daten in der [**\_ \_ Daten \_ deskriptorstruktur des Speicher Protokolls**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) abzurufen.

    -   **Storageadaptertemperatureproperty**
    -   **Storagedevicetemperatureproperty**

    Verwenden Sie eine dieser Temperatureigenschaften-IDs, um Temperaturdaten in [**der \_ \_ \_ deskriptorstruktur der Speichertemperatur Daten**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) abzurufen.

-   [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Rufen Sie nvme-spezifische Daten ab, wenn diese Struktur für das **AdditionalParameters** -Feld der **Speicher \_ Eigenschafts \_ Abfrage** verwendet wird und ein [**\_ \_ nvme \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) -Enumerationswert für das Speicher Protokoll angegeben wird. Verwenden Sie einen der folgenden Werte für den **\_ \_ nvme- \_ \_ Datentyp des Speicher Protokolls** im **DataType** -Feld der **Speicher \_ Protokoll \_ spezifischen \_ Daten** Struktur:

    -   Verwenden Sie **nvmedatatypeidentify** zum Ermitteln von Controller Daten oder zum Identifizieren von Namespace Daten.
    -   Verwenden Sie **nvmedatatypelogpage** zum Aufrufen von Protokoll Seiten (einschließlich intelligenter/Integritäts Daten).
    -   Verwenden Sie **nvmedatatygfeature** , um die Features des nvme-Laufwerks zu erhalten.

-   [**Speicher \_ Temperatur \_ Informationen**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : Diese Struktur wird verwendet, um bestimmte Temperaturdaten aufzunehmen. Es wird im **\_ \_ Daten \_ Deskriptor Storage temerklatur** verwendet, um die Ergebnisse einer Temperatur Abfrage zurückzugeben.

-   [**IOCTL \_ \_ \_ \_ Schwellenwert für die Speicher festgelegte Temperatur**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Verwenden Sie diese IOCTL mit der Struktur der **Speicher \_ Temperatur \_ Schwelle** , um Temperaturschwellen Werte festzulegen Weitere Informationen finden Sie unter [Behavior Changing Commands](#behavior-changing-commands).

-   [**Speicher \_ Temperatur \_ Schwellenwert**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : Diese Struktur wird als Eingabepuffer verwendet, um den Temperaturschwellen Wert anzugeben. Das **overthreshold** -Feld (boolescher Wert) gibt an, ob das **Schwellen** Wert Feld den over-Schwellenwert oder nicht (andernfalls der unter Schwellenwert) ist.

## <a name="pass-through-mechanism"></a>Pass-Through-Mechanismus

Befehle, die nicht in der nvme-Spezifikation definiert sind, sind für das Host Betriebssystem am schwierigsten – der Host hat keinen Einblick in die Auswirkungen der Befehle auf das Zielgerät, die verfügbar gemachte Infrastruktur (Namespaces/Blockgrößen) und das zugehörige Verhalten.

Um solche gerätespezifischen Befehle über den Windows-Speicher Stapel zu übertragen, können mit einem neuen Pass-Through-Mechanismus herstellerspezifische Befehle weitergeleitet werden. Diese Pass-Through-Pipe bietet auch Unterstützung bei der Entwicklung von Verwaltungs-und TestTools. Dieser Pass-Through-Mechanismus erfordert jedoch die Verwendung des Befehls Effekt Protokolls. Darüber hinaus erfordert StoreNVMe.sys, dass alle Befehle, nicht nur Pass-Through-Befehle, im Befehls Effekt Protokoll beschrieben werden.

> [!IMPORTANT]
> StorNVMe.sys und Storport.sys blockieren jeden Befehl an ein Gerät, wenn es nicht im Befehls Effekt Protokoll beschrieben wird.

 

### <a name="supporting-the-command-effects-log"></a>Unterstützen des Befehls Effekt Protokolls

Das Befehls Effekt Protokoll (wie unter "Befehle unterstützt" und "Effects", Abschnitt 5.10.1.5 of [nvme Specification 1,2](https://nvmexpress.org/specifications)), ermöglicht die Beschreibung der Auswirkungen der herstellerspezifischen Befehle sowie von Spezifikations definierten Befehlen. Dadurch wird sowohl die Validierung der Befehls Unterstützung als auch die Befehls Verhaltens Optimierung ermöglicht und sollte daher für alle Befehle implementiert werden, die das Gerät unterstützt. Die folgenden Bedingungen beschreiben das Ergebnis der Übermittlung des Befehls auf der Grundlage des Befehls Effekt-Protokoll Eintrags.

Für jeden bestimmten Befehl, der im Befehls Effekt Protokoll beschrieben wird...

**Während**:

-   Der unterstützte Befehl (csupp) ist auf "1" festgelegt, was bedeutet, dass der Befehl vom Controller unterstützt wird (Bit 01).

    > [!Note]  
    > Wenn csupp auf "0" festgelegt ist (was bedeutet, dass der Befehl nicht unterstützt wird), wird der Befehl blockiert.

     

**Und wenn** Folgendes festgelegt ist:

-   Die Controller Funktionsänderung (CCC) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Controller Funktionen ändern kann (Bit 04).

-   Die Namespace-Inventur Änderung (NIC) ist auf "1" festgelegt, was bedeutet, dass der Befehl möglicherweise die Anzahl oder die Funktionen für mehrere Namespaces (Bit 03) ändert.

-   Die Namespace-Funktionsänderung (NCC) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Funktionen eines einzelnen Namespace ändern kann (Bit 02).

-   Die Befehls Übermittlung und-Ausführung (CSE) ist auf 001b oder 010b festgelegt, was bedeutet, dass der Befehl gesendet werden kann, wenn kein anderer ausstehender Befehl für denselben oder einen Namespace vorhanden ist, und dass ein anderer Befehl erst an denselben oder einen Namespace übermittelt werden soll, wenn dieser Befehl vollständig ist (Bits 18:16).

**Anschließend** wird der Befehl als einziger Befehl an den Adapter gesendet, der für den Adapter aussteht.

**Andernfalls**:

-   Die Befehls Übermittlung und-Ausführung (CSE) ist auf 001b festgelegt, was bedeutet, dass der Befehl übermittelt werden kann, wenn es keinen anderen ausstehenden Befehl für denselben Namespace gibt und dass ein anderer Befehl erst an denselben Namespace übermittelt werden soll, wenn dieser Befehl vollständig ist (Bits 18:16).

**Anschließend** wird der Befehl als einziger Befehl gesendet, der für das logische Gerätenummern Objekt (Logical Unit Number Object, LUN) aussteht.

**Andernfalls** wird der Befehl mit anderen ausstehenden Befehlen ohne Behinderung gesendet. Wenn z. b. ein Hersteller spezifischer Befehl an das Gerät gesendet wird, um statistische Informationen abzurufen, die nicht Spezifikations definiert sind, besteht keine Gefahr, das Verhalten des Geräts oder die Fähigkeit zum Ausführen von I/O-Befehlen zu ändern. Solche Anforderungen können parallel zu e/a-Vorgängen gewartet werden, und es wäre keine Pause-Fortsetzung erforderlich.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Verwenden des IOCTL- \_ Speicher \_ Protokoll \_ Befehls zum Senden von Befehlen

Der Pass-Through-Befehl kann mit dem in Windows 10 eingeführten [**IOCTL- \_ Speicher \_ Protokoll \_ Befehl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)durchgeführt werden. Diese IOCTL wurde so entworfen, dass Sie ein ähnliches Verhalten wie die vorhandene SCSI-und ATA-Pass-Through-IOCTLs hat, um einen eingebetteten Befehl an das Zielgerät zu senden. Über diese IOCTL kann Pass-Through an ein Speichergerät gesendet werden, einschließlich eines nvme-Laufwerks.

In nvme lässt z. b. die IOCTL das Senden der folgenden Befehls Codes zu.

-   Anbieterspezifische Administrator Befehle (C0h – FFH)
-   Anbieterspezifische nvme-Befehle (80he – FFH)

Verwenden Sie wie bei allen anderen IOCTLs [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) , um den Pass-Through-ioctl zu senden. Die IOCTL wird mithilfe der in " **ntddstor. h**" gefundenen Eingabe-/pufferstruktur des [**Speicher \_ Protokoll \_ Befehls**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) aufgefüllt. Füllen Sie das **Befehls** Feld mit dem herstellerspezifischen Befehl auf.


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



Der zu sendende herstellerspezifische Befehl sollte in dem oben markierten Feld aufgefüllt werden. Beachten Sie, dass das Befehls Effekt Protokoll für Pass-Through-Befehle implementiert werden muss. Insbesondere müssen diese Befehle im Befehls Effekt Protokoll als unterstützt gemeldet werden (Weitere Informationen finden Sie im vorherigen Abschnitt). Beachten Sie auch, dass PRP-Felder Treiber spezifisch sind, sodass Anwendungen, die Befehle senden, Sie als 0 belassen können.

Zum Schluss ist diese Pass-Through-ioctl zum Senden Hersteller spezifischer Befehle gedacht. Zum Senden anderer nvme-Befehle (Administrator oder nicht Anbieter), wie z. b. "ermitteln", sollte diese Pass-Through-ioctl nicht verwendet werden. Beispielsweise sollte die **IOCTL \_ Storage \_ Query- \_ Eigenschaft** zum identifizieren oder erhalten von Protokoll Seiten verwendet werden. Weitere Informationen finden Sie im nächsten Abschnitt [Protokoll spezifische Abfragen](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Aktualisieren Sie die Firmware nicht durch den Pass-Through-Mechanismus.

Firmwaredownloads und aktivierungsbefehle sollten nicht mithilfe von Pass-Through gesendet werden. **IOCTL \_ Der Speicher \_ Protokoll \_ Befehl** sollte nur für herstellerspezifische Befehle verwendet werden.

Verwenden Sie stattdessen den folgenden allgemeinen Speicher-IOCTLs (eingeführt in Windows 10), um Anwendungen zu vermeiden, die die SCSI- \_ Mini Port-Version der Firmware ioctl direkt verwenden. Speicher Treiber übersetzen die IOCTL entweder in einen SCSI-Befehl oder die SCSI- \_ Mini PORTVERSION der IOCTL in den Mini Port.

Diese IOCTLs werden zum Entwickeln von Firmwareupdates in Windows 10 und Windows Server 2016 empfohlen:

-   [**IOCTL- \_ Speicher \_ Firmware \_ get \_ Info**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**Download der IOCTL- \_ Speicher \_ Firmware \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**IOCTL- \_ Speicher \_ Firmware \_ aktivieren**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Um Speicherinformationen zu erhalten und Firmware zu aktualisieren, unterstützt Windows auch PowerShell-Cmdlets, um dies schnell zu erreichen:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Zum Aktualisieren der Firmware auf dem nvme in Windows 8.1 verwenden Sie die IOCTL \_ SCSI \_ Miniport- \_ Firmware. Diese IOCTL wurde nicht auf Windows 7 zurückportiert. Weitere Informationen finden Sie [unter Aktualisieren der Firmware für ein nvme-Gerät in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Zurückgeben von Fehlern durch den Pass-Through-Mechanismus

Wenn ein Befehl bzw. eine Anforderung an den Mini Port oder das Gerät gesendet wird, gibt die IOCTL-Datei (ähnlich wie SCSI und ATA Pass-Through IOCTLs) zurück, wenn Sie erfolgreich war oder nicht. In der [**Speicher \_ Protokoll- \_ Befehls**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) Struktur gibt ioctl den Status über das Feld **ReturnStatus** zurück.

### <a name="example-sending-a-vendor-specific-command"></a>Beispiel: Senden eines herstellerspezifischen Befehls

In diesem Beispiel wird ein beliebiger Hersteller spezifischer Befehl (0xFF) per Pass-Through an ein nvme-Laufwerk gesendet. Der folgende Code ordnet einen Puffer zu, Initialisiert eine Abfrage und sendet den Befehl dann über DeviceIoControl an das Gerät.


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



In diesem Beispiel wird davon ausgegangen, dass `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` der Befehl dem Gerät erfolgreich war.

## <a name="protocol-specific-queries"></a>Protokoll spezifische Abfragen

Windows 8.1 hat die [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) zum Abrufen von Daten eingeführt. In Windows 10 wurde die IOCTL verbessert, um häufig angeforderte nvme **-Funktionen** zu unterstützen, wie z. b. " **Get Log Pages**" und " **Get Features**". Dies ermöglicht das Abrufen von nvme-spezifischen Informationen zu Überwachungs-und Inventur Zwecken.

Der Eingabepuffer für die IOCTL-, [**Storage- \_ Eigenschafts \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (aus Windows 10) wird hier dargestellt.


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Wenn Sie die [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) verwenden, um nvme-Protokoll spezifische Informationen im [**Speicher \_ Protokoll \_ Daten \_ Deskriptor**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)abzurufen, konfigurieren Sie die Abfrage Struktur der [**Speicher \_ Eigenschaft \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) wie folgt:

-   Weisen Sie einen Puffer zu, der sowohl eine [**Speicher \_ Eigenschaften \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) als auch eine [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur enthält.

-   Legen Sie das Feld **PropertyId** auf **storageadapterprotocolspecificproperty** oder **storagedeviceprotocolspecificproperty** für eine Controller-oder Geräte-bzw. Namespace Anforderung fest.

-   Legen Sie das Feld **QueryType** auf **propertystandardquery** fest.

-   Füllen Sie die [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur mit den gewünschten Werten aus. Der Anfang der **Speicher \_ Protokoll \_ spezifischen \_ Daten** ist das **AdditionalParameters** -Feld der [**Speicher \_ Eigenschafts \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

Die [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur (aus Windows 10) wird hier dargestellt.


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



Um einen Typ von nvme-Protokoll spezifischen Informationen anzugeben, konfigurieren Sie die [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur wie folgt:

-   Legen Sie das Feld **ProtocolType** auf **protocoltypvme** fest.

-   Legen Sie das Feld **DataType** auf einen Enumerationswert fest, der vom [**\_ \_ nvme- \_ \_ Datentyp des Speicher Protokolls**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)definiert wird:

    -   Verwenden Sie **nvmedatatypeidentify** zum Ermitteln von Controller Daten oder zum Identifizieren von Namespace Daten.
    -   Verwenden Sie **nvmedatatypelogpage** zum Aufrufen von Protokoll Seiten (einschließlich intelligenter/Integritäts Daten).
    -   Verwenden Sie **nvmedatatygfeature** , um die Features des nvme-Laufwerks zu erhalten.

Wenn **protocoltypvme** als **ProtocolType** verwendet wird, können Abfragen für Protokoll spezifische Informationen parallel zu anderen e/a-Vorgängen auf dem nvme-Laufwerk abgerufen werden.

Die folgenden Beispiele veranschaulichen nvme-Protokoll spezifische Abfragen.

### <a name="example-nvme-identify-query"></a>Beispiel: nvme-Abfrage

In diesem Beispiel wird die **identifikanungsanforderung** an ein nvme-Laufwerk gesendet. Der folgende Code initialisiert die Abfrage Datenstruktur und sendet dann den Befehl über DeviceIoControl an das Gerät.


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



Beachten Sie, dass der Aufrufer einen einzelnen Puffer mit einer Speicher \_ Eigenschafts \_ Abfrage und der Größe der \_ spezifischen Speicher Protokolldaten zuordnen muss \_ \_ . In diesem Beispiel wird derselbe Puffer für die Eingabe und die Ausgabe der Eigenschaften Abfrage verwendet. Daher hat der zugewiesene Puffer die Größe "Feld \_ Offset (Speicher \_ Eigenschaften \_ Abfrage, AdditionalParameters) + sizeof (Speicher \_ Protokoll \_ spezifische \_ Daten) + nvme \_ Max \_ log \_ size". Obwohl separate Puffer sowohl für die Eingabe als auch für die Ausgabe reserviert werden können, empfiehlt sich die Verwendung eines einzelnen Puffers, um nvme-bezogene Informationen abzufragen.

### <a name="example-nvme-get-log-pages-query"></a>Beispiel: nvme Get Log Pages Query

In diesem Beispiel, basierend auf dem vorherigen, wird die Anforderung _ *Get Log Pages** an ein nvme-Laufwerk gesendet. Der folgende Code bereitet die Abfrage Datenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Beispiel: nvme Get Features Query

In diesem Beispiel, basierend auf dem vorherigen, wird die Anforderung _ *Get Features** an ein nvme-Laufwerk gesendet. Der folgende Code bereitet die Abfrage Datenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a>Protokoll spezifischer Satz

Aus Windows 10 19h1 wurde die IOCTL_STORAGE_SET_PROPERTY verbessert, um die Funktionen von nvme-Sets zu unterstützen.

Der Eingabepuffer für das IOCTL_STORAGE_SET_PROPERTY wird hier angezeigt:

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

Wenn Sie IOCTL_STORAGE_SET_PROPERTY verwenden, um die nvme-Funktion festzulegen, konfigurieren Sie die STORAGE_PROPERTY_SET Struktur wie folgt:

-   Zuordnen eines Puffers, der sowohl eine STORAGE_PROPERTY_SET als auch eine STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur enthalten kann;
-   Legen Sie das Feld PropertyId auf storageadapterprotocolspecificproperty oder storagedeviceprotocolspecificproperty für eine Controller-oder Geräte-bzw. Namespace Anforderung fest.
-   Füllen Sie die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur mit den gewünschten Werten aus. Der Anfang des STORAGE_PROTOCOL_SPECIFIC_DATA_EXT ist das AdditionalParameters-Feld STORAGE_PROPERTY_SET.

Die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur wird hier dargestellt.

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

Um einen Typ der festzulegenden nvme-Funktion anzugeben, konfigurieren Sie die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur wie folgt:
-   Legen Sie das Feld ProtocolType auf protocoltypvme fest.
-   Legen Sie das Feld DataType auf den Enumerationswert nvmedatatypfeature fest, der durch STORAGE_PROTOCOL_NVME_DATA_TYPE definiert wird.

In den folgenden Beispielen wird die nvme-Funktionsgruppe veranschaulicht.

### <a name="example-nvme-set-features"></a>Beispiel: nvme-Set-Funktionen

In diesem Beispiel wird die Anforderung zum Festlegen von Features an ein nvme-Laufwerk gesendet. Der folgende Code bereitet die Set Data-Struktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a>Temperatur Abfragen

In Windows 10 kann die [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) auch verwendet werden, um Temperaturdaten von nvme-Geräten abzufragen.

Um Temperatur Informationen von einem nvme-Laufwerk im [**Speicher \_ Temperaturdaten \_ - \_ Deskriptor**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)abzurufen, konfigurieren Sie die Abfrage Struktur der [**Speicher \_ Eigenschaft \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) wie folgt:

-   Weisen Sie einen Puffer zu, der [**eine \_ \_ Abfrage Struktur der Speicher Eigenschaft**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) enthalten kann.

-   Legen Sie das Feld **PropertyId** auf **storageadaptertemperatureproperty** oder **storagedevicetemperatureproperty** für eine Controller-oder Geräte-bzw. Namespace Anforderung fest.

-   Legen Sie das Feld **QueryType** auf **propertystandardquery** fest.

Die Struktur der [**Speicher \_ Temperatur \_ Informationen**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (aus Windows 10) wird hier dargestellt.


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a>Verhaltens Wechsel Befehle

Befehle, die Geräte Attribute bearbeiten oder möglicherweise Auswirkungen auf das Geräteverhalten haben, können dem Betriebssystem erschwert werden. Wenn sich Geräte Attribute zur Laufzeit ändern, während e/a-Vorgänge verarbeitet werden, können Synchronisierungs-oder Daten Integritäts Probleme auftreten, wenn Sie nicht ordnungsgemäß behandelt werden.

Der nvme **-Befehl "Set-Features** " ist ein gutes Beispiel für einen Verhaltens Wechsel. Sie ermöglicht die Änderung des-Mechanismus für die Vermittlung und die Einstellung von Temperaturschwellen Werten. Um sicherzustellen, dass in-Flight-Daten nicht gefährdet sind, wenn verhaltensbezogene Set-Befehle gesendet werden, hält Windows alle e/a-Vorgänge für das nvme-Gerät an, entleert Warteschlangen und leert Puffer. Nachdem der SET-Befehl erfolgreich ausgeführt wurde, wird die e/a-Vorgänge fortgesetzt (sofern möglich). Wenn die e/a-Vorgänge nicht fortgesetzt werden können, ist möglicherweise eine Geräte Zurücksetzung erforderlich.

### <a name="setting-temperature-thresholds"></a>Festlegen von Temperaturschwellen Werten

In Windows 10 wurde der [**IOCTL- \_ Speicher \_ Satz \_ Temperatur \_ Schwellenwert**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)eingeführt, eine ioctl zum erhalten und Festlegen von Temperaturschwellen Werten. Sie können es auch verwenden, um die aktuelle Temperatur des Geräts zu erhalten. Der Eingabe-/Ausgabepuffer für diese IOCTL ist die [**Speicher \_ Temperatur \_ Informations**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) Struktur aus dem vorherigen Code Abschnitt.

### <a name="example-setting-over-threshold-temperature"></a>Beispiel: Festlegen der über-Schwellenwert Temperatur

In diesem Beispiel ist die Temperatur eines nvme-Laufwerks über Schwellenwert festgelegt. Mit dem folgenden Code wird der Befehl vorbereitet und dann über DeviceIoControl an das Gerät gesendet.


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a>Festlegen Hersteller spezifischer Features

Ohne das Befehls Effekt Protokoll hat der Treiber keine Kenntnis von den Auswirkungen des Befehls. Aus diesem Grund ist das Befehls Effekt Protokoll erforderlich. Dadurch kann das Betriebssystem ermitteln, ob ein Befehl eine hohe Auswirkung hat und ob er parallel mit anderen Befehlen an das Laufwerk gesendet werden kann.

Das Befehls Effekt Protokoll ist noch nicht genau genug, um anbieterspezifische **Set-Features** -Befehle einzubeziehen. Aus diesem Grund ist es noch nicht möglich, anbieterspezifische **Set-Features-** Befehle zu senden. Es ist jedoch möglich, den zuvor erläuterten Pass-Through-Mechanismus zum Senden Hersteller spezifischer Befehle zu verwenden. Weitere Informationen finden Sie unter [Pass-Through-Mechanismus](#pass-through-mechanism).

## <a name="header-files"></a>Headerdateien

Die folgenden Dateien sind für die nvme-Entwicklung relevant. Diese Dateien sind im [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads)enthalten.



| Headerdatei    | BESCHREIBUNG                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor. h** | Definiert Konstanten und Typen für den Zugriff auf die Speicher Klassen Treiber aus dem Kernel Modus.   |
| **nvme. h**     | Für andere nvme-bezogene Datenstrukturen.                                                 |
| **winioctl. h** | Für allgemeine Win32-ioctl-Definitionen, einschließlich Speicher-APIs für Benutzermodusanwendungen. |



 

 

 
