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

Die **CIM \_** -Klasse "-Klasse" verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_** -Klasse "-Klasse" verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Ruft einen USB-Gerätedeskriptor ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_** -Klasse "-Klasse" verfügt über diese Eigenschaften.

<dl> <dt>

**Classcode**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bdeviceclass")
</dt> </dl>

Der USB-Klassen Code.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Timeout Intervall, das von Verwaltungs Anwendungen konfiguriert werden kann, die die USB-Umleitung unterstützen. Wenn der Umleitungs Dienst einen USB-Geräte Befehl an ein Remote Gerät umleitet und das Remote Gerät nicht vor einem Timeout Intervall antwortet, emuliert der Umleitungs Dienst ein Medien-auswerfen-Ereignis. Außerdem kann der Dienst den Befehl wiederholen oder versuchen, die Verbindung mit dem Remote Gerät wiederherzustellen.

</dd> <dt>

**Currentalternative esettings**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Start **\_ Gerät**".**Currentconfigvalue**")
</dt> </dl>

Ein Array, das die alternativen Einstellungen für jede Schnittstelle in der aktuellen Konfiguration des Geräts enthält.

</dd> <dt>

**Currentconfigvalue**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Start **\_ Gerät**".**Currentalternativ esettings**")
</dt> </dl>

Die Konfiguration, die zurzeit für das Gerät ausgewählt ist. Wenn dieser Wert 0 (null) ist, ist das Gerät nicht konfiguriert.

</dd> <dt>

**Devicereleasenumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-IF \| Standard-Gerätedeskriptor \| bcddevice")
</dt> </dl>

Die Geräte Freigabe Nummer im BCD-Format.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| imanufacturer")
</dt> </dl>

Die Hersteller Zeichenfolge des Geräts.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bmaxpacketsize")
</dt> </dl>

Die maximale Paketgröße für den USB-Endpunkt NULL.

</dd> <dt>

**Anzahlungskonfigurationen**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-IF \| Standard-Gerätedeskriptor \| bnumkonfigurationen")
</dt> </dl>

Die Anzahl der Geräte Konfigurationen, die für das Gerät definiert sind.

</dd> <dt>

**Produkt**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| iproduct")
</dt> </dl>

Die Produkt Zeichenfolge des Geräts.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-IF \| Standard-Gerätedeskriptor \| idProduct")
</dt> </dl>

Die Produkt-ID, die dem Gerät vom Hersteller zugewiesen wird.

</dd> <dt>

**Protocolcode**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bdeviceprotocol")
</dt> </dl>

Der USB-Protokollcode.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| iserialnumber")
</dt> </dl>

Die Seriennummer des Geräts.

</dd> <dt>

**Subclasscode**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("universelle serielle Busspezifikation. USB-Wenn \| Standard Gerätedeskriptor \| bdevicesubclass")
</dt> </dl>

Der USB-Unterklassen Code.

</dd> <dt>

**Start Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die neueste USB-Version, die vom USB-Gerät unterstützt wird. Die-Eigenschaft wird als Binär codiertes Dezimaltrennzeichen (BCD) ausgedrückt, das einen Dezimaltrennzeichen zwischen den 2. und dritten Ziffern enthält. Der Wert 0x201 gibt z. b. an, dass Version 2,01 unterstützt wird.

</dd> <dt>

**Start-CD**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Device Descriptor \| bcdUSB")
</dt> </dl>

Die Nummer der USB-Spezifikation, der das Gerät entspricht. Diese Eigenschaft ist mit dem BCD-Format formatiert.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-IF \| Standard Gerätedeskriptor \| idVendor")
</dt> </dl>

Die Anbieter-ID, die dem Gerät durch USB.org zugewiesen ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

