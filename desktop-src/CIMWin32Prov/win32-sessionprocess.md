---
description: Die \_ WMI-Klasse Win32 sessionprocess Association stellt eine Zuordnung zwischen einer Anmelde Sitzung und den Prozessen dar, die dieser Sitzung zugeordnet sind.
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
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343579"
---
# <a name="win32_sessionprocess-class"></a>Win32- \_ sessionprocess-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ sessionprocess** Association stellt eine Zuordnung zwischen einer Anmelde Sitzung und den Prozessen dar, die dieser Sitzung zugeordnet sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die Win32-Klasse " **\_ sessionprocess** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ sessionprocess** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ logonsession**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Vorgänger"), [**Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Eine [**Win32 \_**](win32-logonsessionmappeddisk.md) -Anmelde Sitzung, die die Sitzung darstellt, die mit dem Prozess verknüpft ist.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Prozess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("abhängig"), [**Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

Ein [**Win32- \_ Prozess**](win32-processor.md) , der den Prozess darstellt, der der Sitzung zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Win32 \_ Sessionprocess** gibt alle Sitzungen für den Administrator zurück, wenn er bei einer erhöhten Rechte oder einer Remote-Remote Anmeldung angemeldet ist Dies ist eine Erweiterung des Verhaltens der-Klasse.

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

[**Win32- \_ sessionresource**](win32-sessionresource.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
