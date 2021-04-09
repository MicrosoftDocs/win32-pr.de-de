---
description: Die pdhvbkreatecounterpathlist-Funktion zeigt das Dialogfeld zum Durchsuchen des Leistungsindikators an, mit dem der Benutzer mehrere Leistungsindikatoren auswählen kann. Jeder ausgewählte Indikator Pfad muss dann mithilfe der pdhvbgetcounterpathfromlist-Funktion gelesen werden.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: Pdhvbkreatecounterpathlist-Funktion
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
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865116"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>Pdhvbkreatecounterpathlist-Funktion

Die **pdhvbkreatecounterpathlist** -Funktion zeigt das Dialogfeld zum Durchsuchen des Leistungsindikators an, mit dem der Benutzer mehrere Leistungsindikatoren auswählen kann. Jeder ausgewählte Indikator Pfad muss dann mithilfe der [**pdhvbgetcounterpathfromlist**](pdhvbgetcounterpathfromlist.md) -Funktion gelesen werden.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Function pdhvbkreatecounterpathlist ( \_ ByVal DetailLevel As Long, \_ ByVal captionstring As String \_ ) so lange

## <a name="parameters"></a>Parameter

<dl> <dt>

*Detail Level* 
</dt> <dd>

Typen von Leistungsindikatoren, die im Dialogfeld angezeigt werden sollen. Verwenden Sie einen der folgenden Werte.



| Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**Leistungs \_ Details \_ erweitert**</dt> </dl> | Leistungsindikatoren, die der Erweiterte Benutzer wahrscheinlich versteht, zusätzlich zu den Endbenutzer-Leistungsindikatoren.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**Perf- \_ Detail \_ Experte**</dt> </dl>       | Leistungsindikatoren für den Benutzer und den Softwareentwickler, zusätzlich zu den Leistungsindikatoren für die Anfänger und Fortgeschrittene.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**Perf- \_ Detail- \_ Anfänger**</dt> </dl>       | Nur Leistungsindikatoren, die der Anfänger wahrscheinlich versteht.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**Perf- \_ Detail- \_ Assistent**</dt> </dl>       | Alle Leistungsindikatoren im System.<br/>                                                                                                                  |



 

</dd> <dt>

*Captionstring* 
</dt> <dd>

Zeichen folgen Variable, die den Text enthält, der auf der Beschriftungs Leiste des Dialog Felds angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt die Anzahl der gegen Pfade zurück, die vom Benutzer ausgewählt wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhvbgetcounterpathelements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**Pdhvbgetcounterpathfromlist**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**Pdhvbgetonecounterpath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




