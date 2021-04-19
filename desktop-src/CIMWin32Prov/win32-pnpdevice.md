---
description: Die \_ WMI-Klasse für die Win32-pnpdevice-Zuordnung verknüpft ein Gerät (bekannt als pntztity) und die Funktion Configuration Manager, die es ausführt.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346458"
---
# <a name="win32_pnpdevice-class"></a>Win32- \_ pnpdevice-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32- \_ pnpdevice** -Zuordnung verknüpft ein Gerät (bekannt als pntztity) und die Funktion Configuration Manager, die es ausführt. Die Funktion wird durch eine Unterklasse des logischen Geräts dargestellt, das deren Verwendung beschreibt. Beispielsweise eine [**Win32- \_ Tastatur**](win32-keyboard.md) oder eine [**Win32 \_ diskdrive**](win32-diskdrive.md) -Instanz. Beide referenzierten Objekte stellen dasselbe zugrunde liegende System Gerät dar. Änderungen an der Ressourcen Zuordnung auf der pnptity-Seite wirken sich auf das zugehörige Gerät aus.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Member

Die **Win32- \_ pnpdevice** -Klasse verfügt über diese Typen von mempdevice:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ pnpdevice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Verweis auf die [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanz, die die Eigenschaften des logischen Geräts darstellt, die dem Plug & Play-Gerät zugeordnet sind.

</dd> <dt>

**Systemelement**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ pnptity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ pnptity")
</dt> </dl>

Verweis auf die [**Win32- \_ pnptity**](win32-pnpentity.md) -Instanz, die das Plug & Play Gerät darstellt, das dem logischen Gerät zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
