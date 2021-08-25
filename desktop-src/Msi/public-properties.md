---
description: Öffentliche Eigenschaften können in der Installationsdatenbank auf die gleiche Weise wie private Eigenschaften erstellt werden.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Öffentliche Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0138db2fcbe664ac9a4064379486c42c3d52a6896fc53a608b99192a8d70c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828430"
---
# <a name="public-properties"></a>Öffentliche Eigenschaften

Öffentliche Eigenschaften können in der Installationsdatenbank auf die gleiche Weise wie [private Eigenschaften](private-properties.md)erstellt werden. Darüber hinaus können die Werte öffentlicher Eigenschaften von einem Benutzer oder Systemadministrator geändert werden, indem die -Eigenschaft in der Befehlszeile festgelegt wird, indem eine Transformation angewendet oder mit einer benutzerdefinierten Benutzeroberfläche interagiert wird. Öffentliche Eigenschaftennamen dürfen keine Kleinbuchstaben enthalten. Weitere Informationen finden Sie unter [Einschränkungen für Eigenschaftsnamen.](restrictions-on-property-names.md)

Öffentliche Eigenschaften werden häufig von Benutzern während der Installation festgelegt. Beispielsweise kann die öffentliche Eigenschaft [**INSTALLLEVEL**](installlevel.md) in der Befehlszeile angegeben werden, die zum Starten der Installation verwendet wird, oder sie kann mithilfe einer benutzerdefinierten Benutzeroberfläche ausgewählt werden.

Öffentliche Eigenschaftswerte können entweder über eine Befehlszeile, mithilfe einer [Standardaktion](standard-actions.md) oder einer [benutzerdefinierten](custom-actions.md) Aktion, durch Anwenden einer Transformation oder durch Interaktion des Benutzers mit einer benutzerdefinierten Benutzeroberfläche überschrieben werden. Um eine öffentliche Eigenschaft in der Eigenschaftentabelle zu löschen, lassen Sie sie aus der Tabelle weg. Eigenschaften, die während der Installation von der Benutzeroberfläche festgelegt und dann an die Ausführungsphase der Installation übergeben werden sollen, müssen öffentlich sein.

Eine Liste der öffentlichen Standardeigenschaften, die vom Installationsprogramm verwendet werden, finden Sie unter [Eigenschaftenreferenz.](property-reference.md) Ein Autor kann auch eine benutzerdefinierte öffentliche Eigenschaft definieren, indem er den Namen der Eigenschaft und einen Anfangswert in die [Property-Tabelle](property-table.md)eingibt. Alle öffentlichen Eigenschaften können von allen Benutzern überschrieben werden, wenn eine der folgenden Bedingungen zutrifft.

-   Der Benutzer ist ein Systemadministrator.
-   Die Richtlinie EnableUserControl pro Computer ist auf 1 festgelegt. Weitere Informationen finden Sie unter [Systemrichtlinie.](system-policy.md)
-   Die [**EnableUserControl-Eigenschaft**](-enableusercontrol.md) ist auf 1 festgelegt.
-   Dies ist eine nicht verwaltete Installation, die nicht mit erhöhten Rechten ausgeführt wird.

Wenn keine der oben genannten Bedingungen zutrifft, beschränkt das Installationsprogramm standardmäßig, welche öffentlichen Eigenschaften von einem Benutzer außer Kraft gesetzt werden können, der kein Systemadministrator ist. Weitere Informationen finden Sie unter [**Eingeschränkte öffentliche Eigenschaften.**](restricted-public-properties.md)

 

 



