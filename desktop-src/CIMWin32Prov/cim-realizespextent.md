---
description: Die CIM- \_ Erweiterung "realizespblock" stellt die Beziehung dar, in der physische Blöcke auf einem physischen Medium realisiert werden. Außerdem wird die Startadresse des physischen Wertebereichs auf dem physischen Medium angegeben.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: CIM_RealizesPExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346223"
---
# <a name="cim_realizespextent-class"></a>CIM \_ realizespblock-Klasse

Die CIM-Erweiterung " **\_ realizespblock** " stellt die Beziehung dar, in der physische Blöcke auf einem physischen Medium realisiert werden. Außerdem wird die Startadresse des physischen Wertebereichs auf dem physischen Medium angegeben.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a>Member

Die CIM-Klasse " **\_ realizespblock** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ realizespblock** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ physicalmedia**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM- \_ physicalmedia**](cim-physicalmedia.md) , das das physische Medium beschreibt, auf dem der Block realisiert wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ physicalblock**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM- \_ physicalblock**](cim-physicalextent.md) , der den physischen Block beschreibt, der sich auf dem Medium befindet.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Startadresse auf dem physischen Medium, an dem der physische Block beginnt. Die Endadresse des physischen Wertebereichs wird mithilfe der Eigenschaften " **zahlofblocks** " und " **BLOCKSIZE** " des [**CIM- \_ physicalblock**](cim-physicalextent.md) -Objekts bestimmt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die CIM-Klasse " **\_ realizespblock** " ist von CIM-Erkenntnissen abgeleitet. [**\_**](cim-realizes.md)

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ erkennt**](cim-realizes.md)
</dt> </dl>

 

