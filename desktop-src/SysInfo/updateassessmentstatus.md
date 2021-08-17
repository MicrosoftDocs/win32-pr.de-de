---
description: Beschreibt, wie aktuell das Betriebssystem auf einem Gerät ist.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: UpdateAssessmentStatus-Enumeration
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
ms.openlocfilehash: f4ece78c9593ab674a4198829c4e75612a9c4b337e17b3d2b6c5ed2fc19f42c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884306"
---
# <a name="updateassessmentstatus-enumeration"></a>UpdateAssessmentStatus-Enumeration

Beschreibt, wie aktuell das Betriebssystem auf einem Gerät ist. **UpdateAssessmentStatus** wird von [**den Strukturen UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) und [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) in den **Membern assessmentForCurrent,** **assessmentForUpToDate** und **securityStatus** verwendet. Es wird genau eine Konstante zurückgegeben.

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

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Neueste Version**
</dt> <dd>

Dieses Ergebnis in **assessmentForCurrent impliziert,** dass sich das Gerät auf dem neuesten Featureupdate und Qualitätsupdate befindet, das für dieses Gerät verfügbar ist. In **assessmentForUpToDate** impliziert dieses Ergebnis, dass das Gerät das neueste Qualitätsupdate für die Veröffentlichung Windows ausgeführt wird.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**
</dt> <dd>

Das neueste Featureupdate wurde aufgrund einer soft-Einschränkung nicht installiert. Wenn für ein Update eine weiche Einschränkung vorgenommen wurde, wird das Update nicht automatisch installiert. Ein Benutzer muss den Download auf der Update-Benutzeroberfläche selbst initiieren. Dieser Status gilt nur für **assessmentForCurrent.**

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**
</dt> <dd>

Das neueste Featureupdate wurde aufgrund einer harte Einschränkung nicht installiert. Wenn für ein Update eine harte Einschränkung gilt, gilt das Update nicht für das Gerät. Dieser Status gilt nur für **assessmentForCurrent.**

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**
</dt> <dd>

Das Gerät befindet sich nicht im neuesten Update, da das Featureupdate des Geräts nicht mehr von Microsoft unterstützt wird. Wenn Microsoft keine Featureversion mehr unterstützt, wird dieser Status sowohl für **assessmentForCurrent** als auch **für assessmentForUpToDate zurückgegeben.**

> [!Note]  
> Wenn **UpdateAssessmentStatus \_ NotLatestEndOfSupport** zurückgegeben wird, ist **UpdateImpactLevel** der Bewertung immer **UpdateImpactLevel \_ High.**

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**
</dt> <dd>

Das Gerät befindet sich nicht im neuesten Featureupdate, da der Wartungs trainieren des Geräts das Update des Geräts auf das neueste Featureupdate beschränkt. Beispiel: Wenn sich ein Gerät auf Current Branch for Business (CBB) befindet und ein neues Featureupdate für Current Branch (CB) veröffentlicht wurde, wird dies zurückgegeben. Dieser Status gilt nur für **assessmentForCurrent.**

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**
</dt> <dd>

Das neueste Featureupdate wurde aufgrund der Richtlinie "Update for Business Windows update update deferral des Geräts nicht installiert. Bei der **Bestimmung von daysOutOfDate** werden Zurückbegrenzungsrichtlinien berücksichtigt. **daysOutOfDate wird** erst erhöht, wenn der Verzögerungszeitraum abgelaufen ist. Dieser Status gilt nur für **assessmentForCurrent.**

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**
</dt> <dd>

Das Gerät befindet sich Windows aufgrund der Richtlinie "Update for Business Quality Update Deferral" des Geräts nicht auf dem neuesten Qualitätsupdate. Bei der **Bestimmung von daysOutOfDate** werden Zurückbegrenzungsrichtlinien berücksichtigt. **daysOutOfDate wird** erst erhöht, wenn der Verzögerungszeitraum abgelaufen ist.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**
</dt> <dd>

Das Gerät befindet sich nicht im neuesten Featureupdate, da das Gerät Funktionsupdates angehalten hat. Ob ein Gerät angehalten wird, wird nicht in die Berechnung von **daysOutOfDate einbezogen.** Dieser Status gilt nur für **assessmentForCurrent.**

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**
</dt> <dd>

Das Gerät befindet sich nicht im neuesten Qualitätsupdate, da das Gerät Qualitätsupdates angehalten hat. Ob ein Gerät angehalten wird, wird nicht in die Berechnung von **daysOutOfDate einbezogen.** **daysOutOfDate** berücksichtigt nicht, ob ein Gerät bei der Berechnung angehalten wird.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**
</dt> <dd>

Das Gerät befindet sich nicht auf dem neuesten Update, da die Genehmigung von Updates nicht über das Windows erfolgt.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**
</dt> <dd>

Das Gerät befindet sich aufgrund eines Grunds, der von der Bewertung nicht bestimmt werden kann, nicht auf dem neuesten Update.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**
</dt> <dd>

Das Gerät befindet sich aufgrund der Richtlinie "Update for Business-Zielversion" Windows gerät nicht auf dem neuesten Featureupdate. Diese Richtlinie hält das Gerät auf der Releaseversion des Zielfeatures.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird am häufigsten mit den [**Strukturen UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) und [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) verwendet, die wiederum mit der [**GetOSUpdateAssessment-Methode**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) für [**IWaaSAssessor verwendet werden.**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                   |
| Idl<br/>                      | <dl> <dt>WaaSAPI.idl</dt> </dl> |



 

 




