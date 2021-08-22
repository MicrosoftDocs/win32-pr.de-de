---
description: LOCALE \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: da0d8697e8a02bb6943f4a4154a1ea89c4e01cbaed7576631e3a61d161e80503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147423"
---
# <a name="locale_ifirstweekofyear"></a>LOCALE \_ IFIRSTWEEKOFYEAR

Die erste Woche des Jahres.



| Wert | Bedeutung                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | Die Woche, die 1/1 enthält, ist die erste Woche des Jahres. Beachten Sie, dass dies ein einzelner Tag sein kann, wenn 1/1 auf den letzten Tag der Woche fällt. |
| 1     | Die erste vollständige Woche nach dem 1.1.ist die erste Woche des Jahres.                                                                     |
| 2     | Die erste Woche mit mindestens vier Tagen ist die erste Woche des Jahres. ISO 8601-kompatibel.                                     |

Wenn LOCALE_IFIRSTWEEKOFYEAR 2, LOCALE_IFIRSTDAYOFWEEK 0 (Montag) und LOCALE_ICALENDARTYPE gregorianisch ist, folgt die erste Woche der ISO 8601-Definition, wobei die erste Woche die Woche mit dem ersten Donnerstag des gregorianischen Jahres ist.


 

 

 



