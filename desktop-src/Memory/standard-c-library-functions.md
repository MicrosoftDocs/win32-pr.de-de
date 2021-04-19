---
description: Anwendungen können die Speicherverwaltungsfunktionen der C-Lauf Zeit Bibliothek (malloc, Free usw.) und C++ (neu, löschen usw.) sicher verwenden.
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Standard-C-Bibliotheksfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349057"
---
# <a name="standard-c-library-functions"></a>Standard-C-Bibliotheksfunktionen

Anwendungen können die Speicherverwaltungsfunktionen der C-Lauf Zeit Bibliothek (**malloc**, **Free** usw.) und C++ (**neu**, **Löschen** usw.) sicher verwenden. Die Funktionen der C-Lauf Zeit Bibliothek haben nicht die potenziellen Probleme, die Sie unter 16-Bit-Fenstern haben. Die Speicherverwaltung ist kein Problem mehr, da das System Arbeitsspeicher freigeben kann, indem Seiten des physischen Speichers verschoben werden, ohne dass sich dies auf die virtuellen Adressen auswirkt. Ebenso ist der Unterschied zwischen Near-und Far-Zeigern nicht mehr relevant. Daher können Sie die Standard-C-Bibliotheksfunktionen für die Speicherverwaltung verwenden. Die Speicherverwaltungsfunktionen bieten jedoch Funktionen, die in der C-Lauf Zeit Bibliothek nicht verfügbar sind.

 

 



