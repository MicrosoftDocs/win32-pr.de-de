---
description: Um mehrere Instanzen eines Produkts von einem Windows Installer Paket zu installieren, müssen Sie ein Basis Installationspaket für das Produkt und eine instanztransformation für jede zu installierende Instanz zusätzlich zur-Basis Instanz erstellen.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Erstellen mehrerer Instanzen mit instanztransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367883"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Erstellen mehrerer Instanzen mit instanztransformationen

Um mehrere Instanzen eines Produkts von einem Windows Installer Paket zu installieren, müssen Sie ein Basis Installationspaket für das Produkt und eine instanztransformation für jede zu installierende Instanz zusätzlich zur-Basis Instanz erstellen. Beachten Sie beim Erstellen des Basispakets und der Transformationen die folgenden Richtlinien:

-   Ihre Setup Anwendung kann prüfen, ob das Installationsprogramm unter einer Version von Windows Vista, Windows Server 2003, Windows XP mit Service Pack 1 (SP1) und dem Windows Installer 3,0 Redistributable ausgeführt wird. Jede dieser Installer-Versionen (oder höher) ist erforderlich, um mehrere Instanzen von einem einzelnen Paket zu installieren, indem ein Product Code – Changing Transform verwendet wird.
-   Jede Instanz muss über einen eindeutigen Produktcode und einen eindeutigen Instanzbezeichner verfügen. Sie können eine Eigenschaft im Basispaket definieren, deren Wert auf den Instanzbezeichner festgelegt werden kann.
-   Damit die Dateien der einzelnen Instanzen isoliert bleiben, sollte das Basispaket Dateien in einem Verzeichnis Speicherort installieren, der vom Instanzbezeichner abhängig ist.
-   Damit die nicht-Datei Daten der einzelnen Instanzen isoliert bleiben, sollte das Basispaket nicht-Datei Daten in Gruppen von Komponenten für jede Instanz erfassen. Die entsprechenden Komponenten sollten dann basierend auf bedingten Anweisungen installiert werden, die vom Instanzbezeichner abhängen.
-   Erstellen Sie eine instanztransformation für jede Instanz, die zusätzlich zur-Basis Instanz installiert wird. Das Basispaket kann seine eigene Instanz installieren.
-   Die instanztransformation muss den Produktcode und den Bezeichner für jede Instanz ändern.
-   Es wird empfohlen, dass die Product Transform auch den Produktnamen ändert, sodass die Instanz in der Systemsteuerung unter Software leicht unterschieden werden kann.
-   Wenn die instanztransformation Dateien installiert, sollten Sie in einem Verzeichnis installiert werden, das vom Instanzbezeichner abhängt.
-   Alle nicht-Datei Daten, wie z. b. Registrierungsschlüssel, müssen den Instanznamen in ihren Pfad einschließen, um Konflikte zu verhindern. Dies kann erreicht werden, indem die-Eigenschaft verwendet wird, deren Wert der Instanzbezeichner im Pfad ist, wie im folgenden Beispiel einer [Registrierungs Tabelle](registry-table.md)gezeigt.



| Registrierung | Root | Schlüssel                                            | Name         | Wert           | Komponente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft \\ MyProduct \\ \[ InstanceId\] | GUID | \[ProductCode\] | NonFileDataComp1 |



 

Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md) und [Installieren mehrerer Instanzen mit instanztransformationen](installing-multiple-instances-with-instance-transforms.md).

 

 



