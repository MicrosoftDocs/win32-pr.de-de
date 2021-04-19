---
description: Eine Sicherheits-ID (SID) ist ein eindeutiger Wert der Variablen Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Sicherheits-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368b2484cd8766aa7fa74c24679e82b10854e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353129"
---
# <a name="security-identifiers"></a>Sicherheits-IDs

Eine [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) ist ein eindeutiger Wert der Variablen Länge, der zum [Identifizieren eines Vertrauens](trustees.md)nehmers verwendet wird. Jedes Konto verfügt über eine eindeutige SID, die von einer Zertifizierungsstelle, z. b. einem Windows-Domänen Controller, ausgestellt und in einer Sicherheitsdatenbank gespeichert wird. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die sid für diesen Benutzer aus der Datenbank ab und platziert Sie im [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) für diesen Benutzer. Das System verwendet die SID im Zugriffs Token, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren. Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht mehr verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.

Die Windows-Sicherheit verwendet SIDs in den folgenden Sicherheitselementen:

-   In [Sicherheits Beschreibungen](security-descriptors.md) zum Identifizieren des Besitzers eines Objekts und einer primären Gruppe
-   In [Zugriffs Steuerungs Einträgen](access-control-entries.md), um den Vertrauens nehmer zu identifizieren, für den der Zugriff gewährt, verweigert oder überwacht wird.
-   In [Zugriffs Token](access-tokens.md), um den Benutzer und die Gruppen zu identifizieren, zu denen der Benutzer gehört

Zusätzlich zu den eindeutig erstellten domänenspezifischen SIDs, die bestimmten Benutzern und Gruppen zugewiesen sind, gibt es bekannte [SIDs](well-known-sids.md) , die generische Gruppen und generische Benutzer identifizieren. Beispielsweise identifizieren die bekannten SIDs "jeder" und "World" eine Gruppe, die alle Benutzer enthält.

Die meisten Anwendungen müssen nie mit SIDs arbeiten. Da die Namen [bekannter SIDs](well-known-sids.md) variieren können, sollten Sie die-Funktionen verwenden, um die SID aus vordefinierten Konstanten zu erstellen, anstatt den Namen der bekannten SID zu verwenden. Beispielsweise verfügt die US-englische Version des Windows-Betriebssystems über eine bekannte SID mit dem Namen "Builtin \\ Administrators", die in internationalen Versionen des Systems einen anderen Namen aufweisen kann. Ein Beispiel, in dem eine bekannte SID erstellt wird, finden Sie unter [Suchen nach einer SID in einem Zugriffs Token in C++](searching-for-a-sid-in-an-access-token-in-c--.md).

Wenn Sie mit SIDs arbeiten müssen, sollten Sie diese nicht direkt bearbeiten. Verwenden Sie stattdessen die folgenden Funktionen.



| Funktion                                                       | BESCHREIBUNG                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Zuweisung"**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Ordnet eine SID mit der angegebenen Anzahl von untergeordneten Autoritäten zu und initialisiert sie.                                                                              |
| [**Wurde von ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Konvertiert eine SID in ein Zeichen folgen Format, das für die Anzeige, Speicherung oder den Transport geeignet ist.                                                                            |
| [**Convertstringsidto sid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Konvertiert eine Zeichen folgen Format-sid in eine gültige, funktionale sid.                                                                                                  |
| [**Wurde von copysid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Kopiert eine Quell-sid in einen Puffer.                                                                                                                          |
| [**Equalprefixsid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Testet zwei sid-Präfix Werte auf Gleichheit. Ein sid-Präfix ist die gesamte sid, mit Ausnahme des letzten subauthority-Werts.                                          |
| [**Equalsid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Testet zwei SIDs auf Gleichheit. Sie müssen genau übereinstimmen, um als gleich betrachtet zu werden.                                                                              |
| [**Freesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Gibt eine zuvor zugeordnete sid mithilfe der Funktion " [**Zuordnungs-initializesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) " frei.                                      |
| [**Getlängen-sid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Ruft die Länge einer SID ab.                                                                                                                            |
| [**Getsididentifierauthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Ruft einen Zeiger auf die bezeichnerbehörde für eine SID ab.                                                                                                |
| [**Getsidlengthrequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Ruft die Größe des Puffers ab, der zum Speichern einer SID mit einer angegebenen Anzahl von untergeordneten Autoritäten erforderlich ist.                                                       |
| [**Getsidsubauthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Ruft einen Zeiger auf eine angegebene untergeordnete Instanz in einer SID ab.                                                                                                 |
| [**Getsidsubautoritycount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Ruft die Anzahl der untergeordneten Autoritäten in einer SID ab.                                                                                                          |
| [**Initializesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Initialisiert eine [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur.                                                                                                               |
| [**Isvalidsid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Testet die Gültigkeit einer SID, indem überprüft wird, ob die Revisionsnummer innerhalb eines bekannten Bereichs liegt und die Anzahl der untergeordneten Autoritäten kleiner als der Maximalwert ist. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Ruft die SID ab, die einem angegebenen Kontonamen entspricht.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Ruft den Kontonamen ab, der einer angegebenen SID entspricht.                                                                                           |



 

 

 
