---
description: Erfahren Sie, wie Sie mit NVMe-Hochgeschwindigkeitsgeräten aus Ihrer Windows arbeiten.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Arbeiten mit NVMe-Laufwerken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 425516946d1e76e5c01f6ae5d11f104244f85ce0
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436275"
---
# <a name="working-with-nvme-drives"></a>Arbeiten mit NVMe-Laufwerken

**Anwendungsbereich:**

-   Windows 10
-   Windows Server 2016

Erfahren Sie, wie Sie mit NVMe-Hochgeschwindigkeitsgeräten aus Ihrer Windows arbeiten. Der Gerätezugriff wird über **StorNVMe.sys** aktiviert. Dabei handelt es sich um den in Windows Server 2012 R2 eingeführten Windows 8.1. Es ist auch für 7 Windows über einen KB-Hotfix verfügbar. In Windows 10 wurden mehrere neue Features eingeführt, einschließlich eines Pass-Through-Mechanismus für herstellerspezifische NVMe-Befehle und Updates vorhandener IOCTLs.

Dieses Thema bietet eine Übersicht über allgemeine APIs, die Sie für den Zugriff auf NVMe-Laufwerke in Windows 10. Außerdem wird Beschrieben:

-   Senden eines anbieterspezifischen NVMe-Befehls mit [Pass-Through](#pass-through-mechanism)
-   Senden eines [Befehls "Identify", "Get Features" oder "Get Log Pages"](#protocol-specific-queries) an das NVMe-Laufwerk
-   Abrufen von [Temperaturinformationen von](#temperature-queries) einem NVMe-Laufwerk
-   Ausführen von Befehlen zum Ändern des Verhaltens, z. B. [festlegen von Temperaturschwellenwerte](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>APIs für die Arbeit mit NVMe-Laufwerken

Sie können die folgenden allgemeinen APIs verwenden, um auf NVMe-Laufwerke in Windows 10. Diese APIs finden Sie in **winioctl.h** für Benutzermodusanwendungen und **ntddstor.h** für Kernelmodustreiber. Weitere Informationen zu Headerdateien finden Sie unter [Headerdateien.](#header-files)

-   [**IOCTL \_ \_ \_ SPEICHERPROTOKOLLBEFEHL:**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) Verwenden Sie diese IOCTL mit der **\_ SPEICHERPROTOKOLL-BEFEHLsstruktur, \_** um NVMe-Befehle aus auszuführen. Diese IOCTL ermöglicht nvme-Pass-Through und unterstützt das Command Effects-Protokoll in NVMe. Sie können es mit herstellerspezifischen Befehlen verwenden. Weitere Informationen finden Sie unter [Pass-Through-Mechanismus](#pass-through-mechanism).

-   [**STORAGE \_ \_PROTOKOLLBEFEHL:**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) Diese Eingabepufferstruktur enthält ein **ReturnStatus-Feld,** das verwendet werden kann, um die folgenden Statuswerte zu melden.
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS \_ AUSSTEHEND**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS \_ ERFOLGREICH**
    -   **\_ \_ \_ SPEICHERPROTOKOLLSTATUSFEHLER**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS \_ UNGÜLTIGE \_ ANFORDERUNG**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS KEIN \_ \_ GERÄT**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS \_ AUSGELASTET**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUSDATEN \_ \_ ÜBERLAUF**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS UNZUREICHENDE \_ \_ RESSOURCEN**
    -   **\_ \_ SPEICHERPROTOKOLLSTATUS WIRD NICHT \_ \_ UNTERSTÜTZT**
-   [**IOCTL \_ STORAGE \_ QUERY \_ PROPERTY:**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) Verwenden Sie diese IOCTL mit der **STORAGE PROPERTY \_ \_ QUERY-Struktur,** um Geräteinformationen abzurufen. Weitere Informationen finden Sie unter [Protokollspezifische Abfragen und](#protocol-specific-queries) [Temperaturabfragen.](#temperature-queries)

-   [**STORAGE \_ PROPERTY \_ QUERY:**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) Diese Struktur enthält die **Felder PropertyId** und **AdditionalParameters,** um die daten anzugeben, die abgefragt werden sollen. Verwenden Sie **im Feld PropertyId** die **STORAGE PROPERTY \_ \_ ID-Enumeration,** um den Datentyp anzugeben. Verwenden Sie **das Feld AdditionalParameters,** um je nach Datentyp weitere Details anzugeben. Verwenden Sie für protokollspezifische Daten die **STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA-Struktur** im **Feld AdditionalParameters.** Verwenden Sie für Temperaturdaten die **STORAGE \_ TEMPERATURE \_ INFO-Struktur** im **Feld AdditionalParameters.**
-   [**STORAGE \_ PROPERTY \_ ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : Diese Enumeration enthält neue Werte, mit denen **IOCTL \_ STORAGE QUERY \_ \_ PROPERTY** protokollspezifische und Temperaturinformationen abrufen kann.

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    Verwenden Sie eine dieser protokollspezifischen Eigenschaften-IDs in Kombination mit **STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA,** um protokollspezifische Daten in der [**STORAGE PROTOCOL DATA \_ \_ \_ DESCRIPTOR-Struktur abzurufen.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Verwenden Sie eine dieser Temperatureigenschafts-IDs, um Temperaturdaten in der [**\_ \_ \_ SPEICHERTEMPERATURDATEN-DESKRIPTORstruktur abzurufen.**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)

-   [**STORAGE \_ PROTOKOLLSPEZIFISCHE \_ \_ DATEN:**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Rufen Sie NVMe-spezifische Daten ab, wenn diese Struktur für das **Feld AdditionalParameters** von **STORAGE PROPERTY \_ \_ QUERY** verwendet wird und ein [**STORAGE PROTOCOL \_ \_ NVME DATA \_ TYPE-Aufzählwert \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) angegeben wird. Verwenden Sie einen der folgenden **STORAGE \_ PROTOCOL \_ NVME DATA \_ \_ TYPE-Werte** im **Feld DataType** der **STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA-Struktur:**

    -   Verwenden **Sie NVMeDataTypeIdentify zum** Ermitteln von Controllerdaten oder Identifizieren von Namespacedaten.
    -   Verwenden **Sie NVMeDataTypeLogPage,** um Protokollseiten (einschließlich SMART-/Integritätsdaten) zu erhalten.
    -   Verwenden **Sie NVMeDataTypeFeature,** um Features des NVMe-Laufwerks zu erhalten.

-   [**STORAGE \_ TEMPERATURE \_ INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : Diese Struktur wird verwendet, um bestimmte Temperaturdaten zu halten. Sie wird im **\_ SPEICHER-TEMERATURE-DATENDESKRIPTOR \_ \_** verwendet, um die Ergebnisse einer Temperaturabfrage zurück zu geben.

-   [**IOCTL \_ STORAGE \_ SET \_ TEMPERATURE \_ THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Verwenden Sie diese IOCTL mit der **\_ \_ Speichertemperaturschwellenwert-Struktur,** um Temperaturschwellenwerte zu setzen. Weitere Informationen finden Sie unter [Befehle zum Ändern des Verhaltens.](#behavior-changing-commands)

-   [**STORAGE \_ \_TEMPERATURSCHWELLENWERT:**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) Diese Struktur wird als Eingabepuffer verwendet, um den Temperaturschwellenwert anzugeben. Das **OverThreshold-Feld** (boolesch)  gibt an, ob das Schwellenwertfeld der Über-Schwellenwert ist oder nicht (andernfalls ist es der unter dem Schwellenwert).

## <a name="pass-through-mechanism"></a>Pass-Through-Mechanismus

Befehle, die nicht in der NVMe-Spezifikation definiert sind, sind für das Hostbetriebssystem am schwersten zu verarbeiten. Der Host hat keinen Einblick in die Auswirkungen, die die Befehle auf das Zielgerät haben können, die verfügbar gemachte Infrastruktur (Namespaces/Blockgrößen) und ihr Verhalten.

Um solche gerätespezifischen Befehle besser über den Windows-Speicherstapel zu übertragen, ermöglicht ein neuer Pass-Through-Mechanismus das Übergeben anbieterspezifischer Befehle. Diese Pass-Through-Pipe wird auch bei der Entwicklung von Verwaltungs- und Testtools helfen. Dieser Pass-Through-Mechanismus erfordert jedoch die Verwendung des Befehlseffektprotokolls. Darüber hinaus StoreNVMe.sys alle Befehle, nicht nur Pass-Through-Befehle, im Command Effects Log beschrieben werden.

> [!IMPORTANT]
> StorNVMe.sys und Storport.sys blockiert jeden Befehl auf einem Gerät, wenn er nicht im Befehlseffektprotokoll beschrieben wird.

 

### <a name="supporting-the-command-effects-log"></a>Unterstützen des Befehlseffektprotokolls

Das Command Effects-Protokoll (wie unter Unterstützte Befehle und Effekte, Abschnitt 5.10.1.5 der [NVMe-Spezifikation 1.2](https://nvmexpress.org/specifications)beschrieben) ermöglicht die Beschreibung der Auswirkungen herstellerspezifischer Befehle zusammen mit spezifikationsdefinierten Befehlen. Dies erleichtert sowohl die Validierung der Befehlsunterstützung als auch die Optimierung des Befehlsverhaltens und sollte daher für den gesamten Satz von Befehlen implementiert werden, die das Gerät unterstützt. Die folgenden Bedingungen beschreiben das Ergebnis, wie der Befehl basierend auf seinem Command Effects Log-Eintrag gesendet wird.

Für jeden bestimmten Befehl, der im Befehlseffektprotokoll... beschrieben wird.

**While**:

-   Command Supported (CSUPP) ist auf "1" festgelegt, was bedeutet, dass der Befehl vom Controller unterstützt wird (Bit 01).

    > [!Note]  
    > Wenn CSUPP auf "0" festgelegt ist (was bedeutet, dass der Befehl nicht unterstützt wird), wird der Befehl blockiert.

     

**Und wenn** eine der folgenden Bedingungen festgelegt ist:

-   Controller Capability Change (CONTROLLER Capability Change, CONTROLLER-Funktionsänderung) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Controllerfunktionen ändern kann (Bit 04)

-   Die Änderung des Namespacebestands (NIC) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Anzahl oder Funktionen für mehrere Namespaces ändern kann (Bit 03).

-   Die Namespacefunktionsänderung (NCC) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Funktionen eines einzelnen Namespace ändern kann (Bit 02).

-   Die Befehlsübermittlung und -ausführung (Command Submission and Execution, CSE) ist auf 001b oder 010b festgelegt. Dies bedeutet, dass der Befehl übermittelt werden kann, wenn kein anderer ausstehender Befehl für denselben oder einen namespace verfügbar ist, und dass ein anderer Befehl nicht an denselben oder einen namespace übermittelt werden soll, bis dieser Befehl abgeschlossen ist (Bits 18:16).

**Anschließend wird** der Befehl als einziger ausstehender Befehl an den Adapter gesendet.

**Ander denn, wenn**:

-   Die Befehlsübermittlung und -ausführung (Command Submission and Execution, CSE) ist auf 001b festgelegt. Dies bedeutet, dass der Befehl übermittelt werden kann, wenn kein anderer ausstehender Befehl für denselben Namespace verfügbar ist, und dass ein anderer Befehl nicht an denselben Namespace übermittelt werden sollte, bis dieser Befehl abgeschlossen ist (Bits 18:16).

**Anschließend wird** der Befehl als einziger ausstehender Befehl an das Logical Unit Number-Objekt (LUN) gesendet.

**Andernfalls** wird der Befehl mit anderen befehlslos ausstehenden Befehlen gesendet. Wenn beispielsweise ein herstellerspezifischer Befehl an das Gerät gesendet wird, um statistische Informationen abzurufen, die nicht spezifikationsdefiniert sind, sollte es kein Risiko geben, das Verhalten oder die Fähigkeit des Geräts zum Ausführen von E/A-Befehlen zu ändern. Solche Anforderungen können parallel zu E/A-Anforderungen ausgeführt werden, und es ist kein Anhalten und Fortsetzen erforderlich.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Verwenden des IOCTL \_ STORAGE \_ \_ PROTOCOL-BEFEHLs zum Senden von Befehlen

Pass-Through kann mithilfe des [**IOCTL \_ STORAGE PROTOCOL \_ \_ COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)durchgeführt werden, der in Windows 10. Diese IOCTL wurde entwickelt, um ein ähnliches Verhalten wie die vorhandenen SCSI- und ATA-Pass-Through-IOCTLs zu haben, um einen eingebetteten Befehl an das Zielgerät zu senden. Über diese IOCTL kann pass-through an ein Speichergerät gesendet werden, einschließlich eines NVMe-Laufwerks.

Beispielsweise lässt die IOCTL in NVMe das Senden der folgenden Befehlscodes zu.

-   Herstellerspezifische Administratorbefehle (C0h – FFh)
-   Herstellerspezifische NVMe-Befehle (80h – FFh)

Verwenden Sie wie bei allen anderen IOCTLs [**DeviceIoControl,**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) um die Pass-Through-IOCTL nach unten zu senden. Die IOCTL wird mithilfe der [**Eingabepufferstruktur STORAGE \_ PROTOCOL \_ COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) in **ntddstor.h aufgefüllt.** Füllen Sie **das Feld Befehl** mit dem herstellerspezifischen Befehl auf.


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



Der anbieterspezifische Befehl, der gesendet werden soll, sollte im oben hervorgehobenen Feld aufgefüllt werden. Beachten Sie erneut, dass das Befehlseffektprotokoll für Pass-Through-Befehle implementiert werden muss. Insbesondere müssen diese Befehle als unterstützt im Befehlseffektprotokoll gemeldet werden (weitere Informationen finden Sie im vorherigen Abschnitt). Beachten Sie auch, dass PRP-Felder treiberspezifisch sind, daher können Anwendungen, die Befehle senden, diese als 0 (0) beenden.

Schließlich ist diese Pass-Through-IOCTL für das Senden herstellerspezifischer Befehle vorgesehen. Diese Pass-Through-IOCTL sollte nicht verwendet werden, um andere administrator- oder anbieterspezifische NVMe-Befehle wie Identify zu senden. Beispielsweise sollte **IOCTL \_ STORAGE QUERY \_ \_ PROPERTY** zum Identifizieren oder Abrufen von Protokollseiten verwendet werden. Weitere Informationen finden Sie im nächsten Abschnitt [Protokollspezifische Abfragen.](/windows)

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Aktualisieren Sie die Firmware nicht über den Pass-Through-Mechanismus.

Firmwaredownload- und Aktivierungsbefehle sollten nicht per Pass-Through gesendet werden. **IOCTL \_ STORAGE \_ PROTOCOL \_ COMMAND** sollte nur für anbieterspezifische Befehle verwendet werden.

Verwenden Sie stattdessen die folgenden allgemeinen Speicher-IOCTLs (eingeführt in Windows 10), um Anwendungen zu vermeiden, die direkt die \_ SCSI-Miniportversion der Firmware-IOCTL verwenden. Storage Treiber übersetzen die IOCTL entweder in einen SCSI-Befehl oder die \_ SCSI-Miniportversion von IOCTL in den Miniport.

Diese IOCTLs werden für die Entwicklung von Firmwareupgradetools in Windows 10 und Windows Server 2016 empfohlen:

-   [**\_IOCTL-SPEICHERFIRMWARE \_ \_ – ABRUFEN VON \_ INFORMATIONEN**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**HERUNTERLADEN DER \_ IOCTL-SPEICHERFIRMWARE \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**AKTIVIEREN DER \_ IOCTL-SPEICHERFIRMWARE \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Zum Abrufen von Speicherinformationen und Aktualisieren der Firmware unterstützt Windows auch PowerShell-Cmdlets, um dies schnell zu tun:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Um die Firmware auf NVMe in Windows 8.1 zu aktualisieren, verwenden Sie IOCTL \_ SCSI \_ MINIPORT \_ FIRMWARE. Diese IOCTL wurde nicht auf Windows 7 zurückportiert. Weitere Informationen finden Sie unter [Aktualisieren der Firmware für ein NVMe-Gerät in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Zurückgeben von Fehlern über den Pass-Through-Mechanismus

Ähnlich wie bei SCSI- und ATA-Pass-Through-IOCTLs gibt die IOCTL zurück, wenn ein Befehl/eine Anforderung an den Miniport oder das Gerät gesendet wird, wenn sie erfolgreich war oder nicht. In der [**STORAGE \_ PROTOCOL \_ COMMAND-Struktur**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) gibt die IOCTL den Status über das Feld **ReturnStatus** zurück.

### <a name="example-sending-a-vendor-specific-command"></a>Beispiel: Senden eines herstellerspezifischen Befehls

In diesem Beispiel wird ein beliebiger herstellerspezifischer Befehl (0xFF) per Pass-Through an ein NVMe-Laufwerk gesendet. Der folgende Code ordnet einen Puffer zu, initialisiert eine Abfrage und sendet dann den Befehl über DeviceIoControl an das Gerät.


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



In diesem Beispiel wird erwartet, `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` ob der Befehl auf dem Gerät erfolgreich ausgeführt wurde.

## <a name="protocol-specific-queries"></a>Protokollspezifische Abfragen

Windows 8.1 [**IOCTL STORAGE \_ \_ QUERY \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) für den Datenabruf eingeführt. In Windows 10 wurde die IOCTL erweitert, um häufig angeforderte NVMe-Features wie **Get Log Pages,** **Get Features** und **Identify** zu unterstützen. Dies ermöglicht das Abrufen von NVMe-spezifischen Informationen zu Überwachungs- und Inventurzwecken.

Der Eingabepuffer für IOCTL, [**STORAGE \_ PROPERTY \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (aus Windows 10) ist hier dargestellt.


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Wenn Sie [**IOCTL \_ STORAGE QUERY \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) verwenden, um NVMe-protokollspezifische Informationen im [**STORAGE PROTOCOL DATA \_ \_ \_ DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)abzurufen, konfigurieren Sie die [**STORAGE PROPERTY \_ \_ QUERY-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) wie folgt:

-   Zuordnen eines Puffers, der sowohl eine [**STORAGE \_ PROPERTY \_ QUERY-**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) als auch eine [**STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) enthalten kann.

-   Legen Sie das **Feld PropertyID** für einen Controller bzw. eine Geräte-/Namespaceanforderung auf **StorageAdapterProtocolSpecificProperty** oder **StorageDeviceProtocolSpecificProperty** fest.

-   Legen Sie das Feld **QueryType** auf **PropertyStandardQuery** fest.

-   Füllen Sie die [**\_ \_ SPEICHERPROTOKOLLSPEZIFISCHE \_ DATENstruktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) mit den gewünschten Werten aus. Der Anfang der **\_ \_ SPEICHERPROTOKOLLSPEZIFISCHEN \_ DATEN** ist das Feld **AdditionalParameters** von [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

Die [**\_ \_ SPEICHERPROTOKOLLSPEZIFISCHE \_ DATENstruktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (aus Windows 10) ist hier dargestellt.


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



Um einen Typ von NVMe-protokollspezifischen Informationen anzugeben, konfigurieren Sie die [**STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) wie folgt:

-   Legen Sie das **Feld ProtocolType** auf **ProtocolTypeNVMe** fest.

-   Legen Sie das **Feld DataType** auf einen Enumerationswert fest, der durch [**STORAGE PROTOCOL \_ \_ NVME DATA \_ \_ TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)definiert wird:

    -   Verwenden Sie **NVMeDataTypeIdentify,** um Identify Controller-Daten oder Identify Namespace-Daten abzurufen.
    -   Verwenden Sie **NVMeDataTypeLogPage,** um Protokollseiten (einschließlich SMART-/Integritätsdaten) abzurufen.
    -   Verwenden Sie **NVMeDataTypeFeature,** um Features des NVMe-Laufwerks abzurufen.

Wenn **ProtocolTypeNVMe** als **ProtocolType** verwendet wird, können Abfragen protokollspezifischer Informationen parallel zu anderen E/A-Abfragen auf dem NVMe-Laufwerk abgerufen werden.

> [!IMPORTANT]
> Legen Sie für eine [**IOCTL_STORAGE_QUERY_PROPERTY,**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) die eine **STORAGE_PROPERTY_ID** von [**StorageAdapterProtocolSpecificProperty**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)verwendet und deren [**STORAGE_PROTOCOL_SPECIFIC_DATA-**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) oder [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) auf und festgelegt `ProtocolType=ProtocolTypeNvme` `DataType=NVMeDataTypeLogPage` ist, den ProtocolDataLength-Member dieser Struktur auf einen Mindestwert von 512 (Bytes) fest.


Die folgenden Beispiele veranschaulichen NVMe-protokollspezifische Abfragen.

### <a name="example-nvme-identify-query"></a>Beispiel: NVMe-Identifizierungsabfrage

In diesem Beispiel wird die **Identify-Anforderung** an ein NVMe-Laufwerk gesendet. Der folgende Code initialisiert die Abfragedatenstruktur und sendet dann den Befehl über DeviceIoControl an das Gerät.


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
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Identify Controller Data succeeded***.\n"));
        }
    }

  
```

> [!IMPORTANT]
> Legen Sie für eine [**IOCTL_STORAGE_QUERY_PROPERTY,**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) die eine **STORAGE_PROPERTY_ID** von [**StorageAdapterProtocolSpecificProperty**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)verwendet und deren [**STORAGE_PROTOCOL_SPECIFIC_DATA-**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) oder [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) auf und festgelegt `ProtocolType=ProtocolTypeNvme` `DataType=NVMeDataTypeLogPage` ist, den ProtocolDataLength-Member dieser Struktur auf einen Mindestwert von 512 (Bytes) fest.


Beachten Sie, dass der Aufrufer einen einzelnen Puffer zuordnen muss, der STORAGE \_ PROPERTY QUERY und die Größe der \_ \_ \_ SPEICHERPROTOKOLLSPEZIFISCHEN DATEN \_ enthält. In diesem Beispiel wird der gleiche Puffer für die Eingabe und Ausgabe der Eigenschaftenabfrage verwendet. Aus diesem Grund hat der zugeordnete Puffer die Größe "FIELD \_ OFFSET(STORAGE \_ PROPERTY \_ QUERY, AdditionalParameters) + sizeof(STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA) + NVME \_ MAX LOG \_ \_ SIZE". Obwohl separate Puffer sowohl für die Eingabe als auch für die Ausgabe zugeordnet werden können, empfehlen wir die Verwendung eines einzelnen Puffers, um NVMe-bezogene Informationen abzufragen.

### <a name="example-nvme-get-log-pages-query"></a>Beispiel: NVMe-Abfrage "Protokollseiten abrufen"

In diesem Beispiel wird die Anforderung **Protokollseiten abrufen** basierend auf dem vorherigen an ein NVMe-Laufwerk gesendet. Der folgende Code bereitet die Abfragedatenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.


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

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***SMART/Health Information Log succeeded***.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Beispiel: NVMe-Abfrage "Get Features"

In diesem Beispiel wird die Anforderung **Features abrufen** basierend auf dem vorherigen an ein NVMe-Laufwerk gesendet. Der folgende Code bereitet die Abfragedatenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.


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

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Get Feature - Volatile Cache succeeded***.\n"));
    }
```
## <a name="protocol-specific-set"></a>Protokollspezifischer Satz

Ab Windows 10 19H1 wurde die IOCTL_STORAGE_SET_PROPERTY erweitert, um NVMe-Set-Features zu unterstützen.

Der Eingabepuffer für die IOCTL_STORAGE_SET_PROPERTY ist hier dargestellt:

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

} STORAGE_PROPERTY_SET, *PSTORAGE_PROPERTY_SET;
```

Wenn Sie IOCTL_STORAGE_SET_PROPERTY zum Festlegen des NVMe-Features verwenden, konfigurieren Sie die STORAGE_PROPERTY_SET-Struktur wie folgt:

-   Zuordnen eines Puffers, der sowohl eine STORAGE_PROPERTY_SET als auch eine STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur enthalten kann.
-   Legen Sie das Feld PropertyID für einen Controller bzw. eine Geräte-/Namespaceanforderung auf StorageAdapterProtocolSpecificProperty oder StorageDeviceProtocolSpecificProperty fest.
-   Füllen Sie die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur mit den gewünschten Werten aus. Der Anfang des STORAGE_PROTOCOL_SPECIFIC_DATA_EXT ist das Feld AdditionalParameters von STORAGE_PROPERTY_SET.

Die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur ist hier dargestellt.

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

Um einen typisierten NVMe-Featuretyp anzugeben, konfigurieren Sie die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur wie folgt:
-   Legen Sie das Feld ProtocolType auf ProtocolTypeNvme fest.
-   Legen Sie das Feld DataType auf den Enumerationswert NVMeDataTypeFeature fest, der durch STORAGE_PROTOCOL_NVME_DATA_TYPE definiert wird.

In den folgenden Beispielen wird der NVMe-Featuresatz veranschaulicht.

### <a name="example-nvme-set-features"></a>Beispiel: NVMe-Set-Features

In diesem Beispiel wird die Anforderung Features festlegen an ein NVMe-Laufwerk gesendet. Der folgende Code bereitet die Set-Datenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.

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

## <a name="temperature-queries"></a>Temperaturabfragen

In Windows 10 kann [**IOCTL \_ STORAGE \_ QUERY \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) auch zum Abfragen von Temperaturdaten von NVMe-Geräten verwendet werden.

Um Temperaturinformationen von einem NVMe-Laufwerk im [**\_ \_ \_ SPEICHERTEMPERATURDATENDESKRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)abzurufen, konfigurieren Sie die [**STORAGE \_ PROPERTY \_ QUERY-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) wie folgt:

-   Zuordnen eines Puffers, der eine [**STORAGE \_ PROPERTY \_ QUERY-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) enthalten kann.

-   Legen Sie das **Feld PropertyID** für einen Controller bzw. eine Geräte-/Namespaceanforderung auf **StorageAdapterTemperatureProperty** oder **StorageDeviceTemperatureProperty** fest.

-   Legen Sie das Feld **QueryType** auf **PropertyStandardQuery** fest.

Die [**STORAGE \_ TEMPERATURE \_ INFO-Struktur**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (aus Windows 10) ist hier dargestellt.


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



## <a name="behavior-changing-commands"></a>Befehle zum Ändern des Verhaltens

Befehle, die Geräteattribute bearbeiten oder sich potenziell auf das Geräteverhalten auswirken, sind für das Betriebssystem schwieriger zu behandeln. Wenn sich Geräteattribute zur Laufzeit ändern, während E/A verarbeitet wird, können Synchronisierungs- oder Datenintegritätsprobleme auftreten, wenn sie nicht ordnungsgemäß behandelt werden.

Der **NVMe-Befehl Set-Features** ist ein gutes Beispiel für einen Befehl zum Ändern des Verhaltens. Sie ermöglicht die Änderung des Vermittlungsmechanismus und die Festlegung von Temperaturschwellenwerten. Um sicherzustellen, dass während des Flugs keine Daten gefährdet sind, wenn verhaltensbezogene Set-Befehle gesendet werden, halten Windows alle E/A-Datenübertragungen an das NVMe-Gerät an, leeren Warteschlangen und Leeren von Puffern. Sobald der Set-Befehl erfolgreich ausgeführt wurde, wird die E/A fortgesetzt (sofern möglich). Wenn E/A nicht fortgesetzt werden kann, ist möglicherweise eine Geräterücksetzung erforderlich.

### <a name="setting-temperature-thresholds"></a>Festlegen von Temperaturschwellenwerten

Windows 10 [**IOCTL STORAGE \_ \_ SET \_ TEMPERATURE \_ THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)eingeführt, eine IOCTL zum Abrufen und Festlegen von Temperaturschwellenwerten. Sie können es auch verwenden, um die aktuelle Temperatur des Geräts abzurufen. Der Eingabe-/Ausgabepuffer für diese IOCTL ist die [**STORAGE \_ TEMPERATURE \_ INFO-Struktur**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) aus dem vorherigen Codeabschnitt.

### <a name="example-setting-over-threshold-temperature"></a>Beispiel: Festlegen der Überschwellentemperatur

In diesem Beispiel wird die Überschwellentemperatur eines NVMe-Laufwerks festgelegt. Der folgende Code bereitet den Befehl vor und sendet ihn dann über DeviceIoControl an das Gerät.


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



### <a name="setting-vendor-specific-features"></a>Festlegen herstellerspezifischer Features

Ohne das Befehlseffektprotokoll hat der Treiber keine Kenntnis der Auswirkungen des Befehls. Aus diesem Grund ist das Befehlseffektprotokoll erforderlich. Damit kann das Betriebssystem ermitteln, ob ein Befehl eine hohe Auswirkung hat und parallel zu anderen Befehlen an das Laufwerk gesendet werden kann.

Das Befehlseffektprotokoll ist noch nicht präzise genug, um anbieterspezifische **Set-Features-Befehle zu** umfassen. Aus diesem Grund ist es noch nicht möglich, anbieterspezifische **Set-Features-Befehle zu** senden. Es ist jedoch möglich, den weiter oben erläuterten Pass-Through-Mechanismus zu verwenden, um anbieterspezifische Befehle zu senden. Weitere Informationen finden Sie unter [Pass-Through-Mechanismus](#pass-through-mechanism).

## <a name="header-files"></a>Headerdateien

Die folgenden Dateien sind für die NVMe-Entwicklung relevant. Diese Dateien sind im [Microsoft Windows Software Development Kit (SDK) enthalten.](https://developer.microsoft.com/windows/downloads)



| Headerdatei    | BESCHREIBUNG                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor.h** | Definiert Konstanten und Typen für den Zugriff auf die Speicherklassentreiber aus dem Kernelmodus.   |
| **nvme.h**     | Für andere NVMe-bezogene Datenstrukturen.                                                 |
| **winioctl.h** | Für allgemeine Win32-IOCTL-Definitionen, einschließlich Speicher-APIs für Benutzermodusanwendungen. |



 

 

 
