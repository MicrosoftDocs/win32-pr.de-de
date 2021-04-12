---
description: Die Win32 \_ serialportconfiguration-WMI-Klasse stellt die Einstellungen für die Datenübertragung an einem Windows-basierten seriellen Anschluss dar. Dies schließt Konfigurationen für das Herstellen einer Verbindung und Fehlerüberprüfung ein.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958201"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="05a58-104">Win32 \_ serialportconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="05a58-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="05a58-105">Die **Win32 \_ serialportconfiguration** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Einstellungen für die Datenübertragung an einem Windows-basierten seriellen Anschluss dar.</span><span class="sxs-lookup"><span data-stu-id="05a58-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="05a58-106">Dies schließt Konfigurationen für das Herstellen einer Verbindung und Fehlerüberprüfung ein.</span><span class="sxs-lookup"><span data-stu-id="05a58-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="05a58-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05a58-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="05a58-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="05a58-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a58-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="05a58-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="05a58-110">Member</span><span class="sxs-lookup"><span data-stu-id="05a58-110">Members</span></span>

<span data-ttu-id="05a58-111">Die **Win32 \_ serialportconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="05a58-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="05a58-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05a58-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05a58-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05a58-113">Properties</span></span>

<span data-ttu-id="05a58-114">Die **Win32 \_ serialportconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05a58-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05a58-115">**Abortreadschreiteonerror**</span><span class="sxs-lookup"><span data-stu-id="05a58-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-118">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fabortonerror")</span><span class="sxs-lookup"><span data-stu-id="05a58-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-119">**True** gibt an, dass Lese-und Schreibvorgänge beendet werden, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="05a58-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="05a58-120">**True** gibt an, dass der Treiber alle Lese-und Schreibvorgänge mit einem Fehlerstatus beendet, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="05a58-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="05a58-121">Der Treiber nimmt keine weiteren Kommunikations Vorgänge an, bis der Fehler von der Anwendung bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-122">**' Baudrate '**</span><span class="sxs-lookup"><span data-stu-id="05a58-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-125">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Baudrate")</span><span class="sxs-lookup"><span data-stu-id="05a58-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-126">Die Baudrate (Bits pro Sekunde), mit der das Kommunikationsgerät betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="05a58-127">Beispiel: 9600</span><span class="sxs-lookup"><span data-stu-id="05a58-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="05a58-128">**Binarymodeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="05a58-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-131">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sbinary")</span><span class="sxs-lookup"><span data-stu-id="05a58-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-132">**True** gibt an, dass Datenübertragungen im binären Modus für den seriellen Anschluss aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="05a58-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="05a58-133">Computer Systeme, auf denen Windows ausgeführt wird, erlauben nur binäre Übertragungen über serielle Ports, sodass dieser Wert immer **true** ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-134">**Bitsperbyte**</span><span class="sxs-lookup"><span data-stu-id="05a58-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-137">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")</span><span class="sxs-lookup"><span data-stu-id="05a58-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-138">Anzahl von Bits, die für jedes Byte von Daten für den seriellen Port von Windows übertragen und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="05a58-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="05a58-139">Die Zahl kann sich mit Steuerelementen und Fehlerkorrektur Bits (z. b. Paritätsbits) unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="05a58-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="05a58-140">Beispiel: 8</span><span class="sxs-lookup"><span data-stu-id="05a58-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="05a58-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="05a58-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-144">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="05a58-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="05a58-145">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="05a58-145">Short textual description of the current object.</span></span>

<span data-ttu-id="05a58-146">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="05a58-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a58-147">**ContinueXMitOnXOff**</span><span class="sxs-lookup"><span data-stu-id="05a58-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-150">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ftxcontinueonxoff")</span><span class="sxs-lookup"><span data-stu-id="05a58-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-151">**True** gibt an, dass Datenübertragungen fortgesetzt werden, wenn der Eingabepuffer in **XOffXMitThreshold** Bytes voll ist und der Treiber den **xoffchararcter** -Wert übertragen hat, um den Empfang von Bytes zu beenden.</span><span class="sxs-lookup"><span data-stu-id="05a58-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="05a58-152">Der Wert **false** gibt an, dass die Übertragung nicht fortgesetzt wird, bis der Eingabepuffer innerhalb des **XOnXMitThreshold** -Bytes leer ist und der Treiber den **XOnCharacter** -Wert zum Fortsetzen des Empfangs verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="05a58-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-153">**Czoutflowcontrol**</span><span class="sxs-lookup"><span data-stu-id="05a58-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-154">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-156">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| loutxczflow")</span><span class="sxs-lookup"><span data-stu-id="05a58-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-157">Wenn der Wert **true** ist, wird das Signal "Clear to Send (CTS)" vor der Datenübertragung geprüft.</span><span class="sxs-lookup"><span data-stu-id="05a58-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="05a58-158">CTS signalisiert, dass beide Geräte der seriellen Verbindung zum Übertragen von Daten bereit sind.</span><span class="sxs-lookup"><span data-stu-id="05a58-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="05a58-159">Die Datenübertragung wird angehalten, bis das CTS-Signal angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05a58-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05a58-163">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="05a58-163">Textual description of the current object.</span></span>

