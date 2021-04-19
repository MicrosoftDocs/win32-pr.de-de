---
description: Die cmsgthread-Klasse bietet Unterstützung für einen Arbeits Thread, an den Anforderungen asynchron gesendet werden können, anstatt direkt gesendet zu werden.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMSG-Klasse
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
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345593"
---
# <a name="cmsg-class"></a>CMSG-Klasse

Die [**cmsgthread**](cmsgthread.md) -Klasse bietet Unterstützung für einen Arbeits Thread, an den Anforderungen asynchron gesendet werden können, anstatt direkt gesendet zu werden. Die [**camthread**](camthread.md) -Klasse stellt einen Arbeits Thread bereit, an den einzelne Anforderungen gesendet werden können. Nur ein Client kann eine Anforderung gleichzeitig ausführen, und der Client wird blockiert, bis der Arbeits Thread die Anforderung abgeschlossen hat. Im Gegensatz dazu stellt die **cmsgthread** -Klasse einen Arbeits Thread bereit, an den eine beliebige Anzahl von Anforderungen gesendet werden kann. Die Anforderungen (in Form eines- `CMsg` Objekts) werden in der Reihenfolge asynchron in die Warteschlange eingereiht und ausgeführt. Es wird keine Antwort oder kein Rückgabewert empfangen.



| Datenelemente              | BESCHREIBUNG                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Markieren Sie den Parameter für den Anforderungs Code.                                                                                                                                               |
| lpparam                   | Daten, die vom Arbeits Thread als Parameter oder Rückgabewerte benötigt werden. Diese Daten sollten nicht Stapel basiert sein, da nach Abschluss des Warteschlangen Vorgangs einige Zeit darauf verwiesen wird. |
| Peer Event                    | Ereignis Objekt, das ein Arbeits Thread signalisieren kann, um den Abschluss des Vorgangs anzugeben.                                                                                         |
| Umschlag                      | Anforderungs Code, der vom Client der Thread Klasse definiert und von der überschriebenen Arbeits Thread Funktion verstanden wird.                                                           |
| Elementfunktionen          | BESCHREIBUNG                                                                                                                                                                       |
| [**CMSG**](cmsg-cmsg.md) | Erstellt ein [**CMSG**](cmsg-cmsg.md) -Objekt.                                                                                                                                    |



 

 

 



