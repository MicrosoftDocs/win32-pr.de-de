---
description: Stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das Feld "DeviceID" (Schlüssel) "Disks" identifiziert werden.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: CIM_LogicalDisk-Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960277"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a>CIM_LogicalDisk-Klasse (Hyper-V-Verwaltung)

Stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das **DeviceID** (Key)-Feld des Datenträgers identifiziert werden. Beispielsweise enthält das Feld " **DeviceID** " in einer Windows-Umgebung einen Laufwerk Buchstaben. in einer UNIX-Umgebung enthält Sie den Zugriffs Pfad. und in einer NetWare-Umgebung enthält Sie den Volumenamen.

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

Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Gibt an, ob das logische Gerät das Namensformat des Betriebssystems verwendet.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Betriebssystem-Geräte Name** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**Namenamespace**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("namenamespace")
</dt> </dl>

Gibt an, ob das logische Gerät denselben Namespace aufweist wie das Betriebssystem.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Betriebssystem-Geräte Namespace** (8)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ storageblock**](cim-storageextent.md)
</dt> </dl>

 

