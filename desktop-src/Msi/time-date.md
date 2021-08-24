---
description: Der Time/Date-Datentyp verfügt über die Uhrzeit und das Datum, die einzeln gespeichert werden. Dabei werden ganze Zahlen ohne Vorzeichen als Bitfelder verwendet, die wie folgt gepackt werden.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Time/Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3c5cccc2f1211918b52008f0d81a7e4693dfd14766696b77cd184d75f4309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810740"
---
# <a name="timedate"></a>Time/Date

Der Time/Date-Datentyp verfügt über die Uhrzeit und das Datum, die einzeln gespeichert werden. Dabei werden ganze Zahlen ohne Vorzeichen als Bitfelder verwendet, die wie folgt gepackt werden.

## <a name="time"></a>Zeit

Die Zeit wird in einer 2-Byte-Ganzzahl ohne Vorzeichen mit den folgenden Bitfeldern codiert.



| Inhalte           | Bits        | Wertebereich |
|--------------------|-------------|-------------|
| Stunden              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| 2-Sekunden-Intervalle | B C D E F   | 0–29        |



 

## <a name="date"></a>Date

Date wird in einer 2-Byte-Ganzzahl ohne Vorzeichen mit den folgenden Bitfeldern codiert.



| Inhalte | Bits          | Wertebereich              |
|----------|---------------|--------------------------|
| year     | 0 1 2 3 4 5 6 | 0–119 (relativ zu 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



