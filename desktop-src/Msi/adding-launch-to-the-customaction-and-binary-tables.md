---
description: Fügen Sie der Tabelle CustomAction einen Datensatz für die Aktion benutzerdefinierte Aktion starten hinzu.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Hinzufügen von Start zu den Tabellen CustomAction und Binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131505"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Hinzufügen von Start zu den Tabellen CustomAction und Binary

Fügen Sie der [Tabelle CustomAction](customaction-table.md) einen Datensatz für die Aktion benutzerdefinierte Aktion starten hinzu. Geben Sie den Namen der benutzerdefinierten Aktion in der Spalte Aktion der Tabelle CustomAction ein. Geben Sie den gesamten numerischen Typ für Launch, 65 in die Spalte Type der Tabelle Custom Action ein. Die Quell Spalte der Tabelle CustomAction gibt einen Schlüssel in den Datensatz der [binären Tabelle](binary-table.md) an, die die Binärdaten für die dll enthält. Geben Sie Tutorial.dll in die Spalte Quelle der Tabelle CustomAction ein. Der Einstiegspunkt, der im Zielfeld der CustomAction-Tabelle angegeben ist, muss mit dem aus der DLL exportierten Eintrag identisch sein. Geben Sie launchtutorial in die Ziel Spalte der Tabelle CustomAction ein.

[Tabelle "CustomAction"](customaction-table.md)



| Aktion | type | `Source`       | Ziel         |
|--------|------|--------------|----------------|
| Starten | 65   | Tutorial.dll | Launchtutorial |



 

Fügen Sie die Tutorial.dll, die Sie aus Tutorial. cpp erstellt haben, als binären Stream zur binären Tabelle hinzu.

[Binäre Tabelle](binary-table.md)



| Name         | Daten                          |
|--------------|-------------------------------|
| Tutorial.dll | {*binäre Daten für dll-Datei hinzugefügt* |



 

Fügen Sie [am Ende der Installation ein Steuerungs Ereignis hinzu, um den Start auszuführen](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



