---
description: Die \_ WMI-Klasse für die Win32-pnpallocatedresource-Zuordnung stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.
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
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861711"
---
# <a name="win32_pnpallocatedresource-class"></a>Win32- \_ pnpallocatedresource-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32- \_ pnpallocatedresource** -Zuordnung stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar. Diese Klasse wird verwendet, um die Ressourcen zu ermitteln, die von einem bestimmten Gerät verwendet werden, z. b. eine Interruptanforderung (UNQ) oder einen DMA-Kanal (Direct Memory Access).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32- \_ pnpallocatedresource** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ pnpallocatedresource** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Systemresource**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ Systemresource")
</dt> </dl>

Verweis auf die [**CIM- \_ systemressourceninstanz**](cim-systemresource.md) , die die Eigenschaften einer für das logische Gerät verfügbaren System Ressource darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ pnptity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Verweis auf die [**Win32 \_ pnptity**](win32-pnpentity.md) -Instanz, die die Eigenschaften des logischen Geräts mit den zugewiesenen Systemressourcen darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ pnpallocatedresource** -Klasse wird von CIM "" [**\_ zugeordnet**](cim-allocatedresource.md).

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

[**CIM- \_ Verteilungs Quelle**](cim-allocatedresource.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
