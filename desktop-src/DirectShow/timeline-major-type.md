---
description: Die TIMELINE \_ MAJOR \_ TYPE-Enumeration gibt den Haupttyp eines Objekts an.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: TIMELINE_MAJOR_TYPE -Enumeration (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: b18088a9d01b263c80a4ff941a6b7720043da708eaeaebf4f79a2084d1ed258f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501720"
---
# <a name="timeline_major_type-enumeration"></a>TIMELINE \_ MAJOR \_ TYPE-Enumeration

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `TIMELINE_MAJOR_TYPE` -Enumeration gibt den Haupttyp eines Objekts an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**ZUSAMMENGESETZTER \_ \_ ZEITACHSEN-HAUPTTYP \_**
</dt> <dd>

Zusammengesetztes Objekt. Enthält eine oder mehrere Spuren.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**ZEITACHSE \_ \_ HAUPTTYP \_ TRACK**
</dt> <dd>

Track-Objekt. Enthält eine oder mehrere Quellen.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**QUELLE DES \_ \_ ZEITACHSEN-HAUPTTYPS \_**
</dt> <dd>

Quellobjekt. Enthält einen Verweis auf eine Medienquelle.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**ÜBERGANG DES \_ \_ ZEITACHSEN-HAUPTTYPS \_**
</dt> <dd>

Übergangsobjekt. Definiert einen Übergang zwischen Zusammengesetzten, Spuren oder Quellen.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**AUSWIRKUNG DES \_ \_ ZEITACHSEN-HAUPTTYPS \_**
</dt> <dd>

Effect-Objekt. Definiert einen Einzeleingabeeffekt, der auf ein zusammengesetztes, nachverfolgte oder Quellobjekt angewendet werden soll.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_ \_ ZEITACHSEN-HAUPTTYPGRUPPE \_**
</dt> <dd>

Gruppenobjekt. Enthält eine oder mehrere Spuren eines bestimmten Typs.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




