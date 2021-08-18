---
description: Stellt eine Zuordnung dar, bei der ein CIM \_ ServiceAccessPoint- oder CIM \_ ProtocolEndpoint-Objekt von einem zugrunde liegenden CIM \_ LANEndpoint-Objekt auf demselben System abhängt.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: CIM_BindsToLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 53418dd9f2e259ac2b5f109dac4c783682657a7a9c5ac5e0548e23cbe0fd6be1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765610"
---
# <a name="cim_bindstolanendpoint-class"></a>CIM \_ BindsToLANEndpoint-Klasse

Stellt eine Zuordnung dar, bei der ein [**CIM \_ ServiceAccessPoint-**](cim-serviceaccesspoint.md) oder [**CIM \_ ProtocolEndpoint-Objekt**](cim-protocolendpoint.md) von einem zugrunde liegenden [**CIM \_ LANEndpoint-Objekt**](cim-lanendpoint.md) auf demselben System abhängt.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a>Member

Die **CIM \_ BindsToLANEndpoint-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BindsToLANEndpoint-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LANEndpoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Das zugrunde liegende [**CIM \_ LANEndpoint-Objekt.**](cim-lanendpoint.md)

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Das [**CIM \_ ServiceAccessPoint-**](cim-serviceaccesspoint.md) oder [**CIM \_ ProtocolEndpoint-Objekt,**](cim-protocolendpoint.md) das vom [**CIM \_ LANEndpoint**](cim-lanendpoint.md)abhängig ist.

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Rahmenmethode für den Dienstzugriffspunkt oder Protokollendpunkt der oberen Ebene.

> [!Note]  
> Raw802.3 wird nur mit dem IPX-Protokoll verwendet.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="802.2"></span>

**802.2** (2)


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

**SNAP** (3)


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

**Raw802.3** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ BindsTo**](cim-bindsto.md)
</dt> </dl>

 

