---
description: Gibt eine MCA-, korrigierte Computer Überprüfung (CMC) oder einen korrigierten Platt Formfehler (CPE)-Informations Eintrag an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
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
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360760"
---
# <a name="msmcainfo_entry-class"></a>Msmcainfo- \_ Einstiegsklasse

Die **msmcainfo- \_ Einstiegs** Klasse zeigt eine MCA-, korrigierte Computer Überprüfung (SMTP) oder einen korrigierten Platt Formfehler (CPE)-Informations Eintrag an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Member

Die **msmcainfo- \_ Einstiegs** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcainfo- \_ Einstiegs** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Daten**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein ganzzahliges Array, das einen von der System Abstraktionsschicht (SAL) gemeldeten kompletten MCA-Fehler Daten Satz enthält. Der SAL wird in Rom verbrannt, den das Betriebssystem zum Ausführen von Platt Form abhängigen Vorgängen aufruft. Sie ähnelt dem BIOS auf einer x86-Plattform.

</dd> <dt>

**Länge**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Bytes im Fehler Daten Satz.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcainfo- \_ Einstiegs** Klasse wird von [**msmcainfo**](msmcainfo.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**Msmcainfo**](msmcainfo.md)
</dt> </dl>

 

 




