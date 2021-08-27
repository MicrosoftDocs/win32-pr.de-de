---
description: Beschreibt zeitformate, die für die Verwendung in der WQL WHERE-Klausel unterstützt werden.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported Zeitformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627b46ef7d01a2eb3e8e40484b37822c9ebca55a9487b1ffb0e1a138ab7378d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049738"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported Zeitformate

Zusätzlich zum WMI DATETIME-Format werden die folgenden Datumsformate für die Verwendung in der WQL WHERE-Klausel unterstützt.



| Format                                    | Beschreibung                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hh \[ \] {AP}M<br/>                   | Stunde, wie auf einer Zwölf-Stunden-Uhr und AM- oder PM-Bezeichnung dargestellt.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Stunde und Minuten mit Doppelpunkttrennzeichen. Keine AM- oder PM-Bezeichnung.<br/> 3:23<br/>                                                                                                                  |
| hh:mm \[ \] {AP}M<br/>                | Durch Doppelpunkte getrennte Stunden- und Minutenangabe, optionaler Speicherplatz und AM- oder PM-Bezeichnung.<br/> 3:23 Uhr<br/>                                                                                              |
| hh:mm:ss<br/>                       | Stunde, Minuten und Sekunden mit Doppelpunkttrennzeichen. Keine AM/PM-Bezeichnung.<br/> 3:23:00<br/>                                                                                                         |
| hh:mm:ss \[ \] {AP}M<br/>             | Durch Doppelpunkte getrennte Stunde, Minuten und Sekunden, optionaler Speicherplatz und AM/PM-Bezeichnung.<br/> 15:23:00 Uhr<br/>                                                                                      |
| hh:mm:ss:uuu<br/>                   | Durch Doppelpunkte getrennte Stunde, Minuten und Sekunden sowie dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht.<br/>                                    |
| hh:mm:ss: \[ \[ u u u \] \] u<br/>           | Stunde, Minuten und Sekunden mit Doppelpunkttrennzeichen; und ein, zwei- oder dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht.<br/>                       |
| hh:mm:ss:uuu \[ \] {AP}M<br/>         | Stunden-, Minuten- und Sekundenoffset mit Doppelpunkttrennzeichen, dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von der UTC- und AM- oder PM-Bezeichnung abweicht.<br/>              |
| hh:mm:ss: \[ \[ u u u \] \] \[ \] {AP}M<br/> | Stunde, Minuten und Sekunden mit Doppelpunkttrennzeichen; ein-, zwei- oder dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht; und AM- oder PM-Bezeichnung.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WHERE-Klausel](where-clause.md)
</dt> </dl>

 

 




