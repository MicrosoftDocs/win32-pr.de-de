---
description: Diese Zuordnung richtet einen Dienstzugriffspunkt (SERVICE Access Point, SAP) als Anfordernde von Protokolldiensten von einem Protokollendpunkt aus ein.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dc8d88475b23d8d7ac12ec36eba96376cf19b7d4d3168556519597d445c73d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870405"
---
# <a name="msvm_bindstolanendpoint-class"></a>Msvm \_ BindsToLANEndpoint-Klasse

Diese Zuordnung richtet einen Dienstzugriffspunkt (SERVICE Access Point, SAP) als Anfordernde von Protokolldiensten von einem Protokollendpunkt aus ein. In der Regel wird diese Zuordnung zwischen SAPs und Endpunkten auf einem einzelnen System ausgeführt. Da es sich bei einem Protokollendpunkt um eine Art VON SAP handelt, kann diese Bindung verwendet werden, um eine Schicht aus zwei Protokollen zu erstellen, bei der die obere Ebene durch die **abhängige** und die untere Ebene durch den Vordenten dargestellt **wird.**

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ BindsToLANEndpoint-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ BindsToLANEndpoint-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein Verweis auf eine [**Msvm \_ LANEndpoint-Klasse,**](msvm-lanendpoint.md) die den Switchport darstellt. Diese Eigenschaft wird von der [**CIM-Abhängigkeit \_ geerbt.**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein Verweis auf den [**Msvm \_ VLANEndpoint,**](msvm-vlanendpoint.md) der dem Switchport zugeordnet ist. Diese Eigenschaft wird von der [**CIM-Abhängigkeit \_ geerbt.**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Rahmenmethode für den SAP- oder Endpunkt der oberen Ebene, der an den LAN-Endpunkt gebunden ist. Diese Eigenschaft wird von **CIM \_ BindsToLANEndpoint geerbt** und immer auf **NULL festgelegt.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

