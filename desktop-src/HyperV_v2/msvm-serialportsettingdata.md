---
description: Beschreibt die Einstellungsdaten für einen virtuellen seriellen Anschluss.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Msvm_SerialPortSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865512"
---
# <a name="msvm_serialportsettingdata-class"></a>MSVM \_ serialportsettingdata-Klasse

Beschreibt die Einstellungsdaten für einen virtuellen seriellen Anschluss.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a>Member

Die **MSVM \_ serialportsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ serialportsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Debuggermode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**true** , wenn der Debuggermodus auf einem virtuellen seriellen Anschluss aktiviert ist. andernfalls **false**. Der Debugger-Modus verbessert die Verwendung eines Microsoft Windows-Kernel Debuggers über einen virtuellen seriellen Anschluss.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




