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
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="b556c-103">Zeitachsen- \_ \_ Haupttyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b556c-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="b556c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b556c-104">\[Deprecated.</span></span> <span data-ttu-id="b556c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b556c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b556c-106">Die- `TIMELINE_MAJOR_TYPE` Enumeration gibt den Haupttyp eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b556c-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b556c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b556c-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="b556c-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b556c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b556c-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**Zeit \_ Achsen \_ Haupttyp \_ Composite**</span><span class="sxs-lookup"><span data-stu-id="b556c-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="b556c-110">Zusammengesetztes Objekt.</span><span class="sxs-lookup"><span data-stu-id="b556c-110">Composite object.</span></span> <span data-ttu-id="b556c-111">Enthält mindestens einen Titel.</span><span class="sxs-lookup"><span data-stu-id="b556c-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="b556c-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**Zeitachse des \_ \_ Haupttyps \_**</span><span class="sxs-lookup"><span data-stu-id="b556c-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="b556c-113">Objekt nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="b556c-113">Track object.</span></span> <span data-ttu-id="b556c-114">Enthält mindestens eine Quelle.</span><span class="sxs-lookup"><span data-stu-id="b556c-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="b556c-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**Zeitachsen- \_ \_ Haupttyp \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="b556c-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="b556c-116">Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="b556c-116">Source object.</span></span> <span data-ttu-id="b556c-117">Enthält einen Verweis auf eine Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="b556c-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="b556c-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**Zeit \_ Achsen \_ \_ haupttypübergang**</span><span class="sxs-lookup"><span data-stu-id="b556c-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="b556c-119">Übergangs Objekt.</span><span class="sxs-lookup"><span data-stu-id="b556c-119">Transition object.</span></span> <span data-ttu-id="b556c-120">Definiert einen Übergang zwischen Verbund, Spuren oder Quellen.</span><span class="sxs-lookup"><span data-stu-id="b556c-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="b556c-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_Haupt \_ \_ Effekte der Zeitachse**</span><span class="sxs-lookup"><span data-stu-id="b556c-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="b556c-122">Effect-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b556c-122">Effect object.</span></span> <span data-ttu-id="b556c-123">Definiert einen eingabeffekt, der auf ein Composite-, Track-oder Source-Objekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b556c-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="b556c-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**Zeitachsen- \_ \_ Haupttyp \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="b556c-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="b556c-125">Group-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b556c-125">Group object.</span></span> <span data-ttu-id="b556c-126">Enthält mindestens einen Titel eines bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="b556c-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b556c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b556c-127">Requirements</span></span>



| <span data-ttu-id="b556c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b556c-128">Requirement</span></span> | <span data-ttu-id="b556c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b556c-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b556c-130">Header</span><span class="sxs-lookup"><span data-stu-id="b556c-130">Header</span></span><br/> | <dl> <span data-ttu-id="b556c-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b556c-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b556c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b556c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b556c-133">**Iamtimeline**</span><span class="sxs-lookup"><span data-stu-id="b556c-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="b556c-134">**Iamtimelinecomp:: getzählype**</span><span class="sxs-lookup"><span data-stu-id="b556c-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="b556c-135">**Iamtimelineobj:: gettimelinetype**</span><span class="sxs-lookup"><span data-stu-id="b556c-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




