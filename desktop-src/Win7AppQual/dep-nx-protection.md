---
description: DEP/NX-Schutz
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX-Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec30b3758361cbe2ed20e67fe6792d6f76b58a7266c6de1d554afdba8a2519c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329940"
---
# <a name="depnx-protection"></a>DEP/NX-Schutz

Ab Windows Internet Explorer 7 auf Windows Vista enthält das Element der Internetsteuerung eine Option **Speicherschutz aktivieren,** um Onlineangriffe zu minimieren. Diese Option wird auch als *Datenausführungsverhinderung (Data Execution Prevention,* DEP) oder *No-Execute* (NX) bezeichnet. Wenn diese Option aktiviert ist, arbeitet sie mit dem Prozessor zusammen, um Pufferüberlaufangriffe zu verhindern, indem die Codeausführung im Arbeitsspeicher blockiert wird, der als nicht ausführbare Datei markiert ist.

In Windows Internet Explorer 8 auf der Windows Vista mit dem Betriebssystem Service Pack 1 (SP1) oder einer neueren Version ist diese Option standardmäßig aktiviert. DEP/NX schützt nicht vor allen speicherbasierten Sicherheitsrisiken. Wenn sie jedoch mit anderen Technologien wie der Zufälligkeit des Adressraumlayouts (Address Space Layout Randomization, ASLR) kombiniert wird, können sie häufige Pufferüberlaufrisiken in Windows Internet Explorer und den von ihr geladenen Add-Ons verhindern. Für diesen Schutz ist keine zusätzliche Benutzerinteraktion erforderlich, und es werden keine neuen Eingabeaufforderungen eingeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



