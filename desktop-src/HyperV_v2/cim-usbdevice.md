---
description: Die Verwaltungsmerkmale eines USB-Geräts.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: CIM_USBDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372983"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="fc619-103">CIM_USBDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="fc619-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="fc619-104">Die Verwaltungsmerkmale eines USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="fc619-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc619-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc619-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a><span data-ttu-id="fc619-106">Member</span><span class="sxs-lookup"><span data-stu-id="fc619-106">Members</span></span>

<span data-ttu-id="fc619-107">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fc619-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="fc619-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="fc619-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc619-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc619-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc619-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="fc619-110">Methods</span></span>

<span data-ttu-id="fc619-111">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fc619-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="fc619-112">Methode</span><span class="sxs-lookup"><span data-stu-id="fc619-112">Method</span></span>                                               | <span data-ttu-id="fc619-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc619-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="fc619-114">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc619-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="fc619-115">Ruft einen USB-Gerätedeskriptor ab.</span><span class="sxs-lookup"><span data-stu-id="fc619-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fc619-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc619-116">Properties</span></span>

<span data-ttu-id="fc619-117">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc619-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc619-118">**Classcode**</span><span class="sxs-lookup"><span data-stu-id="fc619-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-119">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc619-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-121">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bdeviceclass")</span><span class="sxs-lookup"><span data-stu-id="fc619-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-122">Der USB-Klassen Code.</span><span class="sxs-lookup"><span data-stu-id="fc619-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-123">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="fc619-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-124">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc619-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc619-126">Ein Timeout Intervall, das von Verwaltungs Anwendungen konfiguriert werden kann, die die USB-Umleitung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fc619-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="fc619-127">Wenn der Umleitungs Dienst einen USB-Geräte Befehl an ein Remote Gerät umleitet und das Remote Gerät nicht vor einem Timeout Intervall antwortet, emuliert der Umleitungs Dienst ein Medien-auswerfen-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fc619-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="fc619-128">Außerdem kann der Dienst den Befehl wiederholen oder versuchen, die Verbindung mit dem Remote Gerät wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="fc619-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-129">**Currentalternative esettings**</span><span class="sxs-lookup"><span data-stu-id="fc619-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-130">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="fc619-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fc619-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-132">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Start **\_ Gerät**".**Currentconfigvalue**")</span><span class="sxs-lookup"><span data-stu-id="fc619-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-133">Ein Array, das die alternativen Einstellungen für jede Schnittstelle in der aktuellen Konfiguration des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="fc619-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-134">**Currentconfigvalue**</span><span class="sxs-lookup"><span data-stu-id="fc619-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-135">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc619-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-137">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Start **\_ Gerät**".**Currentalternativ esettings**")</span><span class="sxs-lookup"><span data-stu-id="fc619-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-138">Die Konfiguration, die zurzeit für das Gerät ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fc619-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="fc619-139">Wenn dieser Wert 0 (null) ist, ist das Gerät nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="fc619-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-140">**Devicereleasenumber**</span><span class="sxs-lookup"><span data-stu-id="fc619-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc619-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-IF \| Standard-Gerätedeskriptor \| bcddevice")</span><span class="sxs-lookup"><span data-stu-id="fc619-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-144">Die Geräte Freigabe Nummer im BCD-Format.</span><span class="sxs-lookup"><span data-stu-id="fc619-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-145">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="fc619-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fc619-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| imanufacturer")</span><span class="sxs-lookup"><span data-stu-id="fc619-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-149">Die Hersteller Zeichenfolge des Geräts.</span><span class="sxs-lookup"><span data-stu-id="fc619-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="fc619-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-151">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc619-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-153">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bmaxpacketsize")</span><span class="sxs-lookup"><span data-stu-id="fc619-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-154">Die maximale Paketgröße für den USB-Endpunkt NULL.</span><span class="sxs-lookup"><span data-stu-id="fc619-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-155">**Anzahlungskonfigurationen**</span><span class="sxs-lookup"><span data-stu-id="fc619-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-156">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc619-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-158">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-IF \| Standard-Gerätedeskriptor \| bnumkonfigurationen")</span><span class="sxs-lookup"><span data-stu-id="fc619-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-159">Die Anzahl der Geräte Konfigurationen, die für das Gerät definiert sind.</span><span class="sxs-lookup"><span data-stu-id="fc619-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-160">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="fc619-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fc619-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-163">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| iproduct")</span><span class="sxs-lookup"><span data-stu-id="fc619-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-164">Die Produkt Zeichenfolge des Geräts.</span><span class="sxs-lookup"><span data-stu-id="fc619-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-165">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="fc619-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc619-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-168">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-IF \| Standard-Gerätedeskriptor \| idProduct")</span><span class="sxs-lookup"><span data-stu-id="fc619-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-169">Die Produkt-ID, die dem Gerät vom Hersteller zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fc619-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-170">**Protocolcode**</span><span class="sxs-lookup"><span data-stu-id="fc619-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-171">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc619-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-173">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bdeviceprotocol")</span><span class="sxs-lookup"><span data-stu-id="fc619-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-174">Der USB-Protokollcode.</span><span class="sxs-lookup"><span data-stu-id="fc619-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-175">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="fc619-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fc619-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-178">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| iserialnumber")</span><span class="sxs-lookup"><span data-stu-id="fc619-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-179">Die Seriennummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="fc619-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-180">**Subclasscode**</span><span class="sxs-lookup"><span data-stu-id="fc619-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-181">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc619-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-183">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-Wenn \| Standard Gerätedeskriptor \| bdevicesubclass")</span><span class="sxs-lookup"><span data-stu-id="fc619-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-184">Der USB-Unterklassen Code.</span><span class="sxs-lookup"><span data-stu-id="fc619-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-185">**Start Version**</span><span class="sxs-lookup"><span data-stu-id="fc619-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-186">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc619-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc619-188">Die neueste USB-Version, die vom USB-Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fc619-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="fc619-189">Die-Eigenschaft wird als Binär codiertes Dezimaltrennzeichen (BCD) ausgedrückt, das einen Dezimaltrennzeichen zwischen den 2. und dritten Ziffern enthält.</span><span class="sxs-lookup"><span data-stu-id="fc619-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="fc619-190">Der Wert 0x201 gibt z. b. an, dass Version 2,01 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fc619-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-191">**Start-CD**</span><span class="sxs-lookup"><span data-stu-id="fc619-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-192">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc619-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-194">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bcdUSB")</span><span class="sxs-lookup"><span data-stu-id="fc619-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-195">Die Nummer der USB-Spezifikation, der das Gerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="fc619-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="fc619-196">Diese Eigenschaft ist mit dem BCD-Format formatiert.</span><span class="sxs-lookup"><span data-stu-id="fc619-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="fc619-197">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="fc619-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc619-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc619-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc619-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc619-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc619-200">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Gerätedeskriptor \| idVendor")</span><span class="sxs-lookup"><span data-stu-id="fc619-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="fc619-201">Die Anbieter-ID, die dem Gerät durch USB.org zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fc619-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc619-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc619-202">Requirements</span></span>



| <span data-ttu-id="fc619-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc619-203">Requirement</span></span> | <span data-ttu-id="fc619-204">Wert</span><span class="sxs-lookup"><span data-stu-id="fc619-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc619-205">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc619-205">Minimum supported client</span></span><br/> | <span data-ttu-id="fc619-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fc619-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fc619-207">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc619-207">Minimum supported server</span></span><br/> | <span data-ttu-id="fc619-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fc619-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fc619-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc619-209">Namespace</span></span><br/>                | <span data-ttu-id="fc619-210">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc619-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc619-211">MOF</span><span class="sxs-lookup"><span data-stu-id="fc619-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc619-212"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fc619-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc619-213">DLL</span><span class="sxs-lookup"><span data-stu-id="fc619-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc619-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc619-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc619-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc619-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc619-216">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="fc619-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

