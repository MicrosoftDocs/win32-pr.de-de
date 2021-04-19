---
description: Eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme, die das übergeordnete Element des virtuellen Systems ist.
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
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360387"
---
# <a name="cim_previoussettingdata-class"></a>CIM \_ previoussettingdata-Klasse

Eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme, die das übergeordnete Element des virtuellen Systems ist.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

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

Die **CIM \_ previoussettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ previoussettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Previousobject**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Die Daten der Momentaufnahme Einstellung, die diesem Computersystem übergeordnet sind.

</dd> <dt>

**Target**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das Computersystem, das Ziel der Anwendung ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------|
| Namespace<br/> | Root \\ CIMV2<br/> |



 

 




