---
description: Eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme, die dem virtuellen System übergeordnet ist.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 85f08f22409df8a17bdae33ae81c06cb8167996ecb477f6a2d207d9e0ce2acca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131762"
---
# <a name="cim_previoussettingdata-class"></a>CIM \_ PreviousSettingData-Klasse

Eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme, die dem virtuellen System übergeordnet ist.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>Member

Die **CIM \_ PreviousSettingData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ PreviousSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**PreviousObject**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Die Momentaufnahmeeinstellungsdaten, die das übergeordnete Element dieses Computersystems sind.

</dd> <dt>

**Target**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das Computersystem, das das Ziel der Anwendung war.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------|
| Namespace<br/> | \\Stamm-CIMV2<br/> |



 

 




