---
description: Verbindet einen Switchport mit einem dynamischen Vorwärtseintrag (erlernte MAC-Adresse).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d5deb326877e7af639c7bc18a73a8c968e75c26b64d690d4a4582085833fa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950069"
---
# <a name="msvm_switchportdynamicforwarding-class"></a>Msvm \_ SwitchPortDynamicForwarding-Klasse

Verbindet einen Switchport mit einem dynamischen Vorwärtseintrag (erlernte MAC-Adresse). Dies ist nützlich, um alle erlernten MAC-Adressen für einen angegebenen Port zu finden.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SwitchPortDynamicForwarding-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SwitchPortDynamicForwarding-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ EthernetSwitchPort-Klasse,**](msvm-ethernetswitchport.md) die den Switchport darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ DynamicForwardingEntry-Klasse,**](msvm-dynamicforwardingentry.md) die den dynamischen Weiterleitungseintrag der Weiterleitungsdatenbank darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ SwitchPortDynamicForwarding-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter [Abfragen von Netzwerkobjekten.](querying-networking-objects.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](cim-switchportdynamicforwarding.md)
</dt> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))
</dt> </dl>

 

