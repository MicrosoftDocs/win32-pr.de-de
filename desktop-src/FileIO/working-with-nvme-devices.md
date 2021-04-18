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
# <a name="working-with-nvme-drives"></a><span data-ttu-id="93fcf-103">Arbeiten mit nvme-Laufwerken</span><span class="sxs-lookup"><span data-stu-id="93fcf-103">Working with NVMe drives</span></span>

<span data-ttu-id="93fcf-104">**Anwendungsbereich:**</span><span class="sxs-lookup"><span data-stu-id="93fcf-104">**Applies to:**</span></span>

-   <span data-ttu-id="93fcf-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="93fcf-105">Windows 10</span></span>
-   <span data-ttu-id="93fcf-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="93fcf-106">Windows Server 2016</span></span>

<span data-ttu-id="93fcf-107">Erfahren Sie, wie Sie in Ihrer Windows-Anwendung mit hoch Geschwindigkeits basierten nvme-Geräten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="93fcf-108">Der Gerätezugriff wird über **StorNVMe.sys** aktiviert, der in Windows Server 2012 R2 und Windows 8.1 eingeführte in-Box-Treiber.</span><span class="sxs-lookup"><span data-stu-id="93fcf-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="93fcf-109">Sie steht auch für Windows 7-Geräte über eine KB-Hotfix zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="93fcf-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="93fcf-110">In Windows 10 wurden mehrere neue Features eingeführt, einschließlich eines Pass-Through-Mechanismus für herstellerspezifische nvme-Befehle und Aktualisierungen vorhandener IOCTLs.</span><span class="sxs-lookup"><span data-stu-id="93fcf-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="93fcf-111">Dieses Thema bietet einen Überblick über allgemeine Verwendungs-APIs, mit denen Sie auf nvme-Laufwerke in Windows 10 zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="93fcf-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="93fcf-112">Außerdem wird Folgendes beschrieben:</span><span class="sxs-lookup"><span data-stu-id="93fcf-112">It also describes:</span></span>

