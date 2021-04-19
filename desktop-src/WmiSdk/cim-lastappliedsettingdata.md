---
description: Eine Zuordnung zwischen einem Objekt und einem anderen Objekt, das darauf angewendet wurde.
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
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373605"
---
# <a name="cim_lastappliedsettingdata-class"></a>CIM \_ lastappliedsettingdata-Klasse

Eine Zuordnung zwischen einem Objekt und einem anderen Objekt, das darauf angewendet wurde.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

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

Die **CIM- \_ lastappliedsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ lastappliedsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Appliedobject**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das-Objekt, das auf das Zielobjekt angewendet wurde.

</dd> <dt>

**Target**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
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
| Namespace<br/> | Root \\ CIMV2<br/> |



 

 




