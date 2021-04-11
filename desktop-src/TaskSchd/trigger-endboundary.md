---
title: Auslöse. endborder-Eigenschaft
description: Ruft bei der Skripterstellung das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Endboundary-Eigenschaft Taskplaner
- Endboundary-Eigenschaften Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, endboundary-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040390"
---
# <a name="triggerendboundary-property"></a>Auslöse. endborder-Eigenschaft

Ruft bei der Skripterstellung das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.

## <a name="syntax"></a>Syntax


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Eigenschaftswert

Das Datum und die Uhrzeit der Deaktivierung des Auslösers. Das Datum und die Uhrzeit müssen im folgenden Format vorliegen: yyyy-mm-ddThh: mm: SS (+-) hh: mm. Beispielsweise würde das Datum am 11. Oktober 2005 um 1:21:17 in der Pacific Time Zone als "2005-10-11t13:21:17-08:00" geschrieben werden. Der Abschnitt (+-) hh: mm des Formats beschreibt die Zeitzone als eine bestimmte Anzahl von Stunden vor oder hinter koordinierter Weltzeit (Greenwich Mean Time).

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die aktivierte Eigenschaft mit dem [**endboundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





