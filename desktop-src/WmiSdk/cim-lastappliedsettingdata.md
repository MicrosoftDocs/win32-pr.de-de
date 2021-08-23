---
description: Eine Zuordnung zwischen einem -Objekt und einem anderen -Objekt, das darauf angewendet wurde.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: CIM_LastAppliedSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 6c1e5174cb9fcaf9279d16eceda547e9e5060c4ca4f7deda09cc170cf3dd7653
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244650"
---
# <a name="cim_lastappliedsettingdata-class"></a>CIM \_ LastAppliedSettingData-Klasse

Eine Zuordnung zwischen einem -Objekt und einem anderen -Objekt, das darauf angewendet wurde.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a>Member

Die **CIM \_ LastAppliedSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LastAppliedSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AppliedObject**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das Objekt, das auf das Zielobjekt angewendet wurde.

</dd> <dt>

**Target**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das Objekt, das das Ziel der Anwendung des Objekts war.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------|
| Namespace<br/> | \\Stamm-CIMV2<br/> |



 

 




