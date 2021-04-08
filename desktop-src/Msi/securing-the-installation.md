---
description: Fügen Sie alle Kenn Wort Eigenschaften aus der Tabelle customuseraccounts der Eigenschaft msihiddenproperties in der Eigenschaften Tabelle hinzu.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sichern der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960920"
---
# <a name="securing-the-installation"></a>Sichern der Installation

Fügen Sie alle Kenn Wort Eigenschaften aus der Tabelle customuseraccounts der Eigenschaft [**msihiddenproperties**](msihiddenproperties.md) in der Eigenschaften [Tabelle](property-table.md)hinzu. Fügen Sie die Namen der verzögerten benutzerdefinierten Aktionen ebenfalls der **msihiddenproperties** -Eigenschaft hinzu. Dadurch wird verhindert, dass das Installationsprogramm die sensiblen Eigenschaftswerte (die Kenn Wörter) in das Protokoll schreibt, und sicherstellen, dass diese Werte nicht protokolliert werden, wenn die verzögerten benutzerdefinierten Aktionen die Werte als customaktiondata-Eigenschaft verwenden.

Damit das Kennwort des Benutzers im Windows Installer-Dienst verfügbar ist, muss die Password-Eigenschaft der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft hinzugefügt werden.

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft                                                 | Wert                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**Msihiddenproperties**](msihiddenproperties.md)       | Testuserpassword; "Kreateaccount;" RemoveAccount Rollbackaccount |
| [**Securecustomproperties**](securecustomproperties.md) | Testuserpassword                                             |



 

Dies schließt das Beispiel ab.

 

 



