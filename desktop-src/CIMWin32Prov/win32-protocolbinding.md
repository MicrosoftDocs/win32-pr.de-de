---
description: Die \_ WMI-Klasse der Win32 protocolbinding Association bezieht sich auf den Treiber, das Netzwerkprotokoll und den Netzwerkadapter auf Systemebene.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Win32_ProtocolBinding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860692"
---
# <a name="win32_protocolbinding-class"></a>Win32 \_ protocolbinding-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32 \_ protocolbinding** Association bezieht sich auf den Treiber, das Netzwerkprotokoll und den Netzwerkadapter auf Systemebene.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a>Member

Die **Win32- \_ protocolbinding** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ protocolbinding** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ networkprotocol**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ networkprotocol")
</dt> </dl>

Verweis auf die-Instanz, die das Protokoll darstellt, das mit dem System Treiber und dem Netzwerkadapter verwendet wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ System Driver**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ System Driver")
</dt> </dl>

Verweis auf die-Instanz, die den System Treiber darstellt, der den Netzwerkadapter über das Netzwerkprotokoll dieser Klasse verwendet.

</dd> <dt>

**Device**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ NetworkAdapter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Network Adapter")
</dt> </dl>

Eigenschaften des Netzwerkadapters, die auf dem Computersystem verwendet werden.

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

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
