---
description: Der Datums-/Uhrzeittyp verfügt über die Uhrzeit und das Datum, das einzeln gespeichert wird. dabei werden Ganzzahlen ohne Vorzeichen als Bitfelder verwendet, die wie folgt verpackt werden.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Time/Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360599"
---
# <a name="timedate"></a>Time/Date

Der Datums-/Uhrzeittyp verfügt über die Uhrzeit und das Datum, das einzeln gespeichert wird. dabei werden Ganzzahlen ohne Vorzeichen als Bitfelder verwendet, die wie folgt verpackt werden.

## <a name="time"></a>Time

Die Zeit wird in einer nicht signierten 2-Byte-Ganzzahl mit den folgenden Bitfeldern codiert.



| Inhalte           | Bits        | Wertebereich |
|--------------------|-------------|-------------|
| Stunden              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| 2-Sekunden-Intervalle | B C D E F   | 0 – 29        |



 

## <a name="date"></a>Date

Das Datum wird in einer nicht signierten 2-Byte-Ganzzahl mit den folgenden Bitfeldern codiert.



| Inhalte | Bits          | Wertebereich              |
|----------|---------------|--------------------------|
| year     | 0 1 2 3 4 5 6 | 0 – 119 (relativ zu 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



