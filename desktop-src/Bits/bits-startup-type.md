---
title: BITS-Starttyp
description: Der Starttyp für BITS wird verzögert automatisch gestartet. Vor der Windows Vista ist der Starttyp für BITS manuell. Wenn ein BITS-Auftrag erstellt wird, ändert sich der Starttyp in Automatisch. Der Starttyp kehrt zu Manuell zurück, wenn alle Aufträge abgeschlossen oder abgebrochen wurden.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: defafff5b3dd0a9b03e18b61b84fa6c32022035ce58913599151ee526fd52d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579430"
---
# <a name="bits-startup-type"></a>BITS-Starttyp

Der **Starttyp für** BITS verzögert den automatischen Start (wenn aktive BITS-Aufträge sind) oder der Bedarfsstart (wenn keine aktiven Aufträge sind). Versionen von Windows vor dem November-Update verwendeten nur den verzögerten Starttyp für den automatischen Start. Versionen vor Vista verwendeten den manuellen Starttyp.

Sie sollten den Starttyp **nicht auf** Deaktiviert festlegen. Durch das Deaktivieren von BITS können Anwendungen, die bits zum Übertragen von Dateien verwenden, unter Umständen nicht mehr verwendet werden.

 

 




