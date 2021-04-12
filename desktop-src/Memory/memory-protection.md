---
description: Arbeitsspeicher, der zu einem Prozess gehört, wird implizit durch den privaten virtuellen Adressraum geschützt.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Arbeitsspeicherschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30df8084c91a62c28414f4a8142397ee777e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132036"
---
# <a name="memory-protection"></a>Arbeitsspeicherschutz

Arbeitsspeicher, der zu einem Prozess gehört, wird implizit durch den privaten virtuellen Adressraum geschützt. Außerdem bietet Windows Speicherschutz mithilfe der Hardware des virtuellen Speichers an. Die Implementierung dieses Schutzes variiert je nach Prozessor, z. b. können Codepages im Adressraum eines Prozesses als schreibgeschützt gekennzeichnet und vor Änderungen durch benutzermodusthreads geschützt werden.

Eine umfassende Liste der Attribute finden Sie unter [Speicherschutz Konstanten](memory-protection-constants.md).

## <a name="copy-on-write-protection"></a>Copy-on-Write-Schutz

Der Kopier-/Schreibschutz ist eine Optimierung, die es mehreren Prozessen ermöglicht, Ihre virtuellen Adressräume so zuzuordnen, dass Sie eine physische Seite gemeinsam verwenden, bis einer der Prozesse die Seite ändert. Dies ist Teil einer Technik namens " *Lazy Evaluation*", die es dem System ermöglicht, physischen Arbeitsspeicher und Zeit zu sparen, indem Sie einen Vorgang erst ausführen, wenn dies unbedingt erforderlich ist.

Nehmen Sie beispielsweise an, dass zwei Prozesse Seiten aus derselben DLL in Ihre virtuellen Speicherplätze laden. Diese virtuellen Speicherseiten werden den gleichen physischen Speicherseiten für beide Prozesse zugeordnet. Solange keine Prozesse auf diese Seiten schreiben, können Sie die gleichen physischen Seiten zuordnen und freigeben, wie im folgenden Diagramm dargestellt.

![Felder und Pfeile von Prozess 1 und 2 Seiten, die demselben physischen Speicher zugeordnet sind](images/mem1.png)

Wenn Prozess 1 auf eine dieser Seiten schreibt, wird der Inhalt der physischen Seite auf eine andere physische Seite kopiert, und die virtuelle Arbeitsspeicher Zuordnung wird für Prozess 1 aktualisiert. Beide Prozesse verfügen nun über eine eigene Instanz der Seite im physischen Arbeitsspeicher. Daher ist es nicht möglich, dass ein Prozess auf eine freigegebene physische Seite schreibt und der andere Prozess die Änderungen sieht.

![Felder und Pfeile von Prozessen und Neuzuordnung physischer Speicher](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Laden von Anwendungen und DLLs

Wenn mehrere Instanzen derselben Windows-basierten Anwendung geladen werden, wird jede Instanz in einem eigenen geschützten virtuellen Adressbereich ausgeführt. Ihre Instanzhandles (*HINSTANCE*) weisen jedoch in der Regel den gleichen Wert auf. Dieser Wert stellt die Basisadresse der Anwendung im virtuellen Adressraum dar. Wenn jede Instanz in die Standardbasis Adresse geladen werden kann, kann Sie mithilfe von Copy-on-Write-Schutz die gleichen physischen Seiten mit den anderen Instanzen zuordnen und freigeben. Das System ermöglicht es diesen Instanzen, die gleichen physischen Seiten gemeinsam zu verwenden, bis einer von Ihnen eine Seite ändert. Wenn eine dieser Instanzen aus irgendeinem Grund nicht in die gewünschte Basisadresse geladen werden kann, erhält Sie Ihre eigenen physischen Seiten.

DLLs werden mit einer Standardbasis Adresse erstellt. Jeder Prozess, der eine DLL verwendet, versucht, die dll in Ihrem eigenen Adressraum an der virtuellen Standardadresse für die dll zu laden. Wenn mehrere Anwendungen eine DLL an der virtuellen Standardadresse laden können, können Sie die gleichen physischen Seiten für die DLL verwenden. Wenn die dll aus irgendeinem Grund von einem Prozess nicht in der Standardadresse geladen werden kann, wird die dll an einen anderen Speicherort geladen. Bei einem Kopier-/Schreibschutz müssen einige der dll-Seiten für diesen Prozess auf verschiedene physische Seiten kopiert werden, da die Korrekturen für Jump-Anweisungen auf den Seiten der dll geschrieben werden und für diesen Prozess unterschiedlich sind. Wenn der Code Abschnitt viele Verweise auf den Daten Abschnitt enthält, kann dies dazu führen, dass der gesamte Code Abschnitt auf neue physische Seiten kopiert wird.

 

 



