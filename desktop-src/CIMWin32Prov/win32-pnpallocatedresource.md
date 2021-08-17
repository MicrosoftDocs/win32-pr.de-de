---
description: Die \_ WMI-Zuordnungsklasse Win32 PnPAllocatedResource stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 492bd510965499393b399e8e02c1b901fc33f9abc00acf191899c5bb6b8b6d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118008944"
---
# <a name="win32_pnpallocatedresource-class"></a>Win32 \_ PnPAllocatedResource-Klasse

Die [WMI-Zuordnungsklasse](../wmisdk/retrieving-a-class.md) **Win32 \_ PnPAllocatedResource** stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar. Diese Klasse wird verwendet, um die Ressourcen zu ermitteln, die von einem bestimmten Gerät verwendet werden, z. B. eine Interruptrequest (IRQ) oder ein DMA-Kanal (Direct Memory Access).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ PnPAllocatedResource-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PnPAllocatedResource-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SystemResource**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](../wmisdk/key-qualifier.md) [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")
</dt> </dl>

Verweis auf die [**\_ CIM-SystemResource-Instanz,**](cim-systemresource.md) die die Eigenschaften einer Systemressource darstellt, die für das logische Gerät verfügbar ist. Diese Eigenschaft wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PnPEntity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Verweis auf die [**Win32-PnPEntity-Instanz, \_**](win32-pnpentity.md) die die Eigenschaften des logischen Geräts mithilfe der ihm zugewiesenen Systemressourcen darstellt. Diese Eigenschaft wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PnPAllocatedResource-Klasse** wird von [**CIM \_ AllocatedResource**](cim-allocatedresource.md)abgeleitet.

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

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
