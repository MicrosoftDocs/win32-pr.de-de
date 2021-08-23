---
description: Gibt einen MCA-, korrigierten Computerüberprüfungs- (CMC) oder korrigierten CpE-Informationseintrag (Platform Error) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8f6146d629678c1ee209738095fea901f0edb865bccb9aff2d4eeab02d18e773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640902"
---
# <a name="msmcainfo_entry-class"></a>MSMCAInfo \_ Entry-Klasse

Die **MSMCAInfo \_ Entry-Klasse** gibt einen MCA-, korrigierten Computerüberprüfungs- (CMC) oder korrigierten CPE-Informationseintrag (Platform Error) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Member

Die **MSMCAInfo \_ Entry-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAInfo \_ Entry-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Daten**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ganzzahliges Array, das einen vollständigen MCA-Fehlerdatensatz enthält, wie von der Systemabstraktionsschicht (SAL) gemeldet. Die SAL wird in ein ROM-Laufwerk verbraucht, das das Betriebssystem aufruft, um plattformabhängige Vorgänge auszuführen. Es ähnelt dem BIOS auf einer x86-Plattform.

</dd> <dt>

**Länge**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Bytes im Fehlerdatensatz.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAInfo \_ Entry-Klasse** wird von [**MSMCAInfo**](msmcainfo.md)abgeleitet.

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

 

 




