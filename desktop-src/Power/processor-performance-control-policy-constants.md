---
description: Die Konstanten der Prozessor Leistungs Steuerungs-Richtlinie geben den Prozessor Leistungs Steuerungsalgorithmus an, der auf ein Energie Schema angewendet wird.
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: Richtlinien Konstanten für die Prozessor Leistungssteuerung (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597750f37d9efda80d4bb2bfff7bc121982e7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529108"
---
# <a name="processor-performance-control-policy-constants"></a>Richtlinien Konstanten für die Prozessor Leistungssteuerung

Die Konstanten der Prozessor Leistungs Steuerungs-Richtlinie geben den Prozessor Leistungs Steuerungsalgorithmus an, der auf ein Energie Schema angewendet wird.



| Konstante/Wert                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <dt>**Po \_ Einschränken von \_ adaptiver**</dt> <dt>3</dt> </dl> | Versucht, die Leistung des Prozessors mit der aktuellen Anforderung zu vergleichen. Diese Richtlinie verwendet sowohl den Status "hoch" als auch "niedrig" und "Häufigkeit" Durch diese Richtlinie wird die Leistung des Prozessors auf die niedrigste Spannung gesenkt, die immer dann verfügbar ist, wenn nicht genügend Anforderungen zum begründen einer höheren Spannung vorhanden sind. Diese Richtlinie übernimmt die Prozessor Takt Drosselung, wenn der C3-Zustand nicht verwendet wird, und als Reaktion auf thermische Ereignisse.<br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <dt>**Po \_ Drosselungs \_ Konstante**</dt> <dt>1</dt> </dl> | Ermöglicht es dem Prozessor nicht, Leistungszustände mit hoher Spannung zu verwenden. Diese Richtlinie übernimmt keine Reaktion auf die Prozessor Takt Drosselung, außer als Reaktion auf thermische Ereignisse.<br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <dt>**Po \_ Drosselungs \_ Stufe**</dt> <dt>2</dt> </dl>    | Ermöglicht es dem Prozessor nicht, Leistungszustände mit hoher Spannung zu verwenden. Diese Richtlinie übernimmt die Prozessor Takt Drosselung, wenn der Akku unter einem bestimmten Schwellenwert liegt, wenn der C3-Zustand nicht verwendet wird, oder als Reaktion auf thermische Ereignisse.<br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <dt>**Po \_ Drosselung \_**</dt> nicht <dt>0</dt> </dl>             | Es wird keine Prozessor Leistungskontrolle angewendet. Diese Richtlinie führt den Prozessor immer mit der höchsten möglichen Leistungsstufe aus. Diese Richtlinie übernimmt keine Reaktion auf die Prozessor Takt Drosselung, außer als Reaktion auf thermische Ereignisse.<br/>                                                                                                                                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



 

 




