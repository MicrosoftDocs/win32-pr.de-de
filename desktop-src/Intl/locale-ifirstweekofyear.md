---
description: Gebiets Schema \_ ifirstweekosyear
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106351821"
---
# <a name="locale_ifirstweekofyear"></a>Gebiets Schema \_ ifirstweekosyear

Die erste Woche des Jahres.



| Wert | Bedeutung                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | Woche, die 1/1 enthält, ist die erste Woche des Jahres. Beachten Sie, dass dies ein einzelner Tag sein kann, wenn 1/1 auf den letzten Tag der Woche fällt. |
| 1     | Die erste vollständige Woche nach 1/1 ist die erste Woche des Jahres.                                                                     |
| 2     | Die erste Woche mit mindestens vier Tagen ist die erste Woche des Jahres. ISO 8601-kompatibel.                                     |

Wenn LOCALE_IFIRSTWEEKOFYEAR 2 ist, LOCALE_IFIRSTDAYOFWEEK den Wert 0 (Montag) hat und LOCALE_ICALENDARTYPE Gregorianisch ist, dann folgt die erste Woche der ISO 8601-Definition, wobei die erste Woche die Woche mit dem ersten Donnerstag des gregorianischen Jahres ist.


 

 

 



