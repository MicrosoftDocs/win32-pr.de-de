---
description: Eine Beziehung, die angibt, dass zwei oder mehr Geräte miteinander verbunden sind.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: CIM_DeviceConnection-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81ec2826339e27d956750360b280fcafd7b55e6264a6bcab83ebc1cb41a1ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812844"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a>CIM_DeviceConnection-Klasse (Hyper-V-Verwaltung)

Eine Beziehung, die angibt, dass zwei oder mehr Geräte miteinander verbunden sind.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a>Member

Die **CIM \_ DeviceConnection-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ DeviceConnection-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein Gerät

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein zweites Gerät, das mit dem anderen Gerät verbunden ist.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Bus Port Association \| 001.3"), **PUnit** ("bit")
</dt> </dl>

Wenn mehrere Bus- und Verbindungsdatenbreiten möglich sind, definiert die Eigenschaft NegotiatedDataWidth die Zwischenspeicherung zwischen den Geräten. Die Datenbreite wird in Bits angegeben. Wenn die Datenbreite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder nicht wichtig sind, sollte die -Eigenschaft auf 0 festgelegt werden.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Bus Port Association \| 001.2"), **PUnit** ("bit/second")
</dt> </dl>

Wenn mehrere Bus- und Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die Geschwindigkeit, die zwischen den Geräten in Bits pro Sekunde verwendet wird. Wenn keine Verbindungs- oder Busgeschwindigkeiten ausgehandelt werden oder diese Informationen nicht verfügbar oder für die Geräteverwaltung nicht wichtig sind, sollte die -Eigenschaft auf "0" festgelegt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

