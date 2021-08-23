---
description: Fügen Sie der CustomAction-Tabelle einen Datensatz für die benutzerdefinierte Aktion Starten hinzu.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Hinzufügen von Launch zu CustomAction und Binärtabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b362259f2ee336a540f396dc05f7745cbc3fde8fb44b8a1c06dabbd6247ba05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145963"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Hinzufügen von Launch zu CustomAction und Binärtabellen

Fügen Sie der [CustomAction-Tabelle](customaction-table.md) einen Datensatz für die benutzerdefinierte Aktion Starten hinzu. Geben Sie den Namen der benutzerdefinierten Aktion in der Spalte Aktion der Tabelle CustomAction ein. Geben Sie den numerischen Gesamttyp für Launch(65) in die Spalte Type (Typ) der Tabelle Custom action (Benutzerdefinierte Aktion) ein. Die Source -Spalte der CustomAction-Tabelle gibt einen Schlüssel im Datensatz der [Binärtabelle](binary-table.md) an, der die Binärdaten für die DLL enthält. Geben Tutorial.dll in die Spalte Quelle der CustomAction-Tabelle ein. Der im Feld Ziel der CustomAction-Tabelle angegebene Einstiegspunkt muss mit dem aus der DLL exportierten übereinstimmen. Geben Sie LaunchTutorial in die Spalte Ziel der CustomAction-Tabelle ein.

[CustomAction-Tabelle](customaction-table.md)



| Aktion | type | `Source`       | Ziel         |
|--------|------|--------------|----------------|
| Starten | 65   | Tutorial.dll | LaunchTutorial |



 

Fügen Sie den Tutorial.dll, den Sie aus Tutorial.cpp erstellt haben, als binären Stream zur Binary-Tabelle hinzu.

[Binäre Tabelle](binary-table.md)



| Name         | Daten                          |
|--------------|-------------------------------|
| Tutorial.dll | {*binäre Daten für DLL hinzugefügt*} |



 

Fahren Sie [mit Hinzufügen eines Steuerelementereignis am Ende der Installation fort, um zu starten.](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



