---
description: Öffentliche Eigenschaften können auf die gleiche Weise wie private Eigenschaften in der Installations Datenbank erstellt werden.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Öffentliche Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864855"
---
# <a name="public-properties"></a>Öffentliche Eigenschaften

Öffentliche Eigenschaften können auf die gleiche Weise wie [private Eigenschaften](private-properties.md)in der Installations Datenbank erstellt werden. Außerdem können die Werte öffentlicher Eigenschaften von einem Benutzer oder Systemadministrator geändert werden, indem die-Eigenschaft in der Befehlszeile, durch Anwenden einer Transformation oder durch Interaktion mit einer erstellten Benutzeroberfläche festgelegt wird. Öffentliche Eigenschaftsnamen dürfen keine Kleinbuchstaben enthalten. Siehe [Einschränkungen für Eigenschaftsnamen](restrictions-on-property-names.md).

Öffentliche Eigenschaften werden in der Regel von Benutzern während der Installation festgelegt. So kann z. b. die Eigenschaft " [**INSTALLLEVEL**](installlevel.md) " der öffentlichen Eigenschaft in der Befehlszeile angegeben werden, mit der die Installation gestartet oder mithilfe einer erstellten Benutzeroberfläche ausgewählt wird.

Öffentliche Eigenschaftswerte können entweder in einer Befehlszeile, mithilfe einer [Standard](standard-actions.md) -oder [benutzerdefinierten](custom-actions.md) Aktion, durch Anwenden einer Transformation oder durch Interaktion des Benutzers mit einer erstellten Benutzeroberfläche überschrieben werden. Wenn Sie eine öffentliche Eigenschaft in der Eigenschaften Tabelle löschen möchten, lassen Sie Sie aus der Tabelle aus. Eigenschaften, die während der Installation von der Benutzeroberfläche festgelegt und dann an die Ausführungsphase der Installation weitergeleitet werden, müssen öffentlich sein.

Eine Liste der öffentlichen Standardeigenschaften, die vom Installationsprogramm verwendet werden, finden Sie unter [Eigenschafts Referenz](property-reference.md). Ein Autor kann auch eine benutzerdefinierte öffentliche Eigenschaft definieren, indem er den Eigenschaftsnamen und einen Anfangswert in die [Eigenschaften Tabelle](property-table.md)eingegeben hat. Alle öffentlichen Eigenschaften können von allen Benutzern überschrieben werden, wenn eine der folgenden Bedingungen zutrifft.

-   Der Benutzer ist ein Systemadministrator.
-   Die pro-Computer-enableusercontrol-Richtlinie ist auf 1 festgelegt. Siehe [System Richtlinie](system-policy.md).
-   Die [**enableusercontrol**](-enableusercontrol.md) -Eigenschaft ist auf 1 festgelegt.
-   Dies ist eine nicht verwaltete Installation, die nicht mit erhöhten Rechten ausgeführt wird.

Wenn keine der oben genannten Bedingungen zutrifft, schränkt der Installer standardmäßig ein, welche öffentlichen Eigenschaften von einem Benutzer, der kein Systemadministrator ist, überschrieben werden können. Siehe [**Eingeschränkte öffentliche Eigenschaften**](restricted-public-properties.md).

 

 



