---
description: Arbeitsspeicher, der zu einem Prozess gehört, wird implizit durch seinen privaten virtuellen Adressraum geschützt.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Arbeitsspeicherschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4421b07ee4ed88dffe0e46d1121d5d4117b471a84ffcf4f85738bd8be912f09c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809069"
---
# <a name="memory-protection"></a>Arbeitsspeicherschutz

Arbeitsspeicher, der zu einem Prozess gehört, wird implizit durch seinen privaten virtuellen Adressraum geschützt. Darüber hinaus bietet Windows Speicherschutz mithilfe der virtuellen Arbeitsspeicherhardware. Die Implementierung dieses Schutzes variiert je nach Prozessor, z. B. können Codepages im Adressraum eines Prozesses als schreibgeschützt markiert und vor Änderungen durch Benutzermodusthreads geschützt werden.

Die vollständige Liste der Attribute finden Sie unter [Speicherschutzkonstanten.](memory-protection-constants.md)

## <a name="copy-on-write-protection"></a>Kopierschutz bei Schreibzugriff

Der Kopierschutz beim Schreiben ist eine Optimierung, die es mehreren Prozessen ermöglicht, ihre virtuellen Adressräume so zuzuordnen, dass sie eine physische Seite freigeben, bis einer der Prozesse die Seite ändert. Dies ist Teil einer Technik namens *verzögerte Auswertung,* die es dem System ermöglicht, physischen Speicher und Zeit zu sparen, indem ein Vorgang erst ausgeführt wird, wenn dies unbedingt erforderlich ist.

Angenommen, zwei Prozesse laden Seiten aus derselben DLL in ihre virtuellen Speicherplätze. Diese Seiten des virtuellen Arbeitsspeichers werden den gleichen physischen Speicherseiten für beide Prozesse zugeordnet. Solange keiner der Prozesse auf diese Seiten schreibt, können sie die gleichen physischen Seiten zuordnen und freigeben, wie im folgenden Diagramm dargestellt.

![Felder und Pfeile der Prozessseiten 1 und 2, die demselben physischen Speicher zugeordnet sind](images/mem1.png)

Wenn Prozess 1 auf eine dieser Seiten schreibt, wird der Inhalt der physischen Seite auf eine andere physische Seite kopiert, und die Zuordnung des virtuellen Arbeitsspeichers wird für Prozess 1 aktualisiert. Beide Prozesse verfügen jetzt über eine eigene Instanz der Seite im physischen Speicher. Daher ist es nicht möglich, dass ein Prozess auf eine freigegebene physische Seite schreibt und der andere Prozess die Änderungen sieht.

![Felder und Pfeile von Prozessen und Neuzuordnung des physischen Speichers](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Laden von Anwendungen und DLLs

Wenn mehrere Instanzen derselben Windows-basierten Anwendung geladen werden, wird jede Instanz in ihrem eigenen geschützten virtuellen Adressraum ausgeführt. Ihre Instanzhandles (*hInstance*) haben jedoch in der Regel den gleichen Wert. Dieser Wert stellt die Basisadresse der Anwendung im virtuellen Adressraum dar. Wenn jede Instanz in ihre Standardbasisadresse geladen werden kann, kann sie mithilfe des Kopier-bei-Schreib-Schutzes denselben physischen Seiten zugeordnet und für die anderen Instanzen freigegeben werden. Das System ermöglicht es diesen Instanzen, die gleichen physischen Seiten freizugeben, bis eine von ihnen eine Seite ändert. Wenn eine dieser Instanzen aus irgendeinem Grund nicht in die gewünschte Basisadresse geladen werden kann, erhält sie eigene physische Seiten.

DLLs werden mit einer Standardbasisadresse erstellt. Jeder Prozess, der eine DLL verwendet, versucht, die DLL in ihrem eigenen Adressraum an der virtuellen Standardadresse für die DLL zu laden. Wenn mehrere Anwendungen eine DLL an ihrer virtuellen Standardadresse laden können, können sie die gleichen physischen Seiten für die DLL freigeben. Wenn ein Prozess die DLL aus irgendeinem Grund nicht an der Standardadresse laden kann, lädt er die DLL an einen anderen Ort. Der Kopierschutz bei Schreibzugriff erzwingt, dass einige der DLL-Seiten für diesen Prozess auf verschiedene physische Seiten kopiert werden, da die Fehlerbehebungen für Sprunganweisungen auf den Seiten der DLL geschrieben werden und für diesen Prozess unterschiedlich sind. Wenn der Codeabschnitt viele Verweise auf den Datenabschnitt enthält, kann dies dazu führen, dass der gesamte Codeabschnitt auf neue physische Seiten kopiert wird.

 

 



