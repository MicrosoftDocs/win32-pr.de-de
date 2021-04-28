---
description: 'Msvm_DeviceSAPImplementation-Klasse: Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung.'
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112098"
---
# <a name="msvm_devicesapimplementation-class"></a>Msvm \_ DeviceSAPImplementation-Klasse

Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung. Die Kardinalität dieser Zuordnung ist m:n. Ein SAP kann von mehreren logischen Geräten bereitgestellt werden, die in Verbindung stehen. Jedes Gerät kann mehrere SAP-Geräte bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen. Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen. Diese einzelnen Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ DeviceSAPImplementation-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ DeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das logische Gerät. Diese Eigenschaft wird von [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Mithilfe des logischen Geräts implementierte Dienstzugriffspunkt. Diese Eigenschaft wird von [**CIM \_ DeviceSAPImplementation geerbt.**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **Msvm \_ DeviceSAPImplementation-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Weitere Informationen [finden Sie unter Abfragen von Netzwerkobjekten.](querying-networking-objects.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2012-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dt>

[**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

