---
title: Eigenschafts Bezeichner/Offset-Paare
description: Nach der Anzahl von Eigenschaften Satz Wert für Eigenschaften ist ein Array von Eigenschafts Werten für Eigenschaften Bezeichner/Offset Paare festgelegt.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339449"
---
# <a name="property-identifiersoffset-pairs"></a>Eigenschafts Bezeichner/Offset-Paare

Nach der Anzahl von Eigenschaften Satz Wert für Eigenschaften ist ein Array von Eigenschafts Werten für Eigenschaften Bezeichner/Offset Paare festgelegt. Eigenschafts Bezeichner sind 32-Bit-Werte, die eine Eigenschaft innerhalb eines Abschnitts eindeutig identifizieren. Die Offset Paare geben den Abstand zwischen dem Anfang des Abschnitts und dem Anfang des Eigenschaftentyp-Wert-Paars an. Da die Offsets relativ zum Abschnitt sind, können Abschnitte als Bytearray kopiert werden.

Eigenschafts Bezeichner werden nicht in einer bestimmten Reihenfolge sortiert. Eigenschaften können im gespeicherten Eigenschaften Satz ausgelassen werden. die Leser dürfen sich nicht auf eine bestimmte Reihenfolge oder einen bestimmten Bereich von Eigenschafts Bezeichner verlassen.

 

 




