---
description: DEP/NX-Schutz
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX-Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088568"
---
# <a name="depnx-protection"></a>DEP/NX-Schutz

Ab Windows Internet Explorer 7 unter Windows Vista enthält das  Element der Internetsteuerung die Option Speicherschutz aktivieren, um Onlineangriffe zu minimieren. Diese Option wird auch als Datenausführungsverhindung (Data *Execution Prevention,* DEP) oder *No-Execute* (NX) bezeichnet. Wenn diese Option aktiviert ist, arbeitet sie mit dem Prozessor zusammen, um Pufferüberlaufangriffe zu verhindern, indem die Codeausführung im Arbeitsspeicher blockiert wird, der als nicht ausführbare Datei gekennzeichnet ist.

In Windows Internet Explorer 8 unter Windows Vista mit Service Pack 1 -Betriebssystem (SP1) oder einer neueren Version ist diese Option standardmäßig aktiviert. DEP/NX schützt nicht vor allen speicherbasierten Sicherheitsrisiken. Wenn sie jedoch mit anderen Technologien wie der zufälligen Anordnung des Adressraumlayouts (Address Space Layout Randomization, ASLR) kombiniert wird, trägt sie dazu bei, häufige Pufferüberlauf-Sicherheitsrisiken in Windows Internet Explorer und den add-ons zu verhindern, die geladen werden. Für diesen Schutz ist keine zusätzliche Benutzerinteraktion erforderlich, und es werden keine neuen Eingabeaufforderungen eingeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



