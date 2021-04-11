---
description: Eine Anmelde Sitzung ist eine computesitzung, die beginnt, wenn eine Benutzerauthentifizierung erfolgreich ist, und endet, wenn sich der Benutzer beim System anmeldet.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: LSA-Anmelde Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217329"
---
# <a name="lsa-logon-sessions"></a>LSA-Anmelde Sitzungen

Eine [*Anmelde Sitzung*](../secgloss/l-gly.md) ist eine computesitzung, die beginnt, wenn eine Benutzerauthentifizierung erfolgreich ist, und endet, wenn sich der Benutzer beim System anmeldet.

Wenn ein Benutzer erfolgreich authentifiziert wurde, erstellt das Authentifizierungs Paket eine Anmelde Sitzung und gibt Informationen an die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) zurück, [*die zum Erstellen eines Tokens*](../secgloss/t-gly.md) für den neuen Benutzer verwendet wird. Dieses Token enthält unter anderem einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID) für die Anmelde Sitzung, die als Anmelde- [*ID*](../secgloss/l-gly.md)bezeichnet wird.

Wenn ein Token erstellt wird, wird der [*Verweis Zähler*](../secgloss/r-gly.md) für die Anmelde Sitzung inkrementiert. Der Verweis Zähler wird auch immer dann erhöht, wenn Kopien des Tokens für die Prozesserstellung, den Identitätswechsel oder andere Verwendungszwecke erstellt werden. Wenn tokenverwendungen abgeschlossen sind und Kopien des Tokens gelöscht werden, wird der Verweis Zähler für die Anmelde Sitzung dekrementiert. Wenn der Verweis Zähler Null erreicht, wird die Anmelde Sitzung gelöscht.

> [!Note]  
> Wenn die Authentifizierung nicht erfolgreich ist, sollte das [*Authentifizierungs Paket*](../secgloss/a-gly.md) keine Anmelde Sitzung erstellen. Wenn das Authentifizierungs Paket eine Anmelde Sitzung erstellen muss, bevor die Gültigkeit des Benutzers bestimmt wird, und wenn die Authentifizierung fehlschlägt, muss das Authentifizierungs Paket die Sitzung löschen.

 

 

 
