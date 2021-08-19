---
description: Gibt die Unformatiert-MCA-Protokolle (Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: MSMCAInfo_RawMCAData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 2b7ac9f8c474a1aee55d0dd70a5a838102aec66bc8b3ba3d867070430c38a3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821864"
---
# <a name="msmcainfo_rawmcadata-class"></a>MSMCAInfo \_ RawMCAData-Klasse

**MsmcaInfo \_ RawMCAData gibt** die Unformatiert-MCA-Protokolle (Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Member

Die **MSMCAInfo \_ RawMCAData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ RAWMCAData-Klasse von MSMCAInfo** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

TRUE, wenn diese Instanz der -Klasse aktiv ist; andernfalls **FALSE**.

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Fehlerdatensätze.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eindeutiger Bezeichner dieser Instanz der -Klasse.

</dd> <dt>

**Datensätze**
</dt> <dd> <dl> <dt>

Datentyp: **\_ MSMCAInfo-Eintragsarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von MCA-Fehlerdatensätzen. Die Anzahl der MCA-Fehlerdatensätze im Array wird von der **Count-Eigenschaft** angegeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAInfo \_ RawMCAData-Klasse** wird von [**MSMCAInfo abgeleitet.**](msmcainfo.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

