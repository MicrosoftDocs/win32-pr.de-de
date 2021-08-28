---
description: Die CMsgThread-Klasse bietet Unterstützung für einen Arbeitsthread, an den Anforderungen asynchron anstatt direkt gesendet werden können.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMsg-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: 36d5110cbeda8cbf19c97c3f83ca1431a2cd28c5a07fa70c09e51877e0906a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016248"
---
# <a name="cmsg-class"></a>CMsg-Klasse

Die [**CMsgThread-Klasse**](cmsgthread.md) bietet Unterstützung für einen Arbeitsthread, an den Anforderungen asynchron anstatt direkt gesendet werden können. Die [**KLASSECAMThread**](camthread.md) stellt einen Arbeitsthread zur Verfügung, an den einzelne Anforderungen gesendet werden können. Nur ein Client kann gleichzeitig eine Anforderung senden, und der Client wird blockiert, bis der Arbeitsthread die Anforderung abgeschlossen hat. Im Gegensatz dazu stellt die **CMsgThread-Klasse** einen Arbeitsthread zur Verfügung, an den eine beliebige Anzahl von Anforderungen gesendet werden kann. Die Anforderungen (in Form eines -Objekts) werden asynchron in die Warteschlange gestellt `CMsg` und ausgeführt. Es wird kein Antwort- oder Rückgabewert empfangen.



| Datenelemente              | Beschreibung                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Flagparameter für den Anforderungscode.                                                                                                                                               |
| lpParam                   | Daten, die vom Arbeitsthread als Parameter oder Rückgabewerte benötigt werden. Diese Daten sollten nicht stapelbasierte Daten sein, da nach Abschluss des Warteschlangenvorgang einige Zeit darauf verwiesen wird. |
| pEvent                    | Ereignisobjekt, das ein Arbeitsthread signalisieren kann, um den Abschluss des Vorgangs anzugeben.                                                                                         |
| uMsg                      | Anforderungscode, der vom Client der Threadklasse definiert und von der überschriebenen Workerthreadfunktion verstanden wird.                                                           |
| Elementfunktionen          | Beschreibung                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Erstellt ein [**CMsg-Objekt.**](cmsg-cmsg.md)                                                                                                                                    |



 

 

 



