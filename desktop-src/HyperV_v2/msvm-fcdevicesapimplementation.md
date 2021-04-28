---
description: 'Msvm_FcDeviceSAPImplementation-Klasse: Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert.'
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
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119028"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>Msvm \_ FcDeviceSAPImplementation-Klasse

Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert. Die Kardinalität dieser Zuordnung ist m:n. Ein Dienstzugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die in Verbindung stehen. Jedes Gerät kann mehrere SAP-Geräte bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen. Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen. Diese einzelnen Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ FcDeviceSAPImplementation-Klasse** verfügt über diese Typen von Membern:

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

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
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



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2012-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

