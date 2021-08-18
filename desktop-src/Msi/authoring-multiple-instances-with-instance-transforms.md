---
description: Um mehrere Instanzen eines Produkts aus einem Windows Installer-Paket zu installieren, müssen Sie ein Basisinstallationspaket für das Produkt und eine Instanztransformation für jede Instanz erstellen, die zusätzlich zur Basisinstanz installiert werden soll.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Erstellen mehrerer Instanzen mit Instanztransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efac957d5e0e82665cb1ba20aeb42fe9b60293699c5c3fd97f5e6a6f1abf58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745910"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Erstellen mehrerer Instanzen mit Instanztransformationen

Um mehrere Instanzen eines Produkts aus einem Windows Installer-Paket zu installieren, müssen Sie ein Basisinstallationspaket für das Produkt und eine Instanztransformation für jede Instanz erstellen, die zusätzlich zur Basisinstanz installiert werden soll. Befolgen Sie die folgenden Richtlinien, wenn Sie Ihr Basispaket und Ihre Transformationen erstellen:

-   Ihre Setupanwendung kann überprüfen, ob das Installationsprogramm unter einer Version von Windows Vista, Windows Server 2003, Windows XP mit Service Pack 1 (SP1) und dem Windows Installer 3.0 redistributable ausgeführt wird. Eine dieser Installationsprogrammversionen (oder höher) ist erforderlich, um mehrere Instanzen aus einem einzelnen Paket mithilfe einer Transformation zum Ändern des Produktcodes zu installieren.
-   Jede Instanz muss über einen eindeutigen Produktcode und instanzbezeichner verfügen. Sie können eine Eigenschaft im Basispaket definieren, deren Wert auf den Instanzbezeichner festgelegt werden kann.
-   Um die Dateien jeder Instanz isoliert zu halten, sollte das Basispaket Dateien an einem Verzeichnisspeicherort installieren, der vom Instanzbezeichner abhängt.
-   Um die Nichtdateidaten jeder Instanz isoliert zu halten, sollte das Basispaket Nichtdateidaten in Komponentensätzen für jede Instanz sammeln. Die entsprechenden Komponenten sollten dann basierend auf bedingten Anweisungen installiert werden, die vom Instanzbezeichner abhängen.
-   Erstellen Sie eine Instanztransformation für jede Instanz, die zusätzlich zur Basisinstanz installiert wird. Das Basispaket kann eine eigene Instanz installieren.
-   Die Instanztransformation muss den Produktcode und den Bezeichner für jede Instanz ändern.
-   Es wird empfohlen, dass die Produkttransformation auch den Produktnamen ändert, sodass die Instanz unter Software über Systemsteuerung leicht unterschieden werden kann.
-   Wenn die Instanztransformation Dateien installiert, sollten sie in einem Verzeichnis installiert werden, das vom Instanzbezeichner abhängt.
-   Alle Nichtdateidaten, z. B. Registrierungsschlüssel, sollten den Instanznamen in ihrem Pfad enthalten, um Konflikte zu verhindern. Dies kann mithilfe der -Eigenschaft erreicht werden, deren Wert der Instanzbezeichner im Pfad ist, wie im folgenden Beispiel einer [Registrierungstabelle](registry-table.md)gezeigt.



| Registrierung | Root | Schlüssel                                            | Name         | Wert           | Komponente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft \\ MyProduct \\ \[ InstanceId\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches und](installing-multiple-instances-of-products-and-patches.md) Installieren mehrerer Instanzen mit [Instanztransformationen.](installing-multiple-instances-with-instance-transforms.md)

 

 



