---
description: Die Authentifizierung erfolgt interaktiv, wenn ein Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird. Die lokale Sicherheits Autorität (Local Security Authority, LSA) führt eine interaktive Authentifizierung aus, wenn sich ein Benutzer über die Gina-Benutzeroberfläche anmeldet.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Interaktive Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348059"
---
# <a name="interactive-authentication"></a>Interaktive Authentifizierung

Die Authentifizierung erfolgt interaktiv, wenn ein Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird. Die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) führt eine interaktive Authentifizierung aus, wenn sich ein Benutzer über die [*Gina*](../secgloss/g-gly.md) -Benutzeroberfläche anmeldet. Die folgende Abbildung zeigt die Teile einer typischen interaktiven Authentifizierung.

![interaktive Authentifizierung](images/lsaint3.png)

Ein Benutzer signalisiert dem System, die Anmelde Sequenz zu starten, indem er die Tastenkombination STRG + ALT + ENTF ( [*Secure Attention Sequence*](../secgloss/s-gly.md) , SAS) eingibt. [*Winlogon*](../secgloss/w-gly.md) empfängt die SAS und ruft die Gina auf, um eine Benutzeroberfläche anzuzeigen und die Anmeldedaten des Benutzers zu erhalten, z. b. einen Benutzernamen und ein Kennwort.

Nachdem Sie die Anmeldedaten erhalten haben, ruft die Gina die [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) -Funktion auf, um den Benutzer zu authentifizieren. dabei wird angegeben, welches Authentifizierungs Paket zum Auswerten der Anmeldedaten verwendet werden muss.

Der LSA Ruft das angegebene Authentifizierungs Paket auf und übergibt die Anmeldedaten an das Paket. Das Authentifizierungs Paket überprüft die Daten und ermittelt, ob die Authentifizierung erfolgreich war. Das Authentifizierungs Ergebnis wird an die LSA und von der LSA an die Gina zurückgegeben.

Die Gina zeigt den Erfolg oder das Fehlschlagen der Authentifizierung für den Benutzer an und gibt das Ergebnis der Authentifizierung an Winlogon zurück. Wenn die Authentifizierung erfolgreich ist, beginnt die Anmelde Sitzung des Benutzers, und es wird ein Satz [*von Anmelde Informationen*](../secgloss/c-gly.md) für die spätere Referenz gespeichert.

> [!Note]  
> Im Allgemeinen müssen Entwickler, die eine benutzerdefinierte Gina schreiben, um spezialisierte Anmeldedaten zu akzeptieren, z. b. eine [*Smartcard*](../secgloss/s-gly.md) oder Daten zur Datenverarbeitung, auch ein Authentifizierungs Paketschreiben, das für die Verarbeitung dieser Daten und die Bestimmung der Echtheit zuständig ist.

 

Weitere Informationen zu Winlogon und Ginas finden Sie unter [Winlogon und Gina](winlogon-and-gina.md). Weitere Informationen zu Authentifizierungs Paketen finden Sie unter [Erstellen benutzerdefinierter Sicherheitspakete](creating-custom-security-packages.md).

 

 
