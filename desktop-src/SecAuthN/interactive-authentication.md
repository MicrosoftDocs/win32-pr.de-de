---
description: Die Authentifizierung ist interaktiv, wenn ein Benutzer zur Eingabe von Anmeldeinformationen aufgefordert wird. Die lokale Sicherheitsautorität (Local Security Authority, LSA) führt eine interaktive Authentifizierung durch, wenn sich ein Benutzer über die GINA-Benutzeroberfläche anmeldet.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Interaktive Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876f3aced39afba0d08a9643e14caae91336daf38a63f3855e76fe50136a16a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482294"
---
# <a name="interactive-authentication"></a>Interaktive Authentifizierung

Die Authentifizierung ist interaktiv, wenn ein Benutzer zur Eingabe von Anmeldeinformationen aufgefordert wird. Die [*lokale Sicherheitsautorität (Local Security Authority,*](../secgloss/l-gly.md) LSA) führt eine interaktive Authentifizierung durch, wenn sich ein Benutzer über die [*GINA-Benutzeroberfläche*](../secgloss/g-gly.md) anmeldet. Die folgende Abbildung zeigt die Teile einer typischen interaktiven Authentifizierung.

![interaktive Authentifizierung](images/lsaint3.png)

Ein Benutzer signalisiert dem System, die Anmeldesequenz zu starten, indem er STRG+ALT+ENTF [*(Secure Attention Sequence,*](../secgloss/s-gly.md) SAS) eingibt. [*Winlogon*](../secgloss/w-gly.md) empfängt die SAS und ruft die GINA auf, um eine Benutzeroberfläche anzuzeigen und die Anmeldedaten des Benutzers wie Benutzername und Kennwort abzurufen.

Nach dem Abrufen der Anmeldedaten ruft die GINA die [**LsaLogonUser-Funktion**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) auf, um den Benutzer zu authentifizieren, und gibt an, welches Authentifizierungspaket zum Auswerten der Anmeldedaten verwendet werden muss.

Der LSA ruft das angegebene Authentifizierungspaket auf und übergibt die Anmeldedaten an dieses. Das Authentifizierungspaket untersucht die Daten und bestimmt, ob die Authentifizierung erfolgreich war. Das Authentifizierungsergebnis wird an das LSA und vom LSA an die GINA zurückgegeben.

Die GINA zeigt den Erfolg oder Fehler der Authentifizierung für den Benutzer an und gibt das Ergebnis der Authentifizierung an Winlogon zurück. Wenn die Authentifizierung erfolgreich ist, beginnt die Anmeldesitzung des Benutzers, und ein Satz von Anmeldeinformationen wird zur [*späteren*](../secgloss/c-gly.md) Referenz gespeichert.

> [!Note]  
> Im Allgemeinen muss ein Entwickler, der eine benutzerdefinierte GINA schreibt, um spezielle Anmeldedaten wie [*Smartcard-*](../secgloss/s-gly.md) oder Netzscandaten zu akzeptieren, auch ein Authentifizierungspaket schreiben, das für die Verarbeitung dieser Daten und die Bestimmung der Authentizität verantwortlich ist.

 

Weitere Informationen zu Winlogon und WPAAs finden Sie unter [Winlogon und GINA.](winlogon-and-gina.md) Weitere Informationen zu Authentifizierungspaketen finden Sie unter [Erstellen von benutzerdefinierten Sicherheitspaketen.](creating-custom-security-packages.md)

 

 
