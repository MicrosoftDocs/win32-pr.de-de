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
ms.openlocfilehash: 3766d6c2fdc46b36350e9259e0e988f3a276cee6376d02de349abbe83bf8031b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427730"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>CIM_USBDevice-Klasse (Hyper-V-Verwaltung)

Die Verwaltungsmerkmale eines USB-Geräts.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **CIM \_ USBDevice-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ USBDevice-Klasse** verfügt über diese Methoden.



| Methode                                               | Beschreibung                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Ruft einen USB-Gerätedeskriptor ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ USBDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceClass")
</dt> </dl>

Der USB-Klassencode.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Timeoutintervall, das von Verwaltungsanwendungen konfiguriert werden kann, die die USB-Umleitung unterstützen. Wenn der Umleitungsdienst einen USB-Gerätebefehl an ein Remotegerät umleitet und das Remotegerät nicht vor dem Timeoutintervall antwortet, emuliert der Umleitungsdienst ein Medienauswerfenereignis. Darüber hinaus kann der Dienst den Befehl erneut versuchen oder versuchen, die Verbindung mit dem Remotegerät herzustellen.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")
</dt> </dl>

Ein Array, das die alternativen Einstellungen für jede Schnittstelle in der aktuellen Konfiguration des Geräts enthält.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")
</dt> </dl>

Die konfiguration, die derzeit für das Gerät ausgewählt ist. Wenn dieser Wert 0 (null) ist, ist das Gerät nicht konfiguriert.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bcdDevice")
</dt> </dl>

Die Gerätefreigabenummer im BCD-Format.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iManufacturer")
</dt> </dl>

Die Herstellerzeichenfolge des Geräts.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bMaxPacketSize")
</dt> </dl>

Die maximale Paketgröße für den USB-Endpunkt 0 (null).

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bNumConfigurations")
</dt> </dl>

Die Anzahl der Gerätekonfigurationen, die für das Gerät definiert sind.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iProduct")
</dt> </dl>

Die Produktzeichenfolge des Geräts.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| idProduct")
</dt> </dl>

Die Produkt-ID, die dem Gerät nach Hersteller zugewiesen ist.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceProtocol")
</dt> </dl>

Der USB-Protokollcode.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iSerialNumber")
</dt> </dl>

Die Seriennummer des Geräts.

</dd> <dt>

**UnterklasseCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceSubClass")
</dt> </dl>

Der USB-Unterklassencode.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die neueste USB-Version, die vom USB-Gerät unterstützt wird. Die -Eigenschaft wird als binär codierte Dezimalzahl (Binary-Coded Decimal, BCD) ausgedrückt, die ein Dezimaltrennzeichen zwischen der 2. und 3. Ziffer enthält. Beispielsweise gibt der Wert 0x201 an, dass Version 2.01 unterstützt wird.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bcdUSB")
</dt> </dl>

Die USB-Spezifikationsnummer, der das Gerät entspricht. Diese Eigenschaft wird im BCD-Format formatiert.

</dd> <dt>

**Vendorid**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| idVendor")
</dt> </dl>

Die Anbieter-ID, die dem Gerät durch die USB.org.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

