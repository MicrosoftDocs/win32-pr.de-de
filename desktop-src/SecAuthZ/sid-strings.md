---
description: Erläutert die von sddls verwendeten Zeichen folgen.
ms.assetid: a531532f-afba-46a1-8576-90d4ff881b94
title: SID-Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dad653f221f884fb5d96a402109d0b415d64222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348813"
---
# <a name="sid-strings"></a>SID-Zeichen folgen

In der Security [Deskriptor Definition Language](security-descriptor-definition-language.md) (SDDL) verwendet die [Sicherheits Deskriptor-Zeichenfolge](security-descriptor-string-format.md) sid-Zeichen folgen für die folgenden Komponenten einer [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly):

-   Besitzer
-   Primäre Gruppe
-   Der [Treuhänder](trustees.md) in einem ACE

Eine SID-Zeichenfolge in einer sicherheitsbeschreibungerzeichenfolge kann entweder die standardmäßige Zeichen folgen Darstellung einer sid (s-*R* - *I* - *s* -  ) oder eine der in "SDDL. h" definierten Zeichen folgen Konstanten verwenden. Weitere Informationen zur Standard-sid-Zeichen folgen Notation finden Sie unter [sid-Komponenten](sid-components.md).

Die folgenden sid-Zeichen folgen Konstanten für bekannte SIDs werden in SDDL. h definiert. Informationen zu den entsprechenden [*relativen IDs*](/windows/desktop/SecGloss/r-gly) (RIDs) finden Sie unter [Bekannte SIDs](well-known-sids.md).



