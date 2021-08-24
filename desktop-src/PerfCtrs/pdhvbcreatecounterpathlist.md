---
description: Die PdhVbCreateCounterPathList-Funktion zeigt das Dialogfeld zum Durchsuchen des Leistungsindikators an, in dem der Benutzer mehrere Leistungsindikatoren auswählen kann. Jeder ausgewählte Indikatorpfad muss dann mit der PdhVbGetCounterPathFromList-Funktion gelesen werden.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6471fe3baee14fa1853810b66a804974b05ca84d0db9bc4e7dd805085ad5c0c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775550"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>PdhVbCreateCounterPathList-Funktion

Die **PdhVbCreateCounterPathList-Funktion** zeigt das Dialogfeld zum Durchsuchen des Leistungsindikators an, in dem der Benutzer mehrere Leistungsindikatoren auswählen kann. Jeder ausgewählte Indikatorpfad muss dann mithilfe der [**PdhVbGetCounterPathFromList-Funktion gelesen**](pdhvbgetcounterpathfromlist.md) werden.

> [!IMPORTANT]
> Die funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der unter [Leistungsindikatorfunktionen beschriebenen Funktionen.](performance-counters-functions.md)

Funktion PdhVbCreateCounterPathList( \_ ByVal DetailLevel as long, \_ ByVal CaptionString as String \_ ) as long

## <a name="parameters"></a>Parameter

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Typen von Leistungsindikatoren, die im Dialogfeld angezeigt werden sollen. Verwenden Sie einen der folgenden Werte.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**PERF \_ DETAIL \_ ADVANCED**</dt> </dl> | Leistungsindikatoren, die der fortgeschrittene Benutzer neben den Zählern für Fortgeschrittene wahrscheinlich versteht.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**PERF \_ DETAIL \_ EXPERT**</dt> </dl>       | Leistungsindikatoren, die der erfahrene Benutzer und Softwareentwickler wahrscheinlich verstehen werden, zusätzlich zu den Leistungsindikatoren für die Fortgeschrittene und fortgeschrittene Benutzer.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**\_ \_ PERF-DETAILINSZENIERUNG**</dt> </dl>       | Nur Leistungsindikatoren, die der unerfahrene Benutzer wahrscheinlich versteht.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**ASSISTENT FÜR \_ \_ PERF-DETAILS**</dt> </dl>       | Alle Leistungsindikatoren im System.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Zeichenfolgenvariable, die den Text enthält, der in der Beschriftungsleiste des Dialogfelds angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die Anzahl von Indikatorpfaden zurück, die der Benutzer ausgewählt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




