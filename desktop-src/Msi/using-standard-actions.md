---
description: Eine Aktion wird in der Windows Installer ausgeführt, indem entweder die msidoaction-Funktion aufgerufen oder die Aktion in einer Sequenz Tabelle eingeschlossen wird.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Verwenden von Standard Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360173"
---
# <a name="using-standard-actions"></a>Verwenden von Standard Aktionen

Eine Aktion wird in der Windows Installer ausgeführt, indem entweder die [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion aufgerufen oder die Aktion in einer Sequenz Tabelle eingeschlossen wird. Da die meisten Aktionen einen einzigen Zweck Kapseln, besteht die gängigste Methode zum Verwenden von Aktionen darin, eine Reihe von Aktionen in einer Sequenz zu sortieren, um eine größere Aufgabe zu erledigen. Das Installationsprogramm verfügt über drei Standard Aktionen auf oberster Ebene, die einen zugeordneten Satz von Sequenz Tabellen aufzurufen. Diese zugeordneten Sequenz Tabellen können Standard Aktionen, benutzerdefinierte Aktionen und Benutzeroberflächen Elemente enthalten. Jede Aktion in einer Sequenz Tabelle verfügt über eine zugeordnete Sequenznummer und kann auch über einen zugeordneten bedingten Ausdruck verfügen. Alle Aktionen in einer Sequenz Tabelle werden in der angegebenen Reihenfolge besucht und nur ausgeführt, wenn der bedingte Ausdruck true ergibt.

Während einer Standardaktion eine beliebige Sequenznummer zugeordnet werden kann, haben viele Sequenz Beschränkungen, die befolgt werden müssen, damit die Aktion ordnungsgemäß funktioniert. Beispielsweise muss die [filecost-Aktion](filecost-action.md)nach der [costinitialize-Aktion](costinitialize-action.md)aufgerufen werden. Weitere Informationen zu den standardmäßigen Aktions Sequenz Beschränkungen finden Sie unter [Aktionen mit Sequenz Einschränkungen](actions-with-sequencing-restrictions.md), [Aktionen ohne Sequenz Beschränkungen](actions-without-sequencing-restrictions.md)oder [Referenz zu Standard Aktionen](standard-actions-reference.md).

Die folgenden Themen enthalten weitere Informationen zur Verwendung von Standard Aktionen.

-   [Veröffentlichen von Produkten, Features und Komponenten](publishing-products-features-and-components.md)
-   [Dateisuche](file-searching.md)
-   [Datei Kosten](file-costing.md)
-   [Datei Installation](file-installation.md)
-   [Ändern der Registrierung](modifying-the-registry.md)
-   [Ausführen von Aktionen](running-actions.md)

Weitere Informationen finden Sie unter [Standard Aktionen](about-standard-actions.md) oder [Referenz zu Standard Aktionen](standard-actions-reference.md).

 

 



