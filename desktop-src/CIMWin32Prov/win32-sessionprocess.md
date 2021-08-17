---
description: Die WMI-Klasse für die Win32 SessionProcess-Zuordnung stellt eine Zuordnung zwischen einer Anmeldesitzung und den prozessen \_ dar, die dieser Sitzung zugeordnet sind.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f31473cf1efa0310669523f0481b58d8b54036f738a69191f19a0a52d804eb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416815"
---
# <a name="win32_sessionprocess-class"></a>Win32 \_ SessionProcess-Klasse

Die **WMI-Klasse \_ für die Win32 SessionProcess-Zuordnung** stellt eine Zuordnung zwischen einer Anmeldesitzung und den prozessen dar, die dieser Sitzung zugeordnet sind. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SessionProcess-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionProcess-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ LogonSession**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Eine [**Win32 \_ LogonSession,**](win32-logonsessionmappeddisk.md) die die Sitzung darstellt, die mit dem Prozess verknüpft ist.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ Win32-Prozess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Abhängig"), [**Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Ein [**\_ Win32-Prozess,**](win32-processor.md) der den prozess darstellt, der der Sitzung zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Win32 \_ SessionProcess** gibt alle Sitzungen für den Administrator zurück, wenn er mit erhöhten Rechten angemeldet ist oder remote ausgeführt wird. Dies ist eine Erweiterung des Verhaltens der -Klasse.

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

[**Win32 \_ SessionResource**](win32-sessionresource.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
