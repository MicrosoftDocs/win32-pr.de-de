---
description: Eine Anmeldesitzung ist eine Computersitzung, die beginnt, wenn eine Benutzerauthentifizierung erfolgreich ist, und endet, wenn sich der Benutzer vom System abmeldet.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: LSA-Anmeldesitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4bc6adc81b22b0e48a83b8aec4f9130b1fcb906bea5078afc6517563c98b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922325"
---
# <a name="lsa-logon-sessions"></a>LSA-Anmeldesitzungen

Eine [*Anmeldesitzung ist*](../secgloss/l-gly.md) eine Computersitzung, die beginnt, wenn eine Benutzerauthentifizierung erfolgreich ist, und endet, wenn sich der Benutzer vom System abmeldet.

Wenn ein Benutzer erfolgreich authentifiziert wurde, erstellt das Authentifizierungspaket eine Anmeldesitzung und gibt Informationen [](../secgloss/t-gly.md) an die lokale Sicherheitsstelle [](../secgloss/l-gly.md) (LSA) zurück, die zum Erstellen eines Tokens für den neuen Benutzer verwendet wird. Dieses Token enthält unter anderem [](../secgloss/l-gly.md) einen lokal eindeutigen Bezeichner (LUID) für die Anmeldesitzung, der als [*Anmelde-ID bezeichnet wird.*](../secgloss/l-gly.md)

Wenn ein Token erstellt wird, wird [*die Verweisanzahl*](../secgloss/r-gly.md) für die Anmeldesitzung erhöht. Die Verweisanzahl wird auch erhöht, wenn Kopien des Tokens für die Prozesserstellung, den Identitätswechsel oder andere Verwendungszwecke erstellt werden. Wenn Token verwendet werden und Kopien des Tokens gelöscht werden, wird die Verweisanzahl für die Anmeldesitzung dekrementiert. Wenn die Verweisanzahl 0 (null) erreicht, wird die Anmeldesitzung gelöscht.

> [!Note]  
> Wenn die Authentifizierung nicht erfolgreich ist, sollte das [*Authentifizierungspaket*](../secgloss/a-gly.md) keine Anmeldesitzung erstellen. Wenn das Authentifizierungspaket eine Anmeldesitzung erstellen muss, bevor die Gültigkeit des Benutzers endgültig bestimmt wird, und wenn die Authentifizierung fehlschlägt, muss das Authentifizierungspaket die Sitzung löschen.

 

 

 
