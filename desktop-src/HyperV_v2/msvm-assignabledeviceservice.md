---
description: Verwaltet die zustellbaren Geräte auf einem Host Computersystem.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Msvm_AssignableDeviceService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369100"
---
# <a name="msvm_assignabledeviceservice-class"></a>MSVM-Klasse ' zuder \_ Zustell barkeit '

Verwaltet die zustellbaren Geräte auf einem Host Computersystem.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **MSVM \_** -Klasse "zuder Klasse" weist die folgenden Member auf:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM-Klasse " \_ accessabledeviceservice** " verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Dismountassignabledevice**](msvm-assignabledeviceservice-dismountassignabledevice.md) | Hebt die Einbindung des angegebenen PCI-Geräts auf, sodass es zugewiesen werden kann.<br/>                      |
| [**Mountassignabledevice**](msvm-assignabledeviceservice-mountassignabledevice.md)       | Stellt das angegebene PCI-Gerät bereit, sodass es vom Host Computersystem verwendet werden kann.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




