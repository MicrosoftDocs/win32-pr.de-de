---
description: Microsoft stellt das MSV1 \_ 0-Authentifizierungs Paket für Anmeldungen auf lokalen Computern bereit, für die keine benutzerdefinierte Authentifizierung erforderlich ist.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 Authentifizierungs Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217323"
---
# <a name="msv1_0-authentication-package"></a>MSV1 \_ 0-Authentifizierungs Paket

Microsoft stellt das MSV1 \_ 0- [*Authentifizierungs Paket*](../secgloss/a-gly.md) für Anmeldungen auf lokalen Computern bereit, für die keine benutzerdefinierte Authentifizierung erforderlich ist. Die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) Ruft das \_ Authentifizierungs Paket MSV1 0 auf, um von der [*Gina*](../secgloss/g-gly.md) für den Anmeldevorgang von [*Windows*](../secgloss/w-gly.md) gesammelte Anmeldedaten zu verarbeiten. Das \_ Paket MSV1 0 überprüft die SAM-Datenbank (Local Security Accounts Manager), um zu bestimmen, ob die Anmeldedaten zu einem gültigen [*Sicherheits Prinzipal*](../secgloss/s-gly.md) gehören, und gibt dann das Ergebnis des Anmelde Versuchs an die LSA zurück.

MSV1 \_ 0 unterstützt auch Domänen Anmeldungen. MSV1 \_ 0 verarbeitet Domänen Anmeldungen mithilfe der Passthrough-Authentifizierung, wie in der folgenden Abbildung dargestellt.

![MSV1 \- 0-Authentifizierungs Paket](images/lsaint4.png)

Bei der Passthrough-Authentifizierung verwendet die lokale Instanz von MSV1 \_ 0 den Anmeldedienst, um die Instanz von MSV1 0 aufzurufen, die \_ auf dem Domänen Controller ausgeführt wird. Die Instanz von MSV1 0 des Domänen Controllers \_ überprüft dann die SAM-Datenbank des Domänen Controllers und gibt das Anmelde Ergebnis an die Instanz von MSV1 \_ 0 auf dem lokalen Computer zurück. Die lokale Version von MSV1 \_ 0 leitet das Anmelde Ergebnis an die Instanz der LSA auf dem lokalen Computer weiter.

Wenn der Domänen Controller nicht verfügbar ist und die LSA zwischengespeicherte [*Anmelde*](../secgloss/c-gly.md) Informationen für den Benutzer enthält, kann die lokale Instanz von MSV1 \_ 0 den Benutzer mithilfe der zwischengespeicherten Anmeldedaten authentifizieren.

Das \_ Authentifizierungs Paket MSV1 0 unterstützt auch [unter Authentifizierungs Pakete](subauthentication-packages.md). Ein unter Authentifizierungs Paket ist eine DLL, die einen Teil der Authentifizierungs-und Validierungs Kriterien ersetzen kann, die vom MSV1 \_ 0-Authentifizierungs Paket verwendet werden.

Das MSV1 \_ 0-Authentifizierungs Paket definiert ein Schlüssel-Wert-Paar für [*primär Anmelde*](../secgloss/p-gly.md) Informationen. Die primäre Anmelde Informations Zeichenfolge enthält die Anmelde Informationen, die von den zur Anmeldezeit angegebenen Daten abgeleitet werden. Sie enthält den Benutzernamen und sowohl die Groß-/Kleinschreibung als auch die Groß-/Kleinschreibung für das Kennwort des Benutzers.

 

 
