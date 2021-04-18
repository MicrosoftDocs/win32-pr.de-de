---
description: Hier wird beschrieben, wie das Betriebssystem auf einem Gerät auf dem neuesten Stand ist.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Updateassessment mentstatus-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347224"
---
# <a name="updateassessmentstatus-enumeration"></a>Updateassessment mentstatus-Enumeration

Hier wird beschrieben, wie das Betriebssystem auf einem Gerät auf dem neuesten Stand ist. **Updategutamentstatus** wird von den-Strukturen " [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) " und " [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) " in den Elementen " **Assessment mentforcurrent**", " **bewermentforuptodate**" und " **SecurityStatus** " verwendet. Es wird genau eine Konstante zurückgegeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**Updategutamentstatus \_ Neueste** Version
</dt> <dd>

Dieses Ergebnis in " **bewermentforcurrent** " impliziert, dass sich das Gerät auf dem neuesten Feature Update und Qualitäts Update befindet, das für dieses Gerät verfügbar ist. In " **bewermentforuptodate**" bedeutet das, dass das Gerät das aktuellste Qualitäts Update für die Windows-Version ist, die es ausgeführt wird.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**Updategutamentstatus \_ Notlatestsoftrestriction**
</dt> <dd>

Das aktuellste Funktions Update wurde aufgrund einer Soft-Einschränkung nicht installiert. Wenn eine weiche Einschränkung für ein Update festgelegt wurde, wird das Update nicht automatisch installiert. ein Benutzer muss den Download innerhalb der Update-UX selbst initiieren. Dieser Status gilt nur für " **bewermentforcurrent**".

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**Updategutamentstatus \_ Notlatesthardrestriction**
</dt> <dd>

Das aktuellste Funktions Update wurde aufgrund einer festen Einschränkung nicht installiert. Wenn eine feste Einschränkung für ein Update festgelegt wurde, kann das Update nicht auf das Gerät angewendet werden. Dieser Status gilt nur für " **bewermentforcurrent**".

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**Updategutamentstatus \_ Notlatestendof Support**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Update, da das Feature-Update des Geräts von Microsoft nicht mehr unterstützt wird. Wenn Microsoft eine Featureversion nicht mehr unterstützt, wird dieser Status sowohl für " **bewermentforcurrent** " als auch für " **bewermentforuptodate**" zurückgegeben.

> [!Note]  
> Wenn **updategutamentstatus \_ notlatestendofsupport** zurückgegeben wird, ist **updateimpactlevel** der Bewertung immer **updateimpactlevel \_ hoch**.

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**Updategutamentstatus \_ Notlatestservicingtrain**
</dt> <dd>

Das Gerät befindet sich nicht im aktuellen Featureupdate, da der Wartungsplan des Geräts die Aktualisierung auf das neueste Featureupdate einschränkt. Beispiel: Wenn ein Gerät on Current Branch for Business (CBB) ist und ein neues Funktions Update für Current Branch (CB) veröffentlicht wurde, wird dieses zurückgegeben. Dieser Status gilt nur für " **bewermentforcurrent**".

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**Updategutamentstatus \_ Notlatestdeferredfeature**
</dt> <dd>

Das aktuellste Featureupdate wurde nicht installiert, da es die zurückstellungs Richtlinie für das Windows Update for Business Feature Update des Geräts ist. Beim Bestimmen von **daysoutof** werden zurückstellungs Richtlinien berücksichtigt. **daysoudef** beginnt nicht mit dem Inkrementieren, bis der zurückstellungs Zeitraum abgelaufen ist. Dieser Status gilt nur für " **bewermentforcurrent**".

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**Updategutamentstatus \_ Notlatestdeferredquality**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Qualitäts Update aufgrund der Windows Update des Geräts für die zurückstellungs Richtlinie für Geschäfts Qualitäts Updates. Beim Bestimmen von **daysoutof** werden zurückstellungs Richtlinien berücksichtigt. **daysoudef** beginnt nicht mit dem Inkrementieren, bis der zurückstellungs Zeitraum abgelaufen ist.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**Updategutamentstatus \_ Notlatestpausedfeature**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Feature-Update, weil das Gerät über angehaltene Featureupdates verfügt. Ob ein Gerät angehalten wurde, wird nicht in die Berechnung von **daysouumf Date** einbezogen. Dieser Status gilt nur für " **bewermentforcurrent**".

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**Updategutamentstatus \_ Notlatestpausedquality**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Qualitäts Update, weil das Gerät über angehaltene Qualitäts Updates verfügt. Ob ein Gerät angehalten wurde, wird nicht in die Berechnung von **daysouumf Date** einbezogen. **daysoudef** ist nicht maßgeblich, ob ein Gerät in seiner Berechnung angehalten wird.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**Updategutamentstatus \_ Notlatestmanaged**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Update, da die Genehmigung von Updates nicht über Windows Update erfolgt.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**Updategutamentstatus \_ Notlatestunknown**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Update, weil der Grund dafür nicht durch die Bewertung bestimmt werden kann.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**Updategutamentstatus \_ Notlatesttargetedversion**
</dt> <dd>

Das Gerät befindet sich nicht im aktuellen Featureupdate aufgrund der Richtlinie für das Windows Update für die Geschäftsziel Version des Geräts. Bei dieser Richtlinie wird das Gerät auf der Zielversion der Funktions Version belassen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird am häufigsten mit den Strukturen [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) und [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) verwendet, die wiederum mit der [**gedesupdateassessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) -Methode für [**iwaasassessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>Waasapi. idl</dt> </dl> |



 

 




