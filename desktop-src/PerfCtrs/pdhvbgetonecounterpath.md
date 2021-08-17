---
description: Die PdhVbGetOneCounterPath-Funktion zeigt ein Dialogfeld an, in dem der Benutzer die verfügbaren Leistungsindikatoren durchsuchen und einen Leistungsindikator auswählen kann.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: da6cc5b476373a55135d91d21163f15cb04379fff9d7c7c2cf1342451a5a201d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061158"
---
# <a name="pdhvbgetonecounterpath-function"></a>PdhVbGetOneCounterPath-Funktion

Die **PdhVbGetOneCounterPath-Funktion** zeigt ein Dialogfeld an, in dem der Benutzer die verfügbaren Leistungsindikatoren durchsuchen und einen Leistungsindikator auswählen kann. Der ausgewählte Zähler wird in der *PathString-Variablen* zurückgegeben. Die *PathString-Variable* muss dimensioniert und initialisiert werden, bevor diese Funktion aufgerufen wird, und die dimensionierte Größe muss durch die *PathLength-Variable angegeben* werden.

> [!IMPORTANT]
> Die funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der unter [Leistungsindikatorfunktionen beschriebenen Funktionen.](performance-counters-functions.md)

Funktion PdhVbGetOneCounterPath( \_ ByVal PathString as String, \_ ByVal PathLength as long, \_ ByVal DetailLevel as long, \_ ByVal CaptionString as String \_ ) so long

## <a name="parameters"></a>Parameter

<dl> <dt>

*PathString* 
</dt> <dd>

Initialisierte Zeichenfolgenvariable, die zum Empfangen des vom Benutzer ausgewählten Indikatorpfads verwendet wird.

</dd> <dt>

*PathLength* 
</dt> <dd>

Länge der initialisierten PathString.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Typen von Leistungsindikatoren, die im Dialogfeld angezeigt werden sollen. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**PERF \_ DETAIL \_ ADVANCED**</dt> </dl> | Leistungsindikatoren, die der fortgeschrittene Benutzer neben den Zählern für fortgeschrittene Benutzer wahrscheinlich versteht.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**PERF \_ DETAIL \_ EXPERT**</dt> </dl>       | Leistungsindikatoren, die der erfahrene Benutzer und Softwareentwickler wahrscheinlich verstehen werden, zusätzlich zu den Leistungsindikatoren für die Fortgeschrittene und fortgeschrittene Benutzer.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**\_ \_ PERF-DETAILINSZENIERUNG**</dt> </dl>       | Nur Leistungsindikatoren, die der unerfahrene Benutzer wahrscheinlich versteht.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**ASSISTENT FÜR \_ \_ PERF-DETAILS**</dt> </dl>       | Alle Leistungsindikatoren im System.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Zeichenfolgenvariable, die den Text enthält, der in der Beschriftungsleiste des Dialogfelds angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die Anzahl der Zeichen zurück, die in den *PathString-Puffer geschrieben* werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




