---
description: Die CIM \_ chassisinrack-Zuordnung stellt die &\# 0034 dar, die&\# 0034;-Beziehung zwischen einem Gestell und einem darin enthaltenen Chassis enthält.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: CIM_ChassisInRack-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127113"
---
# <a name="cim_chassisinrack-class"></a>CIM \_ chassisinrack-Klasse

Die **CIM \_ chassisinrack** -Zuordnung stellt die "enthaltende" Beziehung zwischen einem Gestell und einem darin enthaltenen Chassis dar.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a>Member

Die **CIM \_ chassisinrack** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ chassisinrack** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Bottomu**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")
</dt> </dl>

Eine ganze Zahl, die das niedrigste oder untere "U" angibt, in dem das Chassis eingebunden ist. Ein "U" ist eine Standard Maßeinheit für die Höhe eines Rasters oder einer Regal baren Komponente und ist gleich 1,75 Zoll oder 4,445 Zentimeter.

</dd> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Rack**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM- \_ Rack**](cim-rack.md) , das das Gestell beschreibt, das das Chassis enthält.

</dd> <dt>

**Locationwithincontainer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt. Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden. Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.

Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Chassis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**CIM- \_ Chassis**](cim-chassis.md) , das das Chassis beschreibt, das in das Gestell eingebunden ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ chassisinrack** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.

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

[**CIM- \_ Container**](cim-container.md)
</dt> </dl>

 