| SDDL-sid-Zeichenfolge | Konstante in SDDL. h                               | Kontoalias und zugehörige Rid                                                                                                                                                                                                                        |
|-----------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Halbe<br/> | SDDL \_ Anonym<br/>                       | Anonyme Anmeldung. Die entsprechende RID ist die Sicherheits \_ anonyme \_ Anmelde- \_ RID.<br/>                                                                                                                                                                      |
| OS<br/> | SDDL- \_ Konto \_ Operatoren<br/>              | Konto Operatoren. Die entsprechende RID ist Domänen- \_ Alias- \_ RID- \_ Konto \_ Ops.<br/>                                                                                                                                                                   |
| Thaus<br/> | authentifizierte SDDL- \_ \_ Benutzer<br/>            | Authentifizierte Benutzer. Die entsprechende RID ist eine Sicherheits \_ authentifizierte \_ \_ benutzerrid.<br/>                                                                                                                                                               |
| Ben<br/> | SDDL- \_ BuiltIn- \_ Administratoren<br/>         | Integrierte Administratoren. Die entsprechende RID ist der \_ Domänenalias \_ RID- \_ Administratoren.<br/>                                                                                                                                                                   |
| Stammte<br/> | SDDL- \_ BuiltIn- \_ Gäste<br/>                 | Integrierte Gäste. Die entsprechende RID ist Domäne \_ Alias \_ RID- \_ Gäste.<br/>                                                                                                                                                                           |
| Ur<br/> | SDDL- \_ Sicherungs \_ Operatoren<br/>               | Sicherungs Operatoren. Die entsprechende RID ist die \_ RID-Sicherung für Domänenalias \_ \_ \_ .<br/>                                                                                                                                                                     |
| ECM<br/> | SDDL- \_ BuiltIn- \_ Benutzer<br/>                  | Integrierte Benutzer. Die entsprechende RID ist Domänenalias- \_ \_ RID- \_ Benutzer.<br/>                                                                                                                                                                             |
| Etwa<br/> | SDDL \_ CERT- \_ Serv- \_ Administratoren<br/>      | Zertifikat Herausgeber. Die entsprechende RID ist Domänen Gruppen-Rid-CERT-Administratoren \_ \_ \_ \_ .<br/>                                                                                                                                                              |
| CD<br/> | SDDL \_ CertSvc- \_ DCOM- \_ Zugriff<br/>           | Benutzer, die eine Verbindung zu Zertifizierungsstellen mithilfe verteilter Component Object Model (DCOM) herstellen können. Die entsprechende RID ist der \_ Domänenalias \_ RID \_ CertSvc \_ DCOM \_ Access \_ Group.<br/>                                                                  |
| Gewöhnt<br/> | SDDL \_ - \_ Erstellergruppe<br/>                  | Ersteller-Gruppe. Die entsprechende RID ist die \_ RID der sicherheitserstellergruppe \_ \_ .<br/>                                                                                                                                                                          |
| Erung<br/> | SDDL- \_ Ersteller- \_ Besitzer<br/>                  | Ersteller-Besitzer. Die entsprechende RID ist die \_ Besitzer-Rid des Sicherheits Erstellers \_ \_ .<br/>                                                                                                                                                                          |
| De<br/> | SDDL- \_ Domänen \_ Administratoren<br/>          | Domänen Administratoren. Die entsprechende RID ist Domänen Gruppen-Rid-Administratoren \_ \_ \_ .<br/>                                                                                                                                                                     |
| DC<br/> | SDDL- \_ Domänen \_ Computer<br/>               | Domänen Computer. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID- \_ Computer.<br/>                                                                                                                                                                       |
| Benutzen<br/> | SDDL- \_ Domänen \_ \_ Controller<br/>     | Domänen Controller. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID- \_ Controller.<br/>                                                                                                                                                                   |
| DG<br/> | SDDL- \_ Domänen \_ Gäste<br/>                  | Domänen Gäste. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID- \_ Gäste.<br/>                                                                                                                                                                             |
| S<br/> | SDDL- \_ Domänen \_ Benutzer<br/>                   | Domänen Benutzer. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID- \_ Benutzer.<br/>                                                                                                                                                                               |
| Erkrankungen<br/> | SDDL \_ Enterprise- \_ Administratoren<br/>              | Unternehmens Administratoren. Die entsprechende RID ist Domänen \_ Gruppe \_ RID \_ Enterprise \_ Admins.<br/>                                                                                                                                                     |
| Über<br/> | SDDL \_ Enterprise- \_ Domänen \_ Controller<br/> | Unternehmens Domänen Controller. Die entsprechende RID ist Sicherheits Server-Anmeldungs- \_ \_ \_ RID.<br/>                                                                                                                                                           |
| Hallo<br/> | SDDL \_ ml \_ hoch<br/>                        | Hohe Integritäts Stufe. Die entsprechende RID ist eine Sicherheits \_ Pflicht mit \_ hoher \_ RID.<br/>                                                                                                                                                                  |
| IU<br/> | SDDL \_ interaktiv<br/>                     | Interaktiv angemeldeter Benutzer. Dies ist eine Gruppen-ID, die dem Token eines Prozesses hinzugefügt wurde, als Sie interaktiv angemeldet wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ Logon \_ Interactive. Die entsprechende RID ist die Sicherheits \_ interaktive \_ RID.<br/> |
| '<br/> | lokaler SDDL- \_ \_ Administrator<br/>                    | Lokaler Administrator. Die entsprechende RID ist Domänen \_ Benutzer- \_ RID- \_ Administrator.<br/>                                                                                                                                                                         |
| LG<br/> | lokaler SDDL- \_ \_ Gast<br/>                    | Lokaler Gast. Die entsprechende RID ist der \_ domänenbenutzerrid- \_ \_ Gast.<br/>                                                                                                                                                                                 |
| LS<br/> | lokaler SDDL- \_ \_ Dienst<br/>                  | Lokales Dienst Konto. Die entsprechende RID ist die \_ Rid des Sicherheits lokalen \_ Diensts \_ .<br/>                                                                                                                                                                  |
| "LW"<br/> | SDDL \_ ml \_ niedrig<br/>                         | Niedrige Integritäts Stufe. Die entsprechende RID ist eine Sicherheits \_ obligatorische \_ niedrige \_ RID.<br/>                                                                                                                                                                    |
| Abschließend<br/> | SDDL \_ mlmedium<br/>                        | Mittlere Integritäts Stufe. Die entsprechende RID ist eine Sicherheits \_ obligatorische \_ mittlere \_ RID.<br/>                                                                                                                                                              |
| "MU"<br/> | SDDL \_ Perfmon- \_ Benutzer<br/>                  | System Monitor Benutzer.<br/>                                                                                                                                                                                                                      |
| Gar<br/> | SDDL \_ - \_ Netzwerkkonfigurations- \_ Ops<br/>     | Netzwerkkonfigurations-Operatoren. Die entsprechende RID ist der Domänen- \_ Alias \_ RID \_ Network \_ Configuration \_ Ops.<br/>                                                                                                                                      |
| Danach<br/> | SDDL- \_ Netzwerk \_ Dienst<br/>                | Netzwerkdienst Konto. Die entsprechende RID ist Security \_ Network \_ Service \_ RID.<br/>                                                                                                                                                              |
| Kämpfte<br/> | SDDL- \_ Netzwerk<br/>                         | Netzwerk Anmelde Benutzer. Dies ist eine Gruppen-ID, die dem Token eines Prozesses hinzugefügt wurde, als er über ein Netzwerk angemeldet war. Der entsprechende Anmeldetyp ist LOGON32 \_ Logon \_ Network. Die entsprechende RID ist Security \_ Network \_ RID.<br/>                |
| All<br/> | SDDL- \_ Gruppen \_ Richtlinien- \_ Administratoren<br/>           | Gruppenrichtlinie-Administratoren. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID- \_ Richtlinien- \_ Administratoren.<br/>                                                                                                                                                       |
| Po<br/> | SDDL- \_ Drucker \_ Operatoren<br/>              | Drucker Operatoren. Die entsprechende RID ist Domänenalias- \_ \_ RID- \_ Druck \_ Ops.<br/>                                                                                                                                                                     |
| Psel<br/> | SDDL \_ Personal \_ Self<br/>                  | Prinzipal selbst. Die entsprechende RID ist die \_ Self-Rid-Sicherheits Prinzipal \_ \_ .<br/>                                                                                                                                                                        |
| PU<br/> | SDDL-Haupt \_ \_ Benutzer<br/>                    | Poweruser. Die entsprechende Rid sind \_ \_ Domänenalias-Haupt \_ \_ Benutzer.<br/>                                                                                                                                                                         |
| RC<br/> | eingeschränkter SDDL- \_ \_ Code<br/>                | Eingeschränkter Code. Dabei handelt es sich um ein eingeschränktes Token [**, das mit der Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) "" der Funktion "" erstellt wurde. Die entsprechende RID ist eine \_ Sicherheits \_ eingeschränkte \_ coderid.<br/>                                                        |
| 63<br/> | SDDL \_ \_ -Remote Desktop<br/>                 | Terminal Server Benutzer. Die entsprechende RID ist Domäne \_ Alias \_ \_ Remote \_ Desktop \_ Benutzer.<br/>                                                                                                                                                     |
| Turm<br/> | SDDL- \_ Replikator<br/>                      | Replicator. Die entsprechende RID ist der \_ Domänenalias- \_ RID- \_ Replikator.<br/>                                                                                                                                                                            |
| Tal<br/> | SDDL \_ Enterprise \_ RO \_ DCS<br/>             | Schreibgeschützte Unternehmens Domänen Controller. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID- \_ \_ \_ Domänen Controller für Unternehmen \_ .<br/>                                                                                                                |
| Graben<br/> | SDDL- \_ RAS- \_ Server<br/>                    | RAS-Server Gruppe. Die entsprechende Rid sind Domänen- \_ Alias- \_ RAS- \_ \_ Server.<br/>                                                                                                                                                                   |
| Narren<br/> | SDDL- \_ Alias \_ PREW2KCOMPACC<br/>            | Alias zum Erteilen von Berechtigungen für Konten, die Anwendungen verwenden, die mit Betriebssystemen vor Windows 2000 kompatibel sind. Die entsprechende RID ist der \_ Domänenalias \_ RID \_ PREW2KCOMPACCESS.<br/>                                                         |
| SAS<br/> | SDDL- \_ Schema \_ Administratoren<br/>          | Schema Administratoren. Die entsprechende RID ist Domänen \_ Gruppen- \_ RID-Schema- \_ \_ Administratoren.<br/>                                                                                                                                                             |
| Si<br/> | SDDL \_ ml- \_ System<br/>                      | System Integritäts Stufe. Die entsprechende RID ist eine Sicherheits \_ obligatorische \_ System- \_ RID.<br/>                                                                                                                                                              |
| Tut<br/> | SDDL- \_ Server \_ Operatoren<br/>               | Server Operatoren. Die entsprechende RID ist das \_ \_ RID- \_ System OPS des Domänen Alias \_ .<br/>                                                                                                                                                                     |
| Su<br/> | SDDL- \_ Dienst<br/>                         | Dienst Anmelde Benutzer. Dies ist eine Gruppen-ID, die dem Token eines Prozesses beim Protokollieren als Dienst hinzugefügt wurde. Der entsprechende \_ \_ Anmeldetyp ist LOGON32 Logon Service. Die entsprechende RID ist die Sicherheits \_ Dienst- \_ RID.<br/>                       |
| Mütter<br/> | lokales SDDL- \_ \_ System<br/>                   | Lokales System. Die entsprechende RID ist die \_ Rid des Sicherheits lokalen \_ Systems \_ .<br/>                                                                                                                                                                            |
| Zel<br/> | SDDL- \_ alle<br/>                        | Jeder. Die entsprechende RID ist Security \_ World \_ RID.<br/>                                                                                                                                                                                        |



 

Die [**convertsiddestringsid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) -und [**convertstringsiddesid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) -Funktionen verwenden stets die standardmäßige sid-Zeichen folgen Notation und unterstützen keine SDDL-sid-Zeichen folgen Konstanten.

Weitere Informationen zu bekannten SIDs finden Sie unter [Bekannte SIDs](well-known-sids.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[\[MS-DYP \] : Beschreibung der Sicherheits Beschreibungssprache](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

