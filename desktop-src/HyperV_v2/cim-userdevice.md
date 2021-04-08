---
description: Stellt ein logisches Gerät dar, das es einem Benutzer ermöglicht, Daten auf dem Computersystem einzugeben, anzuzeigen oder zu hören.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: CIM_UserDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864111"
---
# <a name="cim_userdevice-class-hyper-v-management"></a>CIM_UserDevice-Klasse (Hyper-V-Verwaltung)

Stellt ein logisches Gerät dar, das es einem Benutzer ermöglicht, Daten auf dem Computersystem einzugeben, anzuzeigen oder zu hören.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a>Member

Die **CIM \_ userdevice** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ userdevice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**IsLocked**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn das Gerät gesperrt ist und Benutzereingaben oder-Ausgaben verhindert. andernfalls **false**.

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




