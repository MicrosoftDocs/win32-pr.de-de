---
description: Stellt ein Produkt dar. Dies schließt Software und Hardware ein, die auf diesem Computersystem verwendet wird.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Win32_ComputerSystemProduct-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47312acde8f346ac4ac3b2260fe06a2a5270610f9b7265da2b627a4c92fb4b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119294030"
---
# <a name="win32_computersystemproduct-class"></a>Win32 \_ ComputerSystemProduct-Klasse

Die **WMI-Klasse \_ Win32 ComputerSystemProduct** stellt ein Produkt dar. [](/windows/desktop/WmiSdk/retrieving-a-class) Dies schließt Software und Hardware ein, die auf diesem Computersystem verwendet wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a>Member

Die **Win32 \_ ComputerSystemProduct-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ComputerSystemProduct-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung für das Produkt.

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des Produkts.

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.4")
</dt> </dl>

Produktidentifikation, z. B. eine Seriennummer für Software, eine Die-Nummer auf einem Hardwarechip oder (bei nicht kommerziellen Produkten) eine Projektnummer.

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.2")
</dt> </dl>

Häufig verwendeter Produktname.

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> <dt>

**SKUNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Informationen zur Lagerbestandseinheit (Stock Keeping Unit, SKU) des Produkts.

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> <dt>

**UUID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| UUID")
</dt> </dl>

Universally Unique Identifier (UUID) für dieses Produkt. Eine UUID ist ein 128-Bit-Bezeichner, der sich garantiert von anderen generierten UUIDs unterscheiden kann. Wenn keine UUID verfügbar ist, wird eine UUID aller Nullen verwendet.

Dieser Wert stammt aus dem **UUID-Member** der Systeminformationen **struktur** in den SMBIOS-Informationen.

</dd> <dt>

**Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Taste,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.1")
</dt> </dl>

Der Name des Lieferanten des Produkts oder die Entität, die das Produkt verkauft (Hersteller, Handelspartner, OEM und so weiter).

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.3")
</dt> </dl>

Produktversionsinformationen.

Diese Eigenschaft wird vom [**\_ CIM-Produkt geerbt.**](cim-product.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ ComputerSystemProduct-Klasse** wird von [**CIM Product \_ abgeleitet.**](cim-product.md)

## <a name="examples"></a>Beispiele

Im [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell-Beispiel im TechNet-Katalog wird **win32 \_ ComputerSystemProduct** verwendet, um eine Liste nicht funktionierender Hardware mithilfe von WMI abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Produkt**](cim-product.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

