---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX-Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868755"
---
# <a name="depnx-protection"></a>DEP/NX-Schutz

Ab Windows Internet Explorer 7 unter Windows Vista enthält das Element "Internet-Systemsteuerung" die Option " **Speicherschutz aktivieren** ", um Online Angriffe zu verringern. Diese Option wird auch als *Daten Ausführungs Verhinderung (Data Execution Prevention* , DEP) oder *No-Execute* (NX) bezeichnet. Wenn diese Option aktiviert ist, funktioniert Sie mit dem Prozessor, um Pufferüberlauf Angriffe durch Blockieren der Codeausführung aus dem Arbeitsspeicher zu verhindern, der als nicht ausführbare Datei markiert ist.

In Windows Internet Explorer 8 unter dem Betriebssystem Windows Vista mit Service Pack 1 (SP1) oder einer höheren Version ist diese Option standardmäßig aktiviert. DEP/NX schützt nicht vor allen Speicher basierten Sicherheitsrisiken. Wenn Sie jedoch mit anderen Technologien wie Address Space Layout Randomization (ASLR) kombiniert werden, hilft Sie dabei, häufige Sicherheitsrisiken für Pufferüberlauf in Windows Internet Explorer und die von ihr Auslastungen zu vermeiden. Es ist keine zusätzliche Benutzerinteraktion erforderlich, um diesen Schutz zu gewährleisten, und es werden keine neuen Eingabe Aufforderungen eingeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



