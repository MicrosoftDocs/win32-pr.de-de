---
description: Eine Aktion wird im Windows Installer entweder durch Aufrufen der MsiDoAction-Funktion oder durch Das Einreihen der Aktion in eine Sequenztabelle ausgeführt.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Verwenden von Standardaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60696e79c12b054739d87ffe5696e898a8eb955c4c7bfe0aa9c2341db7c2d720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996210"
---
# <a name="using-standard-actions"></a>Verwenden von Standardaktionen

Eine Aktion wird im Windows Installer entweder durch Aufrufen der [**MsiDoAction-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) oder durch Das Einreihen der Aktion in eine Sequenztabelle ausgeführt. Da die meisten Aktionen einen einzelnen Zweck kapseln, besteht die gängigste Methode zum Verwenden von Aktionen darin, eine Reihe von Aktionen in eine Sequenz zu geordnet, um eine größere Aufgabe auszuführen. Das Installationsprogramm verfügt über drei Standardaktionen der obersten Ebene, die einen zugeordneten Satz von Sequenztabellen aufrufen. Diese zugeordneten Sequenztabellen können Standardaktionen, benutzerdefinierte Aktionen und Benutzeroberflächenelemente enthalten. Jede Aktion in einer Sequenztabelle verfügt über eine zugeordnete Sequenznummer und kann auch über einen zugeordneten bedingten Ausdruck verfügen. Alle Aktionen in einer Sequenztabelle werden in der richtigen Reihenfolge besucht und nur ausgeführt, wenn der bedingte Ausdruck trueauswertet.

Einer Standardaktion kann zwar eine beliebige Sequenznummer zugeordnet sein, viele verfügen jedoch über Sequenzeinschränkungen, die befolgt werden müssen, damit die Aktion ordnungsgemäß funktioniert. Beispielsweise muss die [FileCost-Aktion](filecost-action.md)nach der [CostInitialize-Aktion aufgerufen werden.](costinitialize-action.md) Weitere Informationen zu Standardeinschränkungen für die Aktionssequenzierung finden Sie [unter](actions-with-sequencing-restrictions.md)Aktionen mit Sequenzierungseinschränkungen, Aktionen ohne Sequenzierungseinschränkungen oder Referenz zu [Standardaktionen.](standard-actions-reference.md) [](actions-without-sequencing-restrictions.md)

Die folgenden Themen enthalten weitere Informationen zur Verwendung von Standardaktionen.

-   [Veröffentlichen von Produkten, Features und Komponenten](publishing-products-features-and-components.md)
-   [Dateisuche](file-searching.md)
-   [Dateikosten](file-costing.md)
-   [Dateiinstallation](file-installation.md)
-   [Ändern der Registrierung](modifying-the-registry.md)
-   [Ausführen von Aktionen](running-actions.md)

Siehe auch [Referenz zu Standardaktionen](about-standard-actions.md) [oder Standardaktionen.](standard-actions-reference.md)

 

 



