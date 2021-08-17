---
description: Stellt einen zusammenhängenden Bereich logischer Blöcke dar, der von einem Dateisystem über das Feld DeviceID (Schlüssel) der Datenträger identifiziert werden kann.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: CIM_LogicalDisk -Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0fccc6600e0eb5f04fd7d00360402ad85a94746e55781acbd6b1a35c7f9b94fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812105"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a>CIM_LogicalDisk -Klasse (Hyper-V-Verwaltung)

Stellt einen zusammenhängenden Bereich logischer Blöcke dar, der von einem Dateisystem über das **Feld DeviceID** (Schlüssel) des Datenträgers identifiziert werden kann. Beispielsweise enthält das Feld **DeviceID** in Windows-Umgebung einen Laufwerkbuchstaben. in einer UNIX-Umgebung enthält sie den Zugriffspfad. und in einer NetWare-Umgebung enthält sie den Volumenamen.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a>Member

Die **KLASSE CIM \_ LogicalDisk** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **KLASSE CIM \_ LogicalDisk** verfügt über diese Eigenschaften.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Gibt an, ob das logische Gerät das Namensformat des Betriebssystems verwendet.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Name des Betriebssystemgeräts** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")
</dt> </dl>

Gibt an, ob das logische Gerät über denselben Namespace wie das Betriebssystem verfügt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Namespace des Betriebssystemgeräts** (8)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> </dl>

 

