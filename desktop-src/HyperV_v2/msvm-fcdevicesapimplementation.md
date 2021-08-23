---
description: 'Msvm_FcDeviceSAPImplementation Klasse: Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert.'
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9aafe3bd029960a0b371c3a3d5ab54b66ad4849210189ab2946df2854656c500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523460"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>Msvm \_ FcDeviceSAPImplementation-Klasse

Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert. Die Kardinalität dieser Zuordnung ist n:n. Ein Dienstzugriffspunkt (SAP) kann von mehr als einem logischen Gerät bereitgestellt werden, das in Verbindung ausgeführt wird. Jedes Gerät kann mehrere SAP-Daten bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen zum Bereitstellen des Zugriffspunkts verwendet werden. Wenn verschiedene Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen. Diese einzelnen Instanziierungen würden dann Zuordnungen zu den eindeutigen Implementierungen haben.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ FcDeviceSAPImplementation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ FcDeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ FCPort**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein Verweis auf eine von **CIM \_ FCPort** abgeleitete Klasse, die das logische Gerät darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ FcEndpoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ FcEndpoint-Klasse,**](msvm-fcendpoint.md) die den SAP darstellt, der die **-Instanz verwendet.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

