---
description: Fügen Sie alle Password-Eigenschaften aus der Tabelle CustomUserAccounts der MsiHiddenProperties-Eigenschaft in der Property-Tabelle hinzu.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sichern der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642170cc2ac4e84bebe5235e84328abe5039ede1bdb8fc2760bbd249ff5268de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040730"
---
# <a name="securing-the-installation"></a>Sichern der Installation

Fügen Sie alle Kennworteigenschaften aus der Tabelle CustomUserAccounts der [**MsiHiddenProperties-Eigenschaft**](msihiddenproperties.md) in der [Property-Tabelle hinzu.](property-table.md) Fügen Sie der **MsiHiddenProperties-Eigenschaft** auch die Namen der zurückgestellten benutzerdefinierten Aktionen hinzu. Dadurch wird verhindert, dass das Installationsprogramm die vertraulichen Eigenschaftswerte (kennwörter) in das Protokoll schreibt, und stellt sicher, dass diese Werte nicht protokolliert werden, wenn die verzögerten benutzerdefinierten Aktionen die Werte als CustomActionData-Eigenschaft verwenden.

Damit das Kennwort des Benutzers im Windows Installer-Dienst verfügbar ist, muss die Kennworteigenschaft der [**SecureCustomProperties-Eigenschaft hinzugefügt**](securecustomproperties.md) werden.

[Eigenschaftentabelle](property-table.md)



| Eigenschaft                                                 | Wert                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount; RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Damit ist das Beispiel beendet.

 

 



