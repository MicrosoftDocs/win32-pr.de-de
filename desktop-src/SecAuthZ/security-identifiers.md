---
description: Eine Sicherheits-ID (SID) ist ein eindeutiger Wert variabler Länge, der zum Identifizieren eines Vertrauensnehmers verwendet wird.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Sicherheits-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6acaaeacfbc77b2dc814062c4254c5f08e58869e0b6d8b2fbb64e8511dc31e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413490"
---
# <a name="security-identifiers"></a>Sicherheits-IDs

Eine [*Sicherheits-ID*](/windows/desktop/SecGloss/s-gly) (SID) ist ein eindeutiger Wert variabler Länge, der zum Identifizieren eines [Vertrauensnehmers](trustees.md)verwendet wird. Jedes Konto verfügt über eine eindeutige SID, die von einer Autorität,z. B. einem Windows Domänencontroller, ausgestellt und in einer Sicherheitsdatenbank gespeichert wird. Jedes Mal, wenn sich ein Benutzer anmeldet, ruft das System die SID für diesen Benutzer aus der Datenbank ab und platziert sie im [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) für diesen Benutzer. Das System verwendet die SID im Zugriffstoken, um den Benutzer in allen nachfolgenden Interaktionen mit Windows Sicherheit zu identifizieren. Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann sie nie wieder verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.

Windows Sicherheit verwendet SIDs in den folgenden Sicherheitselementen:

-   In [Sicherheitsbeschreibungen](security-descriptors.md) zum Identifizieren des Besitzers eines Objekts und einer primären Gruppe
-   In [Zugriffssteuerungseinträgen](access-control-entries.md), um den Vertrauensnehmer zu identifizieren, für den der Zugriff zugelassen, verweigert oder überwacht wird.
-   In [Zugriffstoken](access-tokens.md), um den Benutzer und die Gruppen zu identifizieren, denen der Benutzer angehört

Zusätzlich zu den eindeutig erstellten domänenspezifischen SIDs, die bestimmten Benutzern und Gruppen zugewiesen sind, gibt es [bekannte SIDs,](well-known-sids.md) die generische Gruppen und generische Benutzer identifizieren. Beispielsweise identifizieren die bekannten SIDs Jeder und Welt eine Gruppe, die alle Benutzer enthält.

Die meisten Anwendungen müssen nie mit SIDs arbeiten. Da die Namen [bekannter SIDs](well-known-sids.md) variieren können, sollten Sie die -Funktionen verwenden, um die SID aus vordefinierten Konstanten zu erstellen, anstatt den Namen der bekannten SID zu verwenden. Beispielsweise verfügt die englische Version des betriebssystems Windows über eine bekannte SID namens "BUILTIN \\ Administrators", die in internationalen Versionen des Systems möglicherweise einen anderen Namen hat. Ein Beispiel zum Erstellen einer bekannten SID finden Sie unter [Suchen nach einer SID in einem Zugriffstoken in C++](searching-for-a-sid-in-an-access-token-in-c--.md).

Wenn Sie mit SIDs arbeiten müssen, bearbeiten Sie sie nicht direkt. Verwenden Sie stattdessen die folgenden Funktionen.



| Funktion                                                       | Beschreibung                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Ordnet eine SID mit der angegebenen Anzahl von Unterautoritäten zu und initialisiert sie.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Konvertiert eine SID in ein Zeichenfolgenformat, das für Anzeige, Speicherung oder Transport geeignet ist.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Konvertiert eine SID im Zeichenfolgenformat in eine gültige funktionale SID.                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Kopiert eine Quell-SID in einen Puffer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Testet zwei SID-Präfixwerte auf Gleichheit. Ein SID-Präfix ist die gesamte SID, mit Ausnahme des letzten Unterautoritätswerts.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Überprüft zwei SIDs auf Gleichheit. Sie müssen genau übereinstimmen, um als gleich betrachtet zu werden.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Gibt eine zuvor zugeordnete SID mithilfe der [**AllocateAndInitializeSid-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) frei.                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Ruft die Länge einer SID ab.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Ruft einen Zeiger auf die Bezeichnerautorität für eine SID ab.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Ruft die Größe des Puffers ab, der zum Speichern einer SID mit einer angegebenen Anzahl von Unterautoritäten erforderlich ist.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Ruft einen Zeiger auf eine angegebene Unterautorität in einer SID ab.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Ruft die Anzahl der Unterautoritäten in einer SID ab.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Initialisiert eine [**SID-Struktur.**](/windows/desktop/api/Winnt/ns-winnt-sid)                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Überprüft die Gültigkeit einer SID, indem überprüft wird, ob die Revisionsnummer innerhalb eines bekannten Bereichs liegt und dass die Anzahl der Unterautoritäten kleiner als der Höchstwert ist. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Ruft die SID ab, die einem angegebenen Kontonamen entspricht.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Ruft den Kontonamen ab, der einer angegebenen SID entspricht.                                                                                           |



 

 

 