-   <span data-ttu-id="93fcf-113">Senden eines herstellerspezifischen nvme-Befehls mit [Pass-Through](#pass-through-mechanism)</span><span class="sxs-lookup"><span data-stu-id="93fcf-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="93fcf-114">[Senden eines Befehls zum identifizieren, Anzeigen von Funktionen oder zum Senden von Protokoll Seiten](#protocol-specific-queries) an das nvme-Laufwerk</span><span class="sxs-lookup"><span data-stu-id="93fcf-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="93fcf-115">Abrufen von [Temperatur Informationen](#temperature-queries) von einem nvme-Laufwerk</span><span class="sxs-lookup"><span data-stu-id="93fcf-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="93fcf-116">So führen Sie Verhaltens Wechsel Befehle aus, z. b. das [Festlegen von Temperaturschwellen Werten](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="93fcf-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="93fcf-117">APIs für die Arbeit mit nvme-Laufwerken</span><span class="sxs-lookup"><span data-stu-id="93fcf-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="93fcf-118">Sie können die folgenden allgemeinen APIs verwenden, um auf nvme-Laufwerke in Windows 10 zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="93fcf-119">Diese APIs finden Sie in **winioctl. h** für Benutzermodusanwendungen und **ntddstor. h** für Kernelmodustreiber.</span><span class="sxs-lookup"><span data-stu-id="93fcf-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="93fcf-120">Weitere Informationen zu Header Dateien finden Sie unter [Header Dateien](#header-files).</span><span class="sxs-lookup"><span data-stu-id="93fcf-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="93fcf-121">[**IOCTL \_ Storage- \_ Protokoll \_ Befehl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Verwenden Sie diese IOCTL mit der **Speicher Protokoll- \_ \_ Befehls** Struktur, um nvme-Befehle auszugeben.</span><span class="sxs-lookup"><span data-stu-id="93fcf-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="93fcf-122">Diese IOCTL ermöglicht die nvme-Weiterleitung und unterstützt das Befehls Effekt Protokoll in nvme.</span><span class="sxs-lookup"><span data-stu-id="93fcf-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="93fcf-123">Sie können Sie mit anbieterspezifischen Befehlen verwenden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="93fcf-124">Weitere Informationen finden Sie unter [Pass-Through-Mechanismus](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="93fcf-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="93fcf-125">[**Speicher \_ Protokoll \_ Befehl**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : Diese Eingabepuffer Struktur enthält ein **ReturnStatus** -Feld, das verwendet werden kann, um die folgenden Statuswerte zu melden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="93fcf-126">**Status des Speicher \_ Protokolls steht \_ \_ aus.**</span><span class="sxs-lookup"><span data-stu-id="93fcf-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="93fcf-127">**Status des Speicher \_ Protokolls war \_ \_ erfolgreich.**</span><span class="sxs-lookup"><span data-stu-id="93fcf-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="93fcf-128">**Fehler beim Speicher \_ Protokoll \_ Status \_**</span><span class="sxs-lookup"><span data-stu-id="93fcf-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="93fcf-129">**\_ \_ \_ ungültige Anforderung für Speicher Protokoll Status \_**</span><span class="sxs-lookup"><span data-stu-id="93fcf-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="93fcf-130">**Speicher \_ Protokoll \_ Status " \_ kein \_ Gerät"**</span><span class="sxs-lookup"><span data-stu-id="93fcf-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="93fcf-131">**der Speicher \_ Protokoll \_ Status ist \_ ausgelastet.**</span><span class="sxs-lookup"><span data-stu-id="93fcf-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="93fcf-132">**\_ \_ Status \_ Daten \_ Überlauf des Speicher Protokolls**</span><span class="sxs-lookup"><span data-stu-id="93fcf-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="93fcf-133">**Speicher \_ Protokoll \_ Status \_ unzureichende \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="93fcf-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="93fcf-134">**Speicher \_ Protokoll \_ Status \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="93fcf-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="93fcf-135">[**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Verwenden Sie diese IOCTL mit der **Speicher \_ Eigenschafts \_ Abfrage** -Struktur, um Geräteinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="93fcf-136">Weitere Informationen finden Sie unter [Protokoll spezifische Abfragen](#protocol-specific-queries) und [Temperatur Abfragen](#temperature-queries).</span><span class="sxs-lookup"><span data-stu-id="93fcf-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="93fcf-137">[**Speicher \_ Eigenschaften \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : Diese Struktur enthält die Felder **PropertyId** und **AdditionalParameters** , um die Daten anzugeben, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="93fcf-138">Verwenden Sie in der erfasste **PropertyId** die **Speicher eigen \_ schafts- \_ ID** -Enumeration, um den Datentyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93fcf-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="93fcf-139">Verwenden Sie das **AdditionalParameters** -Feld, um je nach Datentyp weitere Details anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93fcf-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="93fcf-140">Verwenden Sie für Protokoll spezifische Daten die **Speicher \_ Protokoll \_ spezifische \_ Daten** Struktur im Feld **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="93fcf-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="93fcf-141">Verwenden Sie für Temperaturdaten die Struktur der **Speicher \_ Temperatur \_ Informationen** im Feld **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="93fcf-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="93fcf-142">[**Speicher \_ Eigen schafts- \_ ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : Diese Enumeration enthält neue Werte, mit denen die **IOCTL- \_ Speicher \_ Abfrage \_ Eigenschaft** Protokoll spezifische und Temperatur Informationen abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="93fcf-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="93fcf-143">**Storageadapterprotocolspecificproperty**</span><span class="sxs-lookup"><span data-stu-id="93fcf-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="93fcf-144">**Storagedeviceprotocolspecificproperty**</span><span class="sxs-lookup"><span data-stu-id="93fcf-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="93fcf-145">Verwenden Sie eine dieser Protokoll spezifischen Eigenschaften-IDs in Kombination mit **Speicher \_ Protokoll \_ spezifischen \_ Daten** , um Protokoll spezifische Daten in der [**\_ \_ Daten \_ deskriptorstruktur des Speicher Protokolls**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="93fcf-146">**Storageadaptertemperatureproperty**</span><span class="sxs-lookup"><span data-stu-id="93fcf-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="93fcf-147">**Storagedevicetemperatureproperty**</span><span class="sxs-lookup"><span data-stu-id="93fcf-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="93fcf-148">Verwenden Sie eine dieser Temperatureigenschaften-IDs, um Temperaturdaten in [**der \_ \_ \_ deskriptorstruktur der Speichertemperatur Daten**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="93fcf-149">[**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Rufen Sie nvme-spezifische Daten ab, wenn diese Struktur für das **AdditionalParameters** -Feld der **Speicher \_ Eigenschafts \_ Abfrage** verwendet wird und ein [**\_ \_ nvme \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) -Enumerationswert für das Speicher Protokoll angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="93fcf-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="93fcf-150">Verwenden Sie einen der folgenden Werte für den **\_ \_ nvme- \_ \_ Datentyp des Speicher Protokolls** im **DataType** -Feld der **Speicher \_ Protokoll \_ spezifischen \_ Daten** Struktur:</span><span class="sxs-lookup"><span data-stu-id="93fcf-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="93fcf-151">Verwenden Sie **nvmedatatypeidentify** zum Ermitteln von Controller Daten oder zum Identifizieren von Namespace Daten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="93fcf-152">Verwenden Sie **nvmedatatypelogpage** zum Aufrufen von Protokoll Seiten (einschließlich intelligenter/Integritäts Daten).</span><span class="sxs-lookup"><span data-stu-id="93fcf-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="93fcf-153">Verwenden Sie **nvmedatatygfeature** , um die Features des nvme-Laufwerks zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="93fcf-154">[**Speicher \_ Temperatur \_ Informationen**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : Diese Struktur wird verwendet, um bestimmte Temperaturdaten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="93fcf-155">Es wird im **\_ \_ Daten \_ Deskriptor Storage temerklatur** verwendet, um die Ergebnisse einer Temperatur Abfrage zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="93fcf-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="93fcf-156">[**IOCTL \_ \_ \_ \_ Schwellenwert für die Speicher festgelegte Temperatur**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Verwenden Sie diese IOCTL mit der Struktur der **Speicher \_ Temperatur \_ Schwelle** , um Temperaturschwellen Werte festzulegen</span><span class="sxs-lookup"><span data-stu-id="93fcf-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="93fcf-157">Weitere Informationen finden Sie unter [Behavior Changing Commands](#behavior-changing-commands).</span><span class="sxs-lookup"><span data-stu-id="93fcf-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="93fcf-158">[**Speicher \_ Temperatur \_ Schwellenwert**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : Diese Struktur wird als Eingabepuffer verwendet, um den Temperaturschwellen Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93fcf-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="93fcf-159">Das **overthreshold** -Feld (boolescher Wert) gibt an, ob das **Schwellen** Wert Feld den over-Schwellenwert oder nicht (andernfalls der unter Schwellenwert) ist.</span><span class="sxs-lookup"><span data-stu-id="93fcf-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="93fcf-160">Pass-Through-Mechanismus</span><span class="sxs-lookup"><span data-stu-id="93fcf-160">Pass-through mechanism</span></span>

<span data-ttu-id="93fcf-161">Befehle, die nicht in der nvme-Spezifikation definiert sind, sind für das Host Betriebssystem am schwierigsten – der Host hat keinen Einblick in die Auswirkungen der Befehle auf das Zielgerät, die verfügbar gemachte Infrastruktur (Namespaces/Blockgrößen) und das zugehörige Verhalten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="93fcf-162">Um solche gerätespezifischen Befehle über den Windows-Speicher Stapel zu übertragen, können mit einem neuen Pass-Through-Mechanismus herstellerspezifische Befehle weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="93fcf-163">Diese Pass-Through-Pipe bietet auch Unterstützung bei der Entwicklung von Verwaltungs-und TestTools.</span><span class="sxs-lookup"><span data-stu-id="93fcf-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="93fcf-164">Dieser Pass-Through-Mechanismus erfordert jedoch die Verwendung des Befehls Effekt Protokolls.</span><span class="sxs-lookup"><span data-stu-id="93fcf-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="93fcf-165">Darüber hinaus erfordert StoreNVMe.sys, dass alle Befehle, nicht nur Pass-Through-Befehle, im Befehls Effekt Protokoll beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93fcf-166">StorNVMe.sys und Storport.sys blockieren jeden Befehl an ein Gerät, wenn es nicht im Befehls Effekt Protokoll beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="93fcf-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="93fcf-167">Unterstützen des Befehls Effekt Protokolls</span><span class="sxs-lookup"><span data-stu-id="93fcf-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="93fcf-168">Das Befehls Effekt Protokoll (wie unter "Befehle unterstützt" und "Effects", Abschnitt 5.10.1.5 of [nvme Specification 1,2](https://nvmexpress.org/specifications)), ermöglicht die Beschreibung der Auswirkungen der herstellerspezifischen Befehle sowie von Spezifikations definierten Befehlen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="93fcf-169">Dadurch wird sowohl die Validierung der Befehls Unterstützung als auch die Befehls Verhaltens Optimierung ermöglicht und sollte daher für alle Befehle implementiert werden, die das Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="93fcf-170">Die folgenden Bedingungen beschreiben das Ergebnis der Übermittlung des Befehls auf der Grundlage des Befehls Effekt-Protokoll Eintrags.</span><span class="sxs-lookup"><span data-stu-id="93fcf-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="93fcf-171">Für jeden bestimmten Befehl, der im Befehls Effekt Protokoll beschrieben wird...</span><span class="sxs-lookup"><span data-stu-id="93fcf-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="93fcf-172">**Während**:</span><span class="sxs-lookup"><span data-stu-id="93fcf-172">**While**:</span></span>

-   <span data-ttu-id="93fcf-173">Der unterstützte Befehl (csupp) ist auf "1" festgelegt, was bedeutet, dass der Befehl vom Controller unterstützt wird (Bit 01).</span><span class="sxs-lookup"><span data-stu-id="93fcf-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="93fcf-174">Wenn csupp auf "0" festgelegt ist (was bedeutet, dass der Befehl nicht unterstützt wird), wird der Befehl blockiert.</span><span class="sxs-lookup"><span data-stu-id="93fcf-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="93fcf-175">**Und wenn** Folgendes festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="93fcf-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="93fcf-176">Die Controller Funktionsänderung (CCC) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Controller Funktionen ändern kann (Bit 04).</span><span class="sxs-lookup"><span data-stu-id="93fcf-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="93fcf-177">Die Namespace-Inventur Änderung (NIC) ist auf "1" festgelegt, was bedeutet, dass der Befehl möglicherweise die Anzahl oder die Funktionen für mehrere Namespaces (Bit 03) ändert.</span><span class="sxs-lookup"><span data-stu-id="93fcf-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="93fcf-178">Die Namespace-Funktionsänderung (NCC) ist auf "1" festgelegt, was bedeutet, dass der Befehl die Funktionen eines einzelnen Namespace ändern kann (Bit 02).</span><span class="sxs-lookup"><span data-stu-id="93fcf-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="93fcf-179">Die Befehls Übermittlung und-Ausführung (CSE) ist auf 001b oder 010b festgelegt, was bedeutet, dass der Befehl gesendet werden kann, wenn kein anderer ausstehender Befehl für denselben oder einen Namespace vorhanden ist, und dass ein anderer Befehl erst an denselben oder einen Namespace übermittelt werden soll, wenn dieser Befehl vollständig ist (Bits 18:16).</span><span class="sxs-lookup"><span data-stu-id="93fcf-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="93fcf-180">**Anschließend** wird der Befehl als einziger Befehl an den Adapter gesendet, der für den Adapter aussteht.</span><span class="sxs-lookup"><span data-stu-id="93fcf-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="93fcf-181">**Andernfalls**:</span><span class="sxs-lookup"><span data-stu-id="93fcf-181">**Else if**:</span></span>

-   <span data-ttu-id="93fcf-182">Die Befehls Übermittlung und-Ausführung (CSE) ist auf 001b festgelegt, was bedeutet, dass der Befehl übermittelt werden kann, wenn es keinen anderen ausstehenden Befehl für denselben Namespace gibt und dass ein anderer Befehl erst an denselben Namespace übermittelt werden soll, wenn dieser Befehl vollständig ist (Bits 18:16).</span><span class="sxs-lookup"><span data-stu-id="93fcf-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="93fcf-183">**Anschließend** wird der Befehl als einziger Befehl gesendet, der für das logische Gerätenummern Objekt (Logical Unit Number Object, LUN) aussteht.</span><span class="sxs-lookup"><span data-stu-id="93fcf-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="93fcf-184">**Andernfalls** wird der Befehl mit anderen ausstehenden Befehlen ohne Behinderung gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="93fcf-185">Wenn z. b. ein Hersteller spezifischer Befehl an das Gerät gesendet wird, um statistische Informationen abzurufen, die nicht Spezifikations definiert sind, besteht keine Gefahr, das Verhalten des Geräts oder die Fähigkeit zum Ausführen von I/O-Befehlen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="93fcf-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="93fcf-186">Solche Anforderungen können parallel zu e/a-Vorgängen gewartet werden, und es wäre keine Pause-Fortsetzung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93fcf-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="93fcf-187">Verwenden des IOCTL- \_ Speicher \_ Protokoll \_ Befehls zum Senden von Befehlen</span><span class="sxs-lookup"><span data-stu-id="93fcf-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="93fcf-188">Der Pass-Through-Befehl kann mit dem in Windows 10 eingeführten [**IOCTL- \_ Speicher \_ Protokoll \_ Befehl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="93fcf-189">Diese IOCTL wurde so entworfen, dass Sie ein ähnliches Verhalten wie die vorhandene SCSI-und ATA-Pass-Through-IOCTLs hat, um einen eingebetteten Befehl an das Zielgerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="93fcf-190">Über diese IOCTL kann Pass-Through an ein Speichergerät gesendet werden, einschließlich eines nvme-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="93fcf-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="93fcf-191">In nvme lässt z. b. die IOCTL das Senden der folgenden Befehls Codes zu.</span><span class="sxs-lookup"><span data-stu-id="93fcf-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="93fcf-192">Anbieterspezifische Administrator Befehle (C0h – FFH)</span><span class="sxs-lookup"><span data-stu-id="93fcf-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="93fcf-193">Anbieterspezifische nvme-Befehle (80he – FFH)</span><span class="sxs-lookup"><span data-stu-id="93fcf-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="93fcf-194">Verwenden Sie wie bei allen anderen IOCTLs [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) , um den Pass-Through-ioctl zu senden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="93fcf-195">Die IOCTL wird mithilfe der in " **ntddstor. h**" gefundenen Eingabe-/pufferstruktur des [**Speicher \_ Protokoll \_ Befehls**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="93fcf-196">Füllen Sie das **Befehls** Feld mit dem herstellerspezifischen Befehl auf.</span><span class="sxs-lookup"><span data-stu-id="93fcf-196">Populate the **Command** field with the vendor-specific command.</span></span>


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



<span data-ttu-id="93fcf-197">Der zu sendende herstellerspezifische Befehl sollte in dem oben markierten Feld aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="93fcf-198">Beachten Sie, dass das Befehls Effekt Protokoll für Pass-Through-Befehle implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="93fcf-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="93fcf-199">Insbesondere müssen diese Befehle im Befehls Effekt Protokoll als unterstützt gemeldet werden (Weitere Informationen finden Sie im vorherigen Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="93fcf-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="93fcf-200">Beachten Sie auch, dass PRP-Felder Treiber spezifisch sind, sodass Anwendungen, die Befehle senden, Sie als 0 belassen können.</span><span class="sxs-lookup"><span data-stu-id="93fcf-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="93fcf-201">Zum Schluss ist diese Pass-Through-ioctl zum Senden Hersteller spezifischer Befehle gedacht.</span><span class="sxs-lookup"><span data-stu-id="93fcf-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="93fcf-202">Zum Senden anderer nvme-Befehle (Administrator oder nicht Anbieter), wie z. b. "ermitteln", sollte diese Pass-Through-ioctl nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="93fcf-203">Beispielsweise sollte die **IOCTL \_ Storage \_ Query- \_ Eigenschaft** zum identifizieren oder erhalten von Protokoll Seiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="93fcf-204">Weitere Informationen finden Sie im nächsten Abschnitt [Protokoll spezifische Abfragen](/windows).</span><span class="sxs-lookup"><span data-stu-id="93fcf-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="93fcf-205">Aktualisieren Sie die Firmware nicht durch den Pass-Through-Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="93fcf-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="93fcf-206">Firmwaredownloads und aktivierungsbefehle sollten nicht mithilfe von Pass-Through gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="93fcf-207">**IOCTL \_ Der Speicher \_ Protokoll \_ Befehl** sollte nur für herstellerspezifische Befehle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="93fcf-208">Verwenden Sie stattdessen den folgenden allgemeinen Speicher-IOCTLs (eingeführt in Windows 10), um Anwendungen zu vermeiden, die die SCSI- \_ Mini Port-Version der Firmware ioctl direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="93fcf-209">Speicher Treiber übersetzen die IOCTL entweder in einen SCSI-Befehl oder die SCSI- \_ Mini PORTVERSION der IOCTL in den Mini Port.</span><span class="sxs-lookup"><span data-stu-id="93fcf-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="93fcf-210">Diese IOCTLs werden zum Entwickeln von Firmwareupdates in Windows 10 und Windows Server 2016 empfohlen:</span><span class="sxs-lookup"><span data-stu-id="93fcf-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="93fcf-211">**IOCTL- \_ Speicher \_ Firmware \_ get \_ Info**</span><span class="sxs-lookup"><span data-stu-id="93fcf-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="93fcf-212">**Download der IOCTL- \_ Speicher \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="93fcf-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="93fcf-213">**IOCTL- \_ Speicher \_ Firmware \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="93fcf-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="93fcf-214">Um Speicherinformationen zu erhalten und Firmware zu aktualisieren, unterstützt Windows auch PowerShell-Cmdlets, um dies schnell zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="93fcf-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="93fcf-215">Zum Aktualisieren der Firmware auf dem nvme in Windows 8.1 verwenden Sie die IOCTL \_ SCSI \_ Miniport- \_ Firmware.</span><span class="sxs-lookup"><span data-stu-id="93fcf-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="93fcf-216">Diese IOCTL wurde nicht auf Windows 7 zurückportiert.</span><span class="sxs-lookup"><span data-stu-id="93fcf-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="93fcf-217">Weitere Informationen finden Sie [unter Aktualisieren der Firmware für ein nvme-Gerät in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span><span class="sxs-lookup"><span data-stu-id="93fcf-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="93fcf-218">Zurückgeben von Fehlern durch den Pass-Through-Mechanismus</span><span class="sxs-lookup"><span data-stu-id="93fcf-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="93fcf-219">Wenn ein Befehl bzw. eine Anforderung an den Mini Port oder das Gerät gesendet wird, gibt die IOCTL-Datei (ähnlich wie SCSI und ATA Pass-Through IOCTLs) zurück, wenn Sie erfolgreich war oder nicht.</span><span class="sxs-lookup"><span data-stu-id="93fcf-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="93fcf-220">In der [**Speicher \_ Protokoll- \_ Befehls**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) Struktur gibt ioctl den Status über das Feld **ReturnStatus** zurück.</span><span class="sxs-lookup"><span data-stu-id="93fcf-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="93fcf-221">Beispiel: Senden eines herstellerspezifischen Befehls</span><span class="sxs-lookup"><span data-stu-id="93fcf-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="93fcf-222">In diesem Beispiel wird ein beliebiger Hersteller spezifischer Befehl (0xFF) per Pass-Through an ein nvme-Laufwerk gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="93fcf-223">Der folgende Code ordnet einen Puffer zu, Initialisiert eine Abfrage und sendet den Befehl dann über DeviceIoControl an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="93fcf-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


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



<span data-ttu-id="93fcf-224">In diesem Beispiel wird davon ausgegangen, dass `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` der Befehl dem Gerät erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="93fcf-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="93fcf-225">Protokoll spezifische Abfragen</span><span class="sxs-lookup"><span data-stu-id="93fcf-225">Protocol-specific queries</span></span>

<span data-ttu-id="93fcf-226">Windows 8.1 hat die [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) zum Abrufen von Daten eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="93fcf-227">In Windows 10 wurde die IOCTL verbessert, um häufig angeforderte nvme **-Funktionen** zu unterstützen, wie z. b. " **Get Log Pages**" und " **Get Features**".</span><span class="sxs-lookup"><span data-stu-id="93fcf-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="93fcf-228">Dies ermöglicht das Abrufen von nvme-spezifischen Informationen zu Überwachungs-und Inventur Zwecken.</span><span class="sxs-lookup"><span data-stu-id="93fcf-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="93fcf-229">Der Eingabepuffer für die IOCTL-, [**Storage- \_ Eigenschafts \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (aus Windows 10) wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="93fcf-230">Wenn Sie die [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) verwenden, um nvme-Protokoll spezifische Informationen im [**Speicher \_ Protokoll \_ Daten \_ Deskriptor**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)abzurufen, konfigurieren Sie die Abfrage Struktur der [**Speicher \_ Eigenschaft \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93fcf-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="93fcf-231">Weisen Sie einen Puffer zu, der sowohl eine [**Speicher \_ Eigenschaften \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) als auch eine [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="93fcf-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="93fcf-232">Legen Sie das Feld **PropertyId** auf **storageadapterprotocolspecificproperty** oder **storagedeviceprotocolspecificproperty** für eine Controller-oder Geräte-bzw. Namespace Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="93fcf-233">Legen Sie das Feld **QueryType** auf **propertystandardquery** fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="93fcf-234">Füllen Sie die [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur mit den gewünschten Werten aus.</span><span class="sxs-lookup"><span data-stu-id="93fcf-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="93fcf-235">Der Anfang der **Speicher \_ Protokoll \_ spezifischen \_ Daten** ist das **AdditionalParameters** -Feld der [**Speicher \_ Eigenschafts \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span><span class="sxs-lookup"><span data-stu-id="93fcf-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="93fcf-236">Die [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur (aus Windows 10) wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


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



<span data-ttu-id="93fcf-237">Um einen Typ von nvme-Protokoll spezifischen Informationen anzugeben, konfigurieren Sie die [**Speicher \_ Protokoll \_ spezifische \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) Struktur wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93fcf-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="93fcf-238">Legen Sie das Feld **ProtocolType** auf **protocoltypvme** fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="93fcf-239">Legen Sie das Feld **DataType** auf einen Enumerationswert fest, der vom [**\_ \_ nvme- \_ \_ Datentyp des Speicher Protokolls**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)definiert wird:</span><span class="sxs-lookup"><span data-stu-id="93fcf-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="93fcf-240">Verwenden Sie **nvmedatatypeidentify** zum Ermitteln von Controller Daten oder zum Identifizieren von Namespace Daten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="93fcf-241">Verwenden Sie **nvmedatatypelogpage** zum Aufrufen von Protokoll Seiten (einschließlich intelligenter/Integritäts Daten).</span><span class="sxs-lookup"><span data-stu-id="93fcf-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="93fcf-242">Verwenden Sie **nvmedatatygfeature** , um die Features des nvme-Laufwerks zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="93fcf-243">Wenn **protocoltypvme** als **ProtocolType** verwendet wird, können Abfragen für Protokoll spezifische Informationen parallel zu anderen e/a-Vorgängen auf dem nvme-Laufwerk abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="93fcf-244">Die folgenden Beispiele veranschaulichen nvme-Protokoll spezifische Abfragen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="93fcf-245">Beispiel: nvme-Abfrage</span><span class="sxs-lookup"><span data-stu-id="93fcf-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="93fcf-246">In diesem Beispiel wird die **identifikanungsanforderung** an ein nvme-Laufwerk gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="93fcf-247">Der folgende Code initialisiert die Abfrage Datenstruktur und sendet dann den Befehl über DeviceIoControl an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="93fcf-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


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



<span data-ttu-id="93fcf-248">Beachten Sie, dass der Aufrufer einen einzelnen Puffer mit einer Speicher \_ Eigenschafts \_ Abfrage und der Größe der \_ spezifischen Speicher Protokolldaten zuordnen muss \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93fcf-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="93fcf-249">In diesem Beispiel wird derselbe Puffer für die Eingabe und die Ausgabe der Eigenschaften Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="93fcf-250">Daher hat der zugewiesene Puffer die Größe "Feld \_ Offset (Speicher \_ Eigenschaften \_ Abfrage, AdditionalParameters) + sizeof (Speicher \_ Protokoll \_ spezifische \_ Daten) + nvme \_ Max \_ log \_ size".</span><span class="sxs-lookup"><span data-stu-id="93fcf-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="93fcf-251">Obwohl separate Puffer sowohl für die Eingabe als auch für die Ausgabe reserviert werden können, empfiehlt sich die Verwendung eines einzelnen Puffers, um nvme-bezogene Informationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="93fcf-252">Beispiel: nvme Get Log Pages Query</span><span class="sxs-lookup"><span data-stu-id="93fcf-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="93fcf-253">In diesem Beispiel, basierend auf dem vorherigen, wird die Anforderung _ *Get Log Pages*\* an ein nvme-Laufwerk gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="93fcf-254">Der folgende Code bereitet die Abfrage Datenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="93fcf-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


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



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="93fcf-255">Beispiel: nvme Get Features Query</span><span class="sxs-lookup"><span data-stu-id="93fcf-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="93fcf-256">In diesem Beispiel, basierend auf dem vorherigen, wird die Anforderung _ *Get Features*\* an ein nvme-Laufwerk gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="93fcf-257">Der folgende Code bereitet die Abfrage Datenstruktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="93fcf-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


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
## <a name="protocol-specific-set"></a><span data-ttu-id="93fcf-258">Protokoll spezifischer Satz</span><span class="sxs-lookup"><span data-stu-id="93fcf-258">Protocol-specific set</span></span>

<span data-ttu-id="93fcf-259">Aus Windows 10 19h1 wurde die IOCTL_STORAGE_SET_PROPERTY verbessert, um die Funktionen von nvme-Sets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="93fcf-260">Der Eingabepuffer für das IOCTL_STORAGE_SET_PROPERTY wird hier angezeigt:</span><span class="sxs-lookup"><span data-stu-id="93fcf-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

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

<span data-ttu-id="93fcf-261">Wenn Sie IOCTL_STORAGE_SET_PROPERTY verwenden, um die nvme-Funktion festzulegen, konfigurieren Sie die STORAGE_PROPERTY_SET Struktur wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93fcf-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="93fcf-262">Zuordnen eines Puffers, der sowohl eine STORAGE_PROPERTY_SET als auch eine STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur enthalten kann;</span><span class="sxs-lookup"><span data-stu-id="93fcf-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="93fcf-263">Legen Sie das Feld PropertyId auf storageadapterprotocolspecificproperty oder storagedeviceprotocolspecificproperty für eine Controller-oder Geräte-bzw. Namespace Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="93fcf-264">Füllen Sie die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT-Struktur mit den gewünschten Werten aus.</span><span class="sxs-lookup"><span data-stu-id="93fcf-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="93fcf-265">Der Anfang des STORAGE_PROTOCOL_SPECIFIC_DATA_EXT ist das AdditionalParameters-Feld STORAGE_PROPERTY_SET.</span><span class="sxs-lookup"><span data-stu-id="93fcf-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="93fcf-266">Die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

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

<span data-ttu-id="93fcf-267">Um einen Typ der festzulegenden nvme-Funktion anzugeben, konfigurieren Sie die STORAGE_PROTOCOL_SPECIFIC_DATA_EXT Struktur wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93fcf-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="93fcf-268">Legen Sie das Feld ProtocolType auf protocoltypvme fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="93fcf-269">Legen Sie das Feld DataType auf den Enumerationswert nvmedatatypfeature fest, der durch STORAGE_PROTOCOL_NVME_DATA_TYPE definiert wird.</span><span class="sxs-lookup"><span data-stu-id="93fcf-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="93fcf-270">In den folgenden Beispielen wird die nvme-Funktionsgruppe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="93fcf-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="93fcf-271">Beispiel: nvme-Set-Funktionen</span><span class="sxs-lookup"><span data-stu-id="93fcf-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="93fcf-272">In diesem Beispiel wird die Anforderung zum Festlegen von Features an ein nvme-Laufwerk gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="93fcf-273">Der folgende Code bereitet die Set Data-Struktur vor und sendet dann den Befehl über DeviceIoControl an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="93fcf-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

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

## <a name="temperature-queries"></a><span data-ttu-id="93fcf-274">Temperatur Abfragen</span><span class="sxs-lookup"><span data-stu-id="93fcf-274">Temperature queries</span></span>

<span data-ttu-id="93fcf-275">In Windows 10 kann die [**IOCTL \_ Storage \_ Query- \_ Eigenschaft**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) auch verwendet werden, um Temperaturdaten von nvme-Geräten abzufragen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="93fcf-276">Um Temperatur Informationen von einem nvme-Laufwerk im [**Speicher \_ Temperaturdaten \_ - \_ Deskriptor**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)abzurufen, konfigurieren Sie die Abfrage Struktur der [**Speicher \_ Eigenschaft \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93fcf-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="93fcf-277">Weisen Sie einen Puffer zu, der [**eine \_ \_ Abfrage Struktur der Speicher Eigenschaft**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="93fcf-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="93fcf-278">Legen Sie das Feld **PropertyId** auf **storageadaptertemperatureproperty** oder **storagedevicetemperatureproperty** für eine Controller-oder Geräte-bzw. Namespace Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="93fcf-279">Legen Sie das Feld **QueryType** auf **propertystandardquery** fest.</span><span class="sxs-lookup"><span data-stu-id="93fcf-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="93fcf-280">Die Struktur der [**Speicher \_ Temperatur \_ Informationen**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (aus Windows 10) wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


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



## <a name="behavior-changing-commands"></a><span data-ttu-id="93fcf-281">Verhaltens Wechsel Befehle</span><span class="sxs-lookup"><span data-stu-id="93fcf-281">Behavior changing commands</span></span>

<span data-ttu-id="93fcf-282">Befehle, die Geräte Attribute bearbeiten oder möglicherweise Auswirkungen auf das Geräteverhalten haben, können dem Betriebssystem erschwert werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="93fcf-283">Wenn sich Geräte Attribute zur Laufzeit ändern, während e/a-Vorgänge verarbeitet werden, können Synchronisierungs-oder Daten Integritäts Probleme auftreten, wenn Sie nicht ordnungsgemäß behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="93fcf-284">Der nvme **-Befehl "Set-Features** " ist ein gutes Beispiel für einen Verhaltens Wechsel.</span><span class="sxs-lookup"><span data-stu-id="93fcf-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="93fcf-285">Sie ermöglicht die Änderung des-Mechanismus für die Vermittlung und die Einstellung von Temperaturschwellen Werten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="93fcf-286">Um sicherzustellen, dass in-Flight-Daten nicht gefährdet sind, wenn verhaltensbezogene Set-Befehle gesendet werden, hält Windows alle e/a-Vorgänge für das nvme-Gerät an, entleert Warteschlangen und leert Puffer.</span><span class="sxs-lookup"><span data-stu-id="93fcf-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="93fcf-287">Nachdem der SET-Befehl erfolgreich ausgeführt wurde, wird die e/a-Vorgänge fortgesetzt (sofern möglich).</span><span class="sxs-lookup"><span data-stu-id="93fcf-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="93fcf-288">Wenn die e/a-Vorgänge nicht fortgesetzt werden können, ist möglicherweise eine Geräte Zurücksetzung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93fcf-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="93fcf-289">Festlegen von Temperaturschwellen Werten</span><span class="sxs-lookup"><span data-stu-id="93fcf-289">Setting temperature thresholds</span></span>

<span data-ttu-id="93fcf-290">In Windows 10 wurde der [**IOCTL- \_ Speicher \_ Satz \_ Temperatur \_ Schwellenwert**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)eingeführt, eine ioctl zum erhalten und Festlegen von Temperaturschwellen Werten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="93fcf-291">Sie können es auch verwenden, um die aktuelle Temperatur des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="93fcf-292">Der Eingabe-/Ausgabepuffer für diese IOCTL ist die [**Speicher \_ Temperatur \_ Informations**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) Struktur aus dem vorherigen Code Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="93fcf-293">Beispiel: Festlegen der über-Schwellenwert Temperatur</span><span class="sxs-lookup"><span data-stu-id="93fcf-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="93fcf-294">In diesem Beispiel ist die Temperatur eines nvme-Laufwerks über Schwellenwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="93fcf-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="93fcf-295">Mit dem folgenden Code wird der Befehl vorbereitet und dann über DeviceIoControl an das Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="93fcf-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


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



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="93fcf-296">Festlegen Hersteller spezifischer Features</span><span class="sxs-lookup"><span data-stu-id="93fcf-296">Setting vendor-specific features</span></span>

<span data-ttu-id="93fcf-297">Ohne das Befehls Effekt Protokoll hat der Treiber keine Kenntnis von den Auswirkungen des Befehls.</span><span class="sxs-lookup"><span data-stu-id="93fcf-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="93fcf-298">Aus diesem Grund ist das Befehls Effekt Protokoll erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93fcf-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="93fcf-299">Dadurch kann das Betriebssystem ermitteln, ob ein Befehl eine hohe Auswirkung hat und ob er parallel mit anderen Befehlen an das Laufwerk gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="93fcf-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="93fcf-300">Das Befehls Effekt Protokoll ist noch nicht genau genug, um anbieterspezifische **Set-Features** -Befehle einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="93fcf-301">Aus diesem Grund ist es noch nicht möglich, anbieterspezifische **Set-Features-** Befehle zu senden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="93fcf-302">Es ist jedoch möglich, den zuvor erläuterten Pass-Through-Mechanismus zum Senden Hersteller spezifischer Befehle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="93fcf-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="93fcf-303">Weitere Informationen finden Sie unter [Pass-Through-Mechanismus](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="93fcf-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="93fcf-304">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="93fcf-304">Header files</span></span>

<span data-ttu-id="93fcf-305">Die folgenden Dateien sind für die nvme-Entwicklung relevant.</span><span class="sxs-lookup"><span data-stu-id="93fcf-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="93fcf-306">Diese Dateien sind im [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads)enthalten.</span><span class="sxs-lookup"><span data-stu-id="93fcf-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="93fcf-307">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="93fcf-307">Header file</span></span>    | <span data-ttu-id="93fcf-308">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93fcf-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93fcf-309">**ntddstor. h**</span><span class="sxs-lookup"><span data-stu-id="93fcf-309">**ntddstor.h**</span></span> | <span data-ttu-id="93fcf-310">Definiert Konstanten und Typen für den Zugriff auf die Speicher Klassen Treiber aus dem Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="93fcf-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="93fcf-311">**nvme. h**</span><span class="sxs-lookup"><span data-stu-id="93fcf-311">**nvme.h**</span></span>     | <span data-ttu-id="93fcf-312">Für andere nvme-bezogene Datenstrukturen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="93fcf-313">**winioctl. h**</span><span class="sxs-lookup"><span data-stu-id="93fcf-313">**winioctl.h**</span></span> | <span data-ttu-id="93fcf-314">Für allgemeine Win32-ioctl-Definitionen, einschließlich Speicher-APIs für Benutzermodusanwendungen.</span><span class="sxs-lookup"><span data-stu-id="93fcf-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
