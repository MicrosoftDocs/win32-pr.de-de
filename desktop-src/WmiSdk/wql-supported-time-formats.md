---
description: Beschreibt Zeitformate, die für die Verwendung in der WQL WHERE-Klausel unterstützt werden.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported Zeitformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368234"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported Zeitformate

Zusätzlich zum WMI-DateTime-Format werden die folgenden Datumsformate für die Verwendung in der WQL-WHERE-Klausel unterstützt.



| Format                                    | BESCHREIBUNG                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HH \[ \] {AP} M<br/>                   | Stunde, wie in einer zwölfstündigen Uhr und am-oder PM-Bezeichnung angezeigt.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Durch Trennzeichen getrennte Stunde und Minuten. Keine am-oder PM-Bezeichnung.<br/> 3:23<br/>                                                                                                                  |
| hh: mm \[ \] {AP} M<br/>                | Durch Trennzeichen getrennte Stunde und Minuten, optionaler Raum und am-oder PM-Bezeichnung.<br/> 3:23 Uhr<br/>                                                                                              |
| hh:mm:ss<br/>                       | Durch Trennzeichen getrennte Stunde, Minuten und Sekunden. Keine am/pm-Bezeichnung.<br/> 3:23:00<br/>                                                                                                         |
| hh: mm: SS \[ \] {AP} M<br/>             | Durch Trennzeichen getrennte Stunde, Minuten und Sekunden, Optionaler Leerraum und am/pm-Bezeichnung.<br/> 3:23 Uhr<br/>                                                                                      |
| hh: mm: SS: uuu<br/>                   | Durch Trennzeichen getrennte Stunde, Minuten und Sekunden und ein dreistelliger Offset, das die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht.<br/>                                    |
| hh: mm: SS: \[ \[ u \] u \] u<br/>           | Durch Trennzeichen getrennte Stunde, Minuten und Sekunden. und einen, zwei oder dreistelligen Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht.<br/>                       |
| hh: mm: SS: uuu \[ \] {AP} M<br/>         | Durch Trennzeichen getrennte Stunde, Minuten und Sekunden, ein dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC und am oder PM-Bezeichnung abweicht.<br/>              |
| hh: mm: SS: \[ \[ u \] u \] \[ \] {AP} M<br/> | Durch Trennzeichen getrennte Stunde, Minuten und Sekunden. ein-, zwei-oder dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht. und am-oder PM-Bezeichnung.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WHERE-Klausel](where-clause.md)
</dt> </dl>

 

 