<span data-ttu-id="05a58-164">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="05a58-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a58-165">**Verwerdnullbytes**</span><span class="sxs-lookup"><span data-stu-id="05a58-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-166">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-168">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| f NULL")</span><span class="sxs-lookup"><span data-stu-id="05a58-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-169">**True** gibt an, dass **null** -bytes (Zeichen) beim Empfang verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="05a58-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-170">**DSROutflowControl**</span><span class="sxs-lookup"><span data-stu-id="05a58-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-171">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-173">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fioutxdsrflow")</span><span class="sxs-lookup"><span data-stu-id="05a58-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-174">**True** gibt an, dass die Datenflusssteuerung aktiviert ist, wenn eine DSR-Bedingung (Data Set Ready) vorliegt.</span><span class="sxs-lookup"><span data-stu-id="05a58-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="05a58-175">DSR signalisiert, dass die Verbindung von den Geräten der seriellen Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="05a58-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="05a58-176">Die DSR-Datenübertragung wird angehalten, bis das DSR-Signal angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-177">**Dsrsensitivität**</span><span class="sxs-lookup"><span data-stu-id="05a58-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-178">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-180">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sdsrsensisensitivität")</span><span class="sxs-lookup"><span data-stu-id="05a58-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-181">**True** gibt an, dass der Kommunikationstreiber für den Zustand des DSR-Signals sensibel ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="05a58-182">Der Treiber ignoriert alle empfangenen Bytes, es sei denn, die DSR-Modem-Eingabezeile ist hoch.</span><span class="sxs-lookup"><span data-stu-id="05a58-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-183">**DTRFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="05a58-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-186">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sdtrcontrol")</span><span class="sxs-lookup"><span data-stu-id="05a58-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-187">Verwendung der DTR-Fluss Steuerung (Data Terminal Ready), nachdem eine Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="05a58-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="05a58-188">**Aktivieren** ("aktivieren")</span><span class="sxs-lookup"><span data-stu-id="05a58-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="05a58-189">**Deaktivieren** ("deaktivieren")</span><span class="sxs-lookup"><span data-stu-id="05a58-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="05a58-190">**Handshake** ("Handshake")</span><span class="sxs-lookup"><span data-stu-id="05a58-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05a58-191">**EOF-Zeichen**</span><span class="sxs-lookup"><span data-stu-id="05a58-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-192">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-194">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EOF char")</span><span class="sxs-lookup"><span data-stu-id="05a58-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-195">Der Wert des Zeichens, das verwendet wird, um das Ende der Daten zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="05a58-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="05a58-196">Beispiel: ^ Z</span><span class="sxs-lookup"><span data-stu-id="05a58-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="05a58-197">**Errorreplacecharacter**</span><span class="sxs-lookup"><span data-stu-id="05a58-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-198">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-200">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")</span><span class="sxs-lookup"><span data-stu-id="05a58-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-201">Der Wert des Zeichens, mit dem Bytes ersetzt werden, die mit einem Paritätsfehler empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="05a58-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="05a58-202">Beispiel: ^ C</span><span class="sxs-lookup"><span data-stu-id="05a58-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="05a58-203">**Errorreplacementaktivierte**</span><span class="sxs-lookup"><span data-stu-id="05a58-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-204">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-206">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ferrorchar")</span><span class="sxs-lookup"><span data-stu-id="05a58-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-207">**True** gibt an, dass mit Paritäts Fehlern empfangene Bytes durch den Wert **errorreplacecharacter** ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="05a58-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="05a58-208">Zeichen mit Paritäts Fehlern werden nur ersetzt, wenn diese Eigenschaft den Wert **true** hat und die Parität aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-209">**EventCharacter**</span><span class="sxs-lookup"><span data-stu-id="05a58-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-210">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-212">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| evtchar")</span><span class="sxs-lookup"><span data-stu-id="05a58-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-213">Der Wert des Steuer Zeichens, das zum Signalisieren eines Ereignisses verwendet wird, z. b. das Ende der Datei.</span><span class="sxs-lookup"><span data-stu-id="05a58-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="05a58-214">Beispiel: ^ e</span><span class="sxs-lookup"><span data-stu-id="05a58-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="05a58-215">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="05a58-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-216">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-218">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Functions-Dateifunktionen \| ")</span><span class="sxs-lookup"><span data-stu-id="05a58-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-219">**True** gibt an, dass der serielle Port ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-220">**Name**</span><span class="sxs-lookup"><span data-stu-id="05a58-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-223">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware- \\ \\ mappcemap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="05a58-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-224">Name des seriellen Windows-Ports.</span><span class="sxs-lookup"><span data-stu-id="05a58-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="05a58-225">Beispiel: "COM1"</span><span class="sxs-lookup"><span data-stu-id="05a58-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="05a58-226">**Parität**</span><span class="sxs-lookup"><span data-stu-id="05a58-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-229">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parität")</span><span class="sxs-lookup"><span data-stu-id="05a58-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-230">Methode der zu verwendenden Paritäts Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="05a58-230">Method of parity checking to be used.</span></span> <span data-ttu-id="05a58-231">Parität wird als Fehler Überprüfungs Methode verwendet, bei der ein zusätzliches Paritäts Bit in jeder Dateneinheit enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="05a58-232">Der Empfänger kann dann die Gültigkeit der Daten überprüfen, indem er die Bits zählt, die festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="05a58-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="05a58-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="05a58-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-234">Die Paritäts Überprüfung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="05a58-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="05a58-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Ungerade** ("ungerade")</span><span class="sxs-lookup"><span data-stu-id="05a58-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-236">Legt das Paritätsbit fest, sodass die Anzahl der festgelegten Bits eine ungerade Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="05a58-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Sogar** ("auch")</span><span class="sxs-lookup"><span data-stu-id="05a58-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-238">Legt das Paritätsbit fest, sodass die Anzahl der festgelegten Bits eine gerade Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="05a58-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span><span class="sxs-lookup"><span data-stu-id="05a58-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-240">Behält die Festlegung des Paritätsbits auf 1 bei.</span><span class="sxs-lookup"><span data-stu-id="05a58-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="05a58-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Leerzeichen** ("Leerraum")</span><span class="sxs-lookup"><span data-stu-id="05a58-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-242">Lässt das Paritätsbit auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05a58-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05a58-243">**Parametercheckaktivierte**</span><span class="sxs-lookup"><span data-stu-id="05a58-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-244">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-246">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| f Parity")</span><span class="sxs-lookup"><span data-stu-id="05a58-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-247">**True** gibt an, dass die Paritäts Überprüfung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-248">**Rzflowcontroltype**</span><span class="sxs-lookup"><span data-stu-id="05a58-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05a58-251">Request to Send (RTS)-Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="05a58-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="05a58-252">RTS wird verwendet, um zu signalisieren, dass Daten für die Übertragung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="05a58-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="05a58-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Aktivieren** ("aktivieren")</span><span class="sxs-lookup"><span data-stu-id="05a58-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-254">RTS ist für die Datenübertragungs Sitzung noch nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="05a58-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="05a58-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** ("deaktivieren")</span><span class="sxs-lookup"><span data-stu-id="05a58-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-256">RTS wird ignoriert, nachdem das erste RTS-Signal empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="05a58-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="05a58-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span><span class="sxs-lookup"><span data-stu-id="05a58-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-258">RTS ist deaktiviert, wenn der Übertragungs Puffer mehr als drei Quartale voll ist, und RTS aktiviert ist, wenn der Puffer kleiner als 1-halbist.</span><span class="sxs-lookup"><span data-stu-id="05a58-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="05a58-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Umschalten ("** umschalten")</span><span class="sxs-lookup"><span data-stu-id="05a58-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="05a58-260">RTS ist eingeschaltet, wenn für die Übertragung Daten gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="05a58-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05a58-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="05a58-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-264">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="05a58-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="05a58-265">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="05a58-266">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="05a58-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a58-267">**Stoppbits**</span><span class="sxs-lookup"><span data-stu-id="05a58-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05a58-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-270">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Stopbits")</span><span class="sxs-lookup"><span data-stu-id="05a58-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-271">Anzahl der zu verwendenden Stoppbits.</span><span class="sxs-lookup"><span data-stu-id="05a58-271">Number of stop bits to be used.</span></span> <span data-ttu-id="05a58-272">Beenden Sie Bits trennen Sie jede Einheit von Daten in einer asynchronen seriellen Verbindung.</span><span class="sxs-lookup"><span data-stu-id="05a58-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="05a58-273">Sie werden auch fortlaufend gesendet, wenn keine Daten für die Übertragung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="05a58-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="05a58-274">**1** ("1")</span><span class="sxs-lookup"><span data-stu-id="05a58-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="05a58-275">**1,5** ("1,5")</span><span class="sxs-lookup"><span data-stu-id="05a58-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="05a58-276">**2** ("2")</span><span class="sxs-lookup"><span data-stu-id="05a58-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05a58-277">**XOffCharacter**</span><span class="sxs-lookup"><span data-stu-id="05a58-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-278">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-280">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")</span><span class="sxs-lookup"><span data-stu-id="05a58-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-281">Der Wert des XOFF-Zeichens sowohl für die Übertragung als auch für den Empfang.</span><span class="sxs-lookup"><span data-stu-id="05a58-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="05a58-282">XOFF ist ein Software Steuerelement, mit dem die Datenübertragung beendet wird (während "RTS" und "CTS" Hardware Steuerelemente sind).</span><span class="sxs-lookup"><span data-stu-id="05a58-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="05a58-283">XOn nimmt die Übertragung wieder auf.</span><span class="sxs-lookup"><span data-stu-id="05a58-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-284">**XOffXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="05a58-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-287">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| xofflim")</span><span class="sxs-lookup"><span data-stu-id="05a58-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-288">Maximale Anzahl von Bytes, die im Eingabepuffer zulässig sind, bevor das XOff-Zeichen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-289">**XOnCharacter**</span><span class="sxs-lookup"><span data-stu-id="05a58-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-290">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-292">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")</span><span class="sxs-lookup"><span data-stu-id="05a58-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-293">Der Wert des XOn-Zeichens für die Übertragung und den Empfang.</span><span class="sxs-lookup"><span data-stu-id="05a58-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="05a58-294">XOn ist ein Software Steuerelement, mit dem die Datenübertragung fortgesetzt werden kann (während RTS und CTS Hardware Steuerelemente sind).</span><span class="sxs-lookup"><span data-stu-id="05a58-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="05a58-295">XOFF beendet die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="05a58-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-296">**XOnXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="05a58-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-297">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-299">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")</span><span class="sxs-lookup"><span data-stu-id="05a58-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-300">Mindestanzahl von Bytes, die im Eingabepuffer zulässig sind, bevor das XON-Zeichen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="05a58-301">Diese Eigenschaft funktioniert in Verbindung mit **XOffXMitThreshold** , um die Rate zu steuern, mit der Daten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="05a58-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="05a58-302">**XOnXOffInFlowControl**</span><span class="sxs-lookup"><span data-stu-id="05a58-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-303">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-305">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| finx")</span><span class="sxs-lookup"><span data-stu-id="05a58-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-306">**True** gibt an, dass die "XON/XOFF"-Fluss Steuerung beim Empfang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="05a58-307">**True** gibt an, dass der **XOffCharacter** -Wert gesendet wird, wenn der Eingabepuffer in die **XOffXMitThreshold** -Bytes voll ist, und der **XOnCharacter** -Wert gesendet wird, wenn der Eingabepuffer in die **XOnXMitThreshold** -Bytes leer ist.</span><span class="sxs-lookup"><span data-stu-id="05a58-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="05a58-308"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="05a58-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="05a58-309">false</span><span class="sxs-lookup"><span data-stu-id="05a58-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="05a58-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="05a58-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="05a58-311">TRUE</span><span class="sxs-lookup"><span data-stu-id="05a58-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05a58-312">**XOnXOffOutFlowControl**</span><span class="sxs-lookup"><span data-stu-id="05a58-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05a58-313">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05a58-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05a58-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05a58-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05a58-315">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| f")</span><span class="sxs-lookup"><span data-stu-id="05a58-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="05a58-316">Das **XOnXOffOutFlowControl** -Element gibt an, ob bei der Übertragung die XOn-oder XOFF-Fluss Steuerung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="05a58-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="05a58-317">Wenn **true**, wird die Übertragung beendet, wenn der **XOffCharacter** -Wert empfangen wird, und wird erneut gestartet, wenn der **XOnCharacter** -Wert empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="05a58-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05a58-318">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05a58-318">Remarks</span></span>

<span data-ttu-id="05a58-319">Die Win32-Klasse " **\_ serialportconfiguration** " wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05a58-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05a58-320">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05a58-320">Requirements</span></span>



| <span data-ttu-id="05a58-321">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05a58-321">Requirement</span></span> | <span data-ttu-id="05a58-322">Wert</span><span class="sxs-lookup"><span data-stu-id="05a58-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05a58-323">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05a58-323">Minimum supported client</span></span><br/> | <span data-ttu-id="05a58-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05a58-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05a58-325">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05a58-325">Minimum supported server</span></span><br/> | <span data-ttu-id="05a58-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05a58-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05a58-327">Namespace</span><span class="sxs-lookup"><span data-stu-id="05a58-327">Namespace</span></span><br/>                | <span data-ttu-id="05a58-328">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="05a58-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05a58-329">MOF</span><span class="sxs-lookup"><span data-stu-id="05a58-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05a58-330"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05a58-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05a58-331">DLL</span><span class="sxs-lookup"><span data-stu-id="05a58-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05a58-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05a58-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a58-333">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05a58-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a58-334">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="05a58-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="05a58-335">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="05a58-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
