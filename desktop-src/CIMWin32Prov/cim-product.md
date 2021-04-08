---
description: Die CIM- \_ Produktklasse ist eine konkrete Klasse, die eine Auflistung physischer Elemente, Software Features und anderer Produkte darstellt, die als Einheit erworben wurden.
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: CIM_Product-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748008"
---
# <a name="cim_product-class"></a>CIM- \_ Produktklasse

Die **CIM- \_ Produkt** Klasse ist eine konkrete Klasse, die eine Auflistung physischer Elemente, Software Features und anderer Produkte darstellt, die als Einheit erworben wurden. Der Erwerb impliziert eine Vereinbarung zwischen dem Lieferanten und dem Consumer, die Auswirkungen auf die Produkt Lizenzierung, den Support und die Gewährleistung haben kann.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Produkt** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Produkt** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung für das Produkt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Textbeschreibung des Produkts.

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")
</dt> </dl>

Produktidentifizierung, z. b. Seriennummer auf Software, eine Nummer auf einem Hardware Chip oder (bei nicht kommerziellen Produkten) eine Projekt Nummer.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,2 ")
</dt> </dl>

Häufig verwendeter Produktname.

</dd> <dt>

**SKUNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

SKU-Informationen (Stock-Keeping Unit) des Produkts.

</dd> <dt>

**Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,1 ")
</dt> </dl>

Der Name des Lieferanten des Produkts oder die Entität, die das Produkt verkauft (Hersteller, Reseller, OEM usw.).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,3 ")
</dt> </dl>

Informationen zur Produktversion.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die vom **CIM- \_ Produkt** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

