---
description: Die Enumeration des Haupttyps der Zeitachse \_ \_ gibt den Haupttyp eines Objekts an.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: TIMELINE_MAJOR_TYPE-Enumeration (qedit. h)
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
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369578"
---
# <a name="timeline_major_type-enumeration"></a>Zeitachsen- \_ \_ Haupttyp-Enumeration

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `TIMELINE_MAJOR_TYPE` Enumeration gibt den Haupttyp eines Objekts an.

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

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**Zeit \_ Achsen \_ Haupttyp \_ Composite**
</dt> <dd>

Zusammengesetztes Objekt. Enthält mindestens einen Titel.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**Zeitachse des \_ \_ Haupttyps \_**
</dt> <dd>

Objekt nachverfolgen. Enthält mindestens eine Quelle.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**Zeitachsen- \_ \_ Haupttyp \_ Quelle**
</dt> <dd>

Quellobjekt. Enthält einen Verweis auf eine Medienquelle.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**Zeit \_ Achsen \_ \_ haupttypübergang**
</dt> <dd>

Übergangs Objekt. Definiert einen Übergang zwischen Verbund, Spuren oder Quellen.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_Haupt \_ \_ Effekte der Zeitachse**
</dt> <dd>

Effect-Objekt. Definiert einen eingabeffekt, der auf ein Composite-, Track-oder Source-Objekt angewendet werden soll.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**Zeitachsen- \_ \_ Haupttyp \_ Gruppe**
</dt> <dd>

Group-Objekt. Enthält mindestens einen Titel eines bestimmten Typs.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimeline**](iamtimeline.md)
</dt> <dt>

[**Iamtimelinecomp:: getzählype**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**Iamtimelineobj:: gettimelinetype**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




