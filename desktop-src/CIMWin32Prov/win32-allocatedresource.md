---
description: Die \_ WMI-Klasse für die Zuordnung der Win32-Zuordnungs Klasse ordnet ein logisches Gerät mit einer System Ressource in Beziehung. Diese Klasse wird verwendet, um zu ermitteln, welche Ressourcen, wie z. b. die unqs-oder DMA-Kanäle, von einem bestimmten Gerät verwendet werden.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Win32_AllocatedResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958547"
---
# <a name="win32_allocatedresource-class"></a>Win32- \_ Klasse "Zuweisung"

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für die **Zuordnung der Win32- \_ Zuordnungs Klasse ordnet** ein logisches Gerät mit einer System Ressource in Beziehung. Diese Klasse wird verwendet, um zu ermitteln, welche Ressourcen, wie z. b. die unqs-oder DMA-Kanäle, von einem bestimmten Gerät verwendet werden.

Diese Klasse ist veraltet. Anstelle dieser Klasse sollten Sie die Eigenschaften in der [**Win32- \_ pnpallocatedresource**](win32-pnpallocatedresource.md) -Klasse verwenden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>Member

Die **Win32 \_** -Klasse "-Klasse" weist die folgenden Typen von Membern auf:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_** -Klasse "-Klasse" weist diese Eigenschaften auf.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Systemresource**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ Systemresource")
</dt> </dl>

Eine [**CIM- \_ System Ressource**](cim-systemresource.md) , die die Eigenschaften einer für das logische Gerät verfügbaren System Ressource beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, von dem die ihm zugewiesenen Systemressourcen verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_** -Klasse "-Klasse" ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

