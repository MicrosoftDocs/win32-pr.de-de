---
description: Stellt eine Gruppe von Controllern dar, die den Betrieb und die Funktion von Geräten steuern, die Protokolle initiieren.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: CIM_ProtocolController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7dcd0f0ca1891914e2c4fc3fedbc0012d930dbaec99926f9db8e013435367f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148510"
---
# <a name="cim_protocolcontroller-class"></a>CIM \_ ProtocolController-Klasse

Stellt eine Gruppe von Controllern dar, die den Betrieb und die Funktion von Geräten steuern, die Protokolle initiieren.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a>Member

Die **CIM \_ ProtocolController-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ProtocolController-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**MaxUnitsControlled**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Einheiten, die über den Protokollcontroller gesteuert oder darauf zugegriffen werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




