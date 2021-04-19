---
description: Eine Zuordnung zwischen einer Instanz von CIM \_ virtualsystemsettingdata und der CIM \_ virtualsystemsettingdata-Instanz, die die aktuelle Momentaufnahme darstellt, auf der dieses Objekt basiert.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: CIM_ParentChildSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359628"
---
# <a name="cim_parentchildsettingdata-class"></a>CIM- \_ parametrientchildsettingdata-Klasse

Eine Zuordnung zwischen einer Instanz von [**CIM \_ virtualsystemsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) und der **CIM \_ virtualsystemsettingdata** -Instanz, die die aktuelle Momentaufnahme darstellt, auf der dieses Objekt basiert.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a>Member

Die CIM-Klasse " **\_ Parser-childsettingdata** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ Parser-childsettingdata** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das unabhängige Objekt in dieser Zuordnung.

Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Untergeordnet**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ virtualsystemsettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Einstellungsdaten für das virtuelle System, das das untergeordnete Element des übergeordneten Elements darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Objekt, das von der **Vorgänger** Eigenschaft abhängt.

Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ virtualsystemsettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Momentaufnahme Einstellungsdaten, auf denen die Daten der untergeordneten Einstellung basieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------|
| Namespace<br/> | Root \\ CIMV2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

