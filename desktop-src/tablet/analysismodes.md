---
description: Gibt an, wie iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: AnalysisModes-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393238"
---
# <a name="analysismodes-enumeration"></a>AnalysisModes-Enumeration

Gibt an, wie [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.

## <a name="syntax"></a>Syntax


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ None**
</dt> <dd>

Es wurden keine Modi angegeben.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ automatikreversöhnung**
</dt> <dd>

Gibt an, ob der [**iinkanalyzer**](iinkanalyzer.md) den Abstimmungs Vorgang automatisch startet, sobald die Zwischenergebnisse oder Endergebnisse bereit sind.

Wenn dieser Modus aktiviert ist, wird das [**\_ ianalysissevents:: leseytor econcile**](-ianalysisevents-readytoreconcile.md) -Ereignis nicht ausgelöst. Wenn dieser Modus deaktiviert ist, wird das **\_ ianalysissevents:: leseytor econcile** -Ereignis ausgelöst.

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ strokecacheautocleanup**
</dt> <dd>

Gibt an, ob der [**iinkanalyzer**](iinkanalyzer.md) automatisch nicht benötigte Striche aus dem Strich Cache löscht, bevor eine Analyse durchgeführt wird.

Wenn dieser Modus aktiviert ist, löscht [**iinkanalyzer**](iinkanalyzer.md) die Strich Daten vor dem Durchführen der Analyse. Der Code muss dann auch das [**\_ ianalysisevents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis behandeln. Wenn das **\_ ianalysil Vents:: updatestrokescache** -Ereignis nicht behandelt wird, wird eine Ausnahme ausgelöst. Diese Überprüfung erfolgt sowohl bei den Analyse-(oder BackgroundAnalyze)-als auch bei Abstimmungs Phasen.

Wenn dieser Modus deaktiviert ist, werden die Strich Daten von [**iinkanalyzer**](iinkanalyzer.md) nicht gelöscht. Um die Strich Daten zu löschen, müssen Sie die [**iinkanalyzer:: ClearStrokeData-Methode**](iinkanalyzer-clearstrokedata.md)aufrufen. Wenn dieser Modus deaktiviert ist, wird das [**\_ ianalysitsvents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis ausgelöst, sodass der **iinkanalyzer** die neuesten hubdaten für alle Striche abrufen kann, bei denen der Cache gelöscht wurde. Wenn der Strich Cache gelöscht wird, das **\_ ianalysil Vents:: updatestrokescache** -Ereignis jedoch nicht behandelt wird, wird eine Ausnahme ausgelöst.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ personalizationaktivierte**
</dt> <dd>

Die Personalisierung der Handschrifterkennung ist aktiviert.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes ( \_ Standard)**
</dt> <dd>

Alle Modi sind aktiviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration ermöglicht eine bitweise Kombination der Element Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer:: getanalysismodes-Methode**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Iinkanalyzer:: abtanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_Ianalysilvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_Ianalysissevents:: luytor econcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_Ianalysil Vents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




