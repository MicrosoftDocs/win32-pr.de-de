---
description: Anwendungen können die Speicherverwaltungsfeatures der C-Laufzeitbibliothek (malloc, free und so weiter) und C++ (neu, löschen und so weiter) sicher verwenden.
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: C-Standardbibliotheksfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1447a64f00fbd1b4cccf70f7589f267ebba526d66528d7342da68068f81ebfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963210"
---
# <a name="standard-c-library-functions"></a>C-Standardbibliotheksfunktionen

Anwendungen können die Speicherverwaltungsfeatures der C-Laufzeitbibliothek **(malloc,** **free** und so weiter) und C++**(neu,** **löschen** und so weiter) sicher verwenden. Die C-Laufzeitbibliotheksfunktionen haben nicht die potenziellen Probleme, die unter 16-Bit-Windows. Die Speicherverwaltung ist kein Problem mehr, da das System den Speicher durch Verschieben von Seiten des physischen Speichers ohne Auswirkungen auf die virtuellen Adressen verwalten kann. Ebenso ist der Unterschied zwischen nah und fernen Zeigern nicht mehr relevant. Daher können Sie die C-Standardbibliotheksfunktionen für die Speicherverwaltung verwenden. Die Speicherverwaltungsfunktionen bieten jedoch Funktionen, die in der C-Laufzeitbibliothek nicht verfügbar sind.

 

 



