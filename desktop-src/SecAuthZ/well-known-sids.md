---
description: Bekannte Sicherheits-IDs (SIDs) identifizieren generische Gruppen und generische Benutzer.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: Bekannte SIDs
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 17fe8827100f9e3684ac0219fc83f183581017cc5738af5933b7bb7cc4ea3ff8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623090"
---
# <a name="well-known-sids"></a>Bekannte SIDs

Bekannte [*Sicherheits-IDs*](/windows/desktop/SecGloss/s-gly) (SIDs) identifizieren generische Gruppen und generische Benutzer. Es gibt z. B. bekannte SIDs, um die folgenden Gruppen und Benutzer zu identifizieren:

-   Everyone oder World. Dabei handelt es sich um eine Gruppe, die alle Benutzer enthält.
-   CREATOR \_ OWNER, der als Platzhalter in einem vererbbaren ACE verwendet wird. Wenn der ACE geerbt wird, ersetzt das System die CREATOR OWNER SID durch die SID des Erstellers \_ des Objekts.
-   Die Gruppe Administratoren für die integrierte Domäne auf dem lokalen Computer.

Es gibt [*universelle bekannte SIDs,*](/windows/desktop/SecGloss/u-gly)die für alle sicheren Systeme sinnvoll sind, die dieses Sicherheitsmodell verwenden, einschließlich anderer Betriebssysteme als Windows. Darüber hinaus gibt es bekannte SIDs, die nur auf Windows sind.

Die Windows-API definiert einen Satz von Konstanten für bekannte Bezeichner-Autoritäts- und [*relative Bezeichnerwerte*](/windows/desktop/SecGloss/r-gly) (RID). Sie können diese Konstanten verwenden, um bekannte SIDs zu erstellen. Im folgenden Beispiel werden die Konstanten SECURITY WORLD SID AUTHORITY und SECURITY WORLD RID kombiniert, um die universelle bekannte SID für die spezielle Gruppe zu zeigen, die alle Benutzer \_ \_ darstellt \_ \_ \_ (Jeder oder Welt):

S-1-1-0

In diesem Beispiel wird die Zeichenfolgen-Notation für SIDs verwendet, bei denen S die Zeichenfolge als SID identifiziert, die erste 1 die Revisionsebene der SID und die restlichen beiden Ziffern die SECURITY WORLD SID AUTHORITY- und SECURITY WORLD RID-Konstanten \_ \_ \_ \_ \_ sind.

Sie können die [**AllocateAndInitializeSid-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) verwenden, um eine SID zu erstellen, indem Sie einen Bezeichnerautoritätswert mit bis zu acht Unterautoritätswerten kombinieren. Um beispielsweise zu bestimmen, ob der angemeldete Benutzer Mitglied einer bestimmten bekannten Gruppe ist, rufen Sie **AllocateAndInitializeSid** auf, um eine SID für die bekannte Gruppe zu erstellen, und verwenden Sie die [**EqualSid-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) um diese SID mit den Gruppen-SIDs im Zugriffstoken des Benutzers [*zu vergleichen.*](/windows/desktop/SecGloss/a-gly) Ein Beispiel finden Sie unter [Suchen nach einer SID in einem Zugriffstoken in C++.](searching-for-a-sid-in-an-access-token-in-c--.md) Sie müssen die [**FreeSid-Funktion aufrufen,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) um eine VON **AllocateAndInitializeSid** zugeordnete SID freigibt.

Der Rest dieses Abschnitts enthält Tabellen mit bekannten SIDs und Tabellen mit Bezeichnerautoritäts- und Unterautoritätskonstatoren, die Sie zum Erstellen bekannter SIDs verwenden können.

Im Folgenden finden Sie einige [*universelle bekannte SIDs.*](/windows/desktop/SecGloss/u-gly)



| Universelle bekannte SID    | Zeichenfolgenwert       | Identifiziert                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL-SID<br/>         | S-1-0-0<br/> | Eine Gruppe ohne Mitglieder. Dies wird häufig verwendet, wenn ein SID-Wert nicht bekannt ist.<br/>                                                                    |
| World<br/>            | S-1-1-0<br/> | Eine Gruppe, die alle Benutzer enthält.<br/>                                                                                                              |
| Lokales Gerät<br/>            | S-1-2-0<br/> | Benutzer, die sich [*lokal*](/windows/desktop/SecGloss/t-gly) (physisch) an Terminals anmelden, die mit dem System verbunden sind.<br/> |
| Creator Owner ID<br/> | S-1-3-0<br/> | Eine Sicherheits-ID, die durch die Sicherheits-ID des Benutzers ersetzt werden soll, der ein neues -Objekt erstellt hat. Diese SID wird in vererbbaren ACEs verwendet.<br/>   |
| Erstellergruppen-ID<br/> | S-1-3-1<br/> | Eine Sicherheits-ID, die durch die PRIMÄRE GRUPPEN-SID des Benutzers ersetzt werden soll, der ein neues -Objekt erstellt hat. Verwenden Sie diese SID in vererbbaren ACEs.<br/>         |



 

In der folgenden Tabelle sind die vordefinierten Konstanten der Bezeichner-Autorität aufgeführt. Die ersten vier Werte werden mit universellen bekannten SIDs verwendet. der letzte Wert wird mit Windows bekannten SIDs verwendet.



| Bezeichnerstelle                         | Wert        | Zeichenfolgenwert |
|----------------------------------------------|--------------|-------------------|
| \_ \_ SICHERHEITS-NULL-SID-AUTORITÄT \_<br/>    | 0<br/> | S-1-0<br/>  |
| SECURITY \_ WORLD \_ SID \_ AUTHORITY<br/>   | 1<br/> | S-1-1<br/>  |
| LOKALE \_ \_ SICHERHEITS-SID-AUTORITÄT \_<br/>   | 2<br/> | S-1-2<br/>  |
| \_ \_ SICHERHEITSERSTELLER-SID-AUTORITÄT \_<br/> | 3<br/> | S-1-3<br/>  |
| \_ \_ SICHERHEITS-NT-AUTORITÄT<br/>           | 5<br/> | S-1-5<br/>  |



 

Die folgenden [*RID-Werte*](/windows/desktop/SecGloss/r-gly) werden mit [*universellen bekannten SIDs verwendet.*](/windows/desktop/SecGloss/u-gly) In der Spalte Bezeichnerstelle wird das Präfix der Bezeichnerstelle angezeigt, mit der Sie die RID kombinieren können, um eine universelle bekannte SID zu erstellen.



| Relative Bezeichnerstelle            | Wert        | Zeichenfolgenwert |
|------------------------------------------|--------------|----------------------|
| SECURITY \_ NULL \_ RID<br/>           | 0<br/> | S-1-0<br/>     |
| SECURITY \_ WORLD \_ RID<br/>          | 0<br/> | S-1-1<br/>     |
| LOKALE \_ \_ SICHERHEITS-RID<br/>          | 0<br/> | S-1-2<br/>     |
| \_ \_ SICHERHEITS-RID FÜR LOKALE \_ ANMELDUNG<br/>   | 1<br/> | S-1-2<br/>     |
| SECURITY \_ CREATOR \_ OWNER \_ RID<br/> | 0<br/> | S-1-3<br/>     |
| SECURITY \_ CREATOR \_ GROUP \_ RID<br/> | 1<br/> | S-1-3<br/>     |



 

Die vordefinierte Bezeichnerstelle SECURITY \_ NT \_ AUTHORITY (S-1-5) erzeugt SIDs, die nicht universell, aber nur bei Windows sind. Sie können die folgenden RID-Werte mit SECURITY \_ NT \_ AUTHORITY verwenden, um bekannte SIDs zu erstellen.



| Konstante                                          | Zeichenfolgenwert               | Identifiziert                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SECURITY \_ DIALUP \_ RID<br/>                  | S-1-5-1<br/>         | Benutzer, die sich mithilfe [*eines*](/windows/desktop/SecGloss/t-gly) DFÜ-Modems an Terminals anmelden. Dies ist ein Gruppenbezeichner.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_ \_ SICHERHEITSNETZWERK-RID<br/>                 | S-1-5-2<br/>         | Benutzer, die sich über ein Netzwerk anmelden. Dies ist ein Gruppenbezeichner, der dem Token eines Prozesses hinzugefügt wurde, als er über ein Netzwerk angemeldet wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ LOGON \_ NETWORK.<br/>                                                                                                                                                                                                                                                                                                                      |
| SICHERHEIT \_ BATCH \_ RID<br/>                   | S-1-5-3<br/>         | Benutzer, die sich mithilfe einer Batchwarteschlangenfunktion anmelden. Dies ist ein Gruppenbezeichner, der dem Token eines Prozesses hinzugefügt wurde, als er als Batchauftrag protokolliert wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ LOGON \_ BATCH.<br/>                                                                                                                                                                                                                                                                                                                 |
| SECURITY \_ INTERACTIVE \_ RID<br/>             | S-1-5-4<br/>         | Benutzer, die sich für den interaktiven Vorgang anmelden. Dies ist ein Gruppenbezeichner, der dem Token eines Prozesses hinzugefügt wurde, als er interaktiv angemeldet wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ LOGON \_ INTERACTIVE.<br/>                                                                                                                                                                                                                                                                                                            |
| RID \_ FÜR \_ SICHERHEITSANMELDUNGS-IDS \_<br/>              | S-1-5-5-*X* - *Y*<br/> | Eine Anmeldesitzung. Dadurch wird sichergestellt, dass nur [*Prozesse*](/windows/desktop/SecGloss/p-gly) in einer bestimmten Anmeldesitzung Zugriff auf die Fensterstationsobjekte für diese Sitzung erhalten. Die *X-* und *Y-Werte* für diese SIDs unterscheiden sich für jede Anmeldesitzung. Der Wert SECURITY \_ LOGON \_ IDS \_ RID COUNT ist die Anzahl der \_ RIDs in diesem Bezeichner (5-*X* - *Y*).<br/>                                                                                                                   |
| \_ \_ SICHERHEITSDIENST-RID<br/>                 | S-1-5-6<br/>         | Konten, die für die Anmeldung als Dienst autorisiert sind. Dies ist ein Gruppenbezeichner, der dem Token eines Prozesses hinzugefügt wurde, als er als Dienst protokolliert wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ LOGON \_ SERVICE.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_ANONYME \_ \_ SICHERHEITSANMELDUNGS-RID<br/>        | S-1-5-7<br/>         | Anonyme Anmeldung oder NULL-Sitzungsanmeldung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ SICHERHEITSPROXY-RID<br/>                   | S-1-5-8<br/>         | Proxy.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| RID FÜR \_ \_ SICHERHEITSUNTERNEHMENSCONTROLLER \_<br/> | S-1-5-9<br/>         | Enterprise Controller.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ SICHERHEITSPRINZIPAL SELF \_ RID<br/>         | S-1-5-10<br/>        | Die PRINCIPAL \_ SELF-Sicherheits-ID kann in der ACL eines Benutzer- oder Gruppenobjekts verwendet werden. Während einer Zugriffsüberprüfung ersetzt das System die SID durch die SID des Objekts. Die PRINCIPAL \_ SELF SID ist nützlich, um einen vererbbaren ACE anzugeben, der für das Benutzer- oder Gruppenobjekt gilt, das den ACE erbt. Es ist die einzige Möglichkeit, die SID eines erstellten Objekts im [*Standardsicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) des Schemas darzustellen.<br/> |
| \_SICHERHEITSAUTHENTIFIZIERTE \_ \_ BENUTZER-RID<br/>     | S-1-5-11<br/>        | Die authentifizierten Benutzer.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SICHERHEITSEINSCHRÄNKUNG \_ DER \_ \_ CODE-RID<br/>        | S-1-5-12<br/>        | Eingeschränkter Code.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ \_ SICHERHEITSTERMINALSERVER-RID<br/>        | S-1-5-13<br/>        | Terminaldienste. Wird automatisch dem Sicherheitstoken eines Benutzers hinzugefügt, der sich bei einem Terminalserver anmeldet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_LOKALE \_ \_ SICHERHEITSSYSTEM-RID<br/>           | S-1-5-18<br/>        | Ein spezielles Konto, das vom Betriebssystem verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SICHERHEIT \_ NT \_ NICHT \_ EINDEUTIG<br/>              | S-1-5-21<br/>        | SIDS sind nicht eindeutig.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SECURITY \_ BUILTIN \_ DOMAIN \_ RID<br/>         | S-1-5-32<br/>        | Die integrierte Systemdomäne.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SICHERHEIT: \_ \_ EINGESCHRÄNKTE \_ \_ CODE-RID SCHREIBEN<br/> | S-1-5-33<br/>        | Schreiben sie eingeschränkten Code.<br/> |


 

Die folgenden RIDs sind relativ zu jeder Domäne.



| RID                                                                | Wert       | Identifiziert                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ DOMÄNENALIAS RID \_ CERTSVC \_ DCOM ACCESS \_ \_ GROUP<br/>              | 0x0000023E | Die Gruppe von Benutzern, die mithilfe von Distributed Component Object Model (DCOM) eine Verbindung mit Zertifizierungsstellen herstellen können.<br/>                                                                                                                          |
| RID-ADMINISTRATOR DES \_ \_ DOMÄNENBENUTZERS \_<br/>                                      | 0x000001F4 | Das Administratorbenutzerkonto in einer Domäne.<br/>                                                                                                                                                                                              |
| \_ \_ RID-GAST DES DOMÄNENBENUTZERS \_<br/>                                      | 0x000001F5 | Das Gastbenutzerkonto in einer Domäne. Benutzer ohne Konto können sich automatisch bei diesem Konto anmelden.<br/>                                                                                                                            |
| \_RID-ADMINISTRATOREN FÜR DOMÄNENGRUPPEN \_ \_<br/>                                    | 0x00000200 | Die Gruppe der Domänenadministratoren. Dieses Konto ist nur auf Systemen mit Serverbetriebssystemen vorhanden.<br/>                                                                                                                                   |
| \_ \_ DOMÄNENGRUPPEN-RID-BENUTZER \_<br/>                                     | 0x00000201 | Eine Gruppe, die alle Benutzerkonten in einer Domäne enthält. Alle Benutzer werden dieser Gruppe automatisch hinzugefügt.<br/>                                                                                                                                     |
| \_RID-GÄSTE DER DOMÄNENGRUPPE \_ \_<br/>                                    | 0x00000202 | Das Gastgruppenkonto in einer Domäne.<br/>                                                                                                                                                                                                      |
| \_RID-COMPUTER DER DOMÄNENGRUPPE \_ \_<br/>                                 | 0x00000203 | Die Gruppe der Domänencomputer. Alle Computer in der Domäne sind Mitglieder dieser Gruppe.<br/>                                                                                                                                                       |
| \_RID-CONTROLLER FÜR DOMÄNENGRUPPEN \_ \_<br/>                               | 0x00000204 | Die Gruppe der Domänencontroller. Alle Dcs in der Domäne sind Mitglieder dieser Gruppe.<br/>                                                                                                                                                           |
| \_ \_ \_ DOMÄNENGRUPPEN-RID-ZERTIFIKATADMINISTRATOREN \_<br/>                              | 0x00000205 | Die Gruppe der Zertifikatverleger. Computer, auf denen Zertifikatdienste ausgeführt werden, sind Mitglieder dieser Gruppe.<br/>                                                                                                                                      |
| \_ \_ DOMÄNENGRUPPEN-RID \_ ENTERPRISE \_ READONLY-DOMÄNENCONTROLLER \_ \_<br/> | 0x000001F2 | Die Gruppe der schreibgeschützten Domänencontroller für Unternehmen.<br/>                                                                                                                                                                                     |
| \_ \_ \_ \_ DOMÄNENGRUPPEN-RID-SCHEMAADMINISTRATOREN<br/>                            | 0x00000206 | Die Gruppe der Schemaadministratoren. Mitglieder dieser Gruppe können das Active Directory-Schema ändern.<br/>                                                                                                                                           |
| \_ \_ \_ DOMÄNENGRUPPEN-RID-UNTERNEHMENSADMINISTRATOREN \_<br/>                        | 0x00000207 | Die Gruppe der Unternehmensadministratoren. Mitglieder dieser Gruppe haben Vollzugriff auf alle Domänen in der Active Directory-Gesamtstruktur. Enterprise Administratoren sind für Vorgänge auf Gesamtstrukturebene verantwortlich, z. B. das Hinzufügen oder Entfernen neuer Domänen.<br/> |
| \_ \_ \_ \_ DOMÄNENGRUPPEN-RID-RICHTLINIENADMINISTRATOREN<br/>                            | 0x00000208 | Die Gruppe der Richtlinienadministratoren.<br/>                                                                                                                                                                                                         |
| \_DOMÄNENCONTROLLER FÜR \_ DIE DOMÄNENGRUPPEN RID \_ READONLY \_<br/>                     | 0x00000209 | Die Gruppe schreibgeschützter Domänencontroller.<br/>                                                                                                                                                                                                |                                             
| RID \_ \_ \_ CLONEABLE-CONTROLLER DER DOMÄNENGRUPPE \_<br />                   | 0x0000020A | Die Gruppe der klonbaren Domänencontroller.<br/>                                                                                                                                                                                                |
| DOMAIN \_ GROUP \_ RID \_ CDC \_ RESERVED<br />                            | 0x0000020C | Die reservierte CDC-Gruppe.<br/>                                                                                                                                                                                                                   |
| DURCH \_ \_ DIE DOMÄNENGRUPPE \_ GESCHÜTZTE \_ BENUTZER<br />                         | 0x0000020D | Die geschützte Benutzergruppe.</br>                                                                                                                                                                                                                |
| \_ \_ \_ \_ RID-SCHLÜSSELADMINISTRATOREN DER DOMÄNENGRUPPE<br />                              | 0x0000020E | Die Gruppe "Schlüsseladministratoren".<br/>                                                                                                                                                                                                                     |
| \_ \_ DOMÄNENGRUPPEN-RID \_ ENTERPRISE KEY \_ \_ ADMINS<br />                  | 0x0000020F | Die Gruppe "Administratoren für Unternehmensschlüssel"</br>                                                                                                                                                                                                           |



 

Die folgenden RIDs werden verwendet, um die obligatorische Integritätsstufe anzugeben.



| RID                                                     | Wert                                               | Identifiziert                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| OBLIGATORISCHE, \_ \_ NICHT VERTRAUENSWÜRDIGE \_ RID-SICHERHEIT<br/>          | 0x00000000<br/>                               | Vertrauenswürdigen.<br/>             |
| SECURITY \_ MANDATORY \_ LOW \_ RID<br/>                | 0x00001000<br/>                               | Niedrige Integrität.<br/>         |
| SECURITY \_ MANDATORY \_ MEDIUM \_ RID<br/>             | 0x00002000<br/>                               | Mittlere Integrität.<br/>      |
| SECURITY \_ MANDATORY \_ MEDIUM \_ PLUS \_ RID<br/>       | \_SECURITY MANDATORY MEDIUM RID + \_ \_ 0x100<br/> | Mittlere hohe Integrität.<br/> |
| SECURITY \_ MANDATORY \_ HIGH \_ RID<br/>               | 0X00003000<br/>                               | Hohe Integrität.<br/>        |
| \_OBLIGATORISCHE \_ SYSTEM \_ RID-SICHERHEIT<br/>             | 0x00004000<br/>                               | Systemintegrität.<br/>      |
| SECURITY \_ MANDATORY \_ PROTECTED \_ PROCESS \_ RID<br/> | 0x00005000<br/>                               | Geschützter Prozess.<br/>     |



 

Die folgende Tabelle enthält Beispiele für domänenbezogene RIDs, mit denen Sie bekannte SIDs für lokale Gruppen (Aliase) erstellen können. Weitere Informationen zu lokalen und globalen Gruppen finden Sie unter [Lokale Gruppenfunktionen](/windows/desktop/NetMgmt/local-group-functions) und [Gruppenfunktionen.](/windows/desktop/NetMgmt/group-functions)



| RID                                                              | Wert                 |Zeichenfolgenwert  | Identifiziert                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RID-ADMINISTRATOREN FÜR \_ \_ \_ DOMÄNENALIAS<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Eine lokale Gruppe, die für die Verwaltung der Domäne verwendet wird.<br/>                                                                                                                                                                                                                            |
| \_ \_ DOMÄNENALIAS-RID-BENUTZER \_<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Eine lokale Gruppe, die alle Benutzer in der Domäne darstellt.<br/>                                                                                                                                                                                                                          |
| DOMAIN \_ ALIAS \_ RID \_ GUESTS<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Eine lokale Gruppe, die Gäste der Domäne darstellt.<br/>                                                                                                                                                                                                                             |
| \_ \_ DOMÄNENALIAS RID POWER \_ \_ USERS<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Eine lokale Gruppe, die verwendet wird, um einen Benutzer oder eine Gruppe von Benutzern darzustellen, die ein System so behandeln möchten, als ob es sich um ihren persönlichen Computer und nicht um eine Arbeitsstation für mehrere Benutzer handelt.<br/>                                                                                                      |
| DOMAIN \_ ALIAS \_ RID \_ ACCOUNT \_ OPS<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Eine lokale Gruppe, die nur auf Systemen mit Serverbetriebssystemen vorhanden ist. Diese lokale Gruppe ermöglicht die Kontrolle über Nichtadministratorkonten.<br/>                                                                                                                                    |
| DOMAIN \_ ALIAS \_ RID \_ SYSTEM \_ OPS<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Eine lokale Gruppe, die nur auf Systemen mit Serverbetriebssystemen vorhanden ist. Diese lokale Gruppe führt Systemverwaltungsfunktionen aus, ohne Sicherheitsfunktionen. Sie richtet Netzwerkfreigaben ein, steuert Drucker, entsperrt Arbeitsstationen und führt andere Vorgänge aus.<br/> |
| DOMAIN \_ ALIAS \_ RID \_ PRINT \_ OPS<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Eine lokale Gruppe, die nur auf Systemen mit Serverbetriebssystemen vorhanden ist. Diese lokale Gruppe steuert Drucker und Druckwarteschlangen.<br/>                                                                                                                                                |
| DOMAIN \_ ALIAS \_ RID \_ BACKUP \_ OPS<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Eine lokale Gruppe, die zum Steuern der Zuweisung von Dateisicherungs- und Wiederherstellungsberechtigungen verwendet wird.<br/>                                                                                                                                                                                            |
| DOMAIN \_ ALIAS \_ RID \_ REPLICATOR<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Eine lokale Gruppe, die für das Kopieren von Sicherheitsdatenbanken vom primären Domänencontroller auf die Sicherungsdomänencontroller verantwortlich ist. Diese Konten werden nur vom System verwendet.<br/>                                                                                                       |
| \_ \_ \_ DOMÄNENALIAS-RID-RAS-SERVER \_<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Eine lokale Gruppe, die RAS- und IAS-Server darstellt. Diese Gruppe ermöglicht den Zugriff auf verschiedene Attribute von Benutzerobjekten.<br/>                                                                                                                                                             |
| \_ \_ DOMÄNENALIAS-RID \_ PREW2KCOMPACCESS<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | Eine lokale Gruppe, die nur auf Systemen mit Windows Server 2000 vorhanden ist. Weitere Informationen finden Sie unter [Zulassen des anonymen Zugriffs.](allowing-anonymous-access.md)<br/>                                                                                                                    |
| \_ \_ REMOTEDESKTOPBENUTZER MIT \_ DOMÄNENALIAS-RID \_ \_<br/>            | 0x0000022B<br/> | S-1-5-32-555<br/> | Eine lokale Gruppe, die alle Remotedesktopbenutzer darstellt.<br/>                                                                                                                                                                                                                         |
| \_ \_ \_ \_ DOMÄNENALIAS-RID-NETZWERKKONFIGURATIONSOPTIONEN \_<br/>       | 0x0000022C<br/> | S-1-5-32-556<br/> | Eine lokale Gruppe, die die Netzwerkkonfiguration darstellt. <br/>                                                                                                                                                                                                                       |
| \_ \_ DOMÄNENALIAS-RID \_ EINGEHENDE \_ \_ GESAMTSTRUKTUR-VERTRAUENSSTELLUNGS-GENERATOREN \_<br/> | 0x0000022D<br/> | S-1-5-32-557<br/> | Eine lokale Gruppe, die alle Gesamtstruktur-Vertrauensstellungsbenutzer darstellt.<br/>                                                                                                                                                                                                                           |
| \_ \_ \_ DOMÄNENALIAS-RID-ÜBERWACHUNGSBENUTZER \_<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Eine lokale Gruppe, die alle überwachten Benutzer darstellt.<br/>                                                                                                                                                                                                                        |
| \_ \_ \_ DOMÄNENALIAS-RID-PROTOKOLLIERUNGSBENUTZER \_<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Eine lokale Gruppe, die für die Protokollierung von Benutzern zuständig ist.<br/>                                                                                                                                                                                                                                    |
| DOMAIN \_ ALIAS \_ RID \_ AUTHORIZATIONACCESS<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Eine lokale Gruppe, die den autorisierten Zugriff darstellt.<br/>                                                                                                                                                                                                                            |
| \_ \_ DOMÄNENALIAS-RID \_ \_ TS-LIZENZSERVER \_<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Eine lokale Gruppe, die nur auf Systemen mit Serverbetriebssystemen vorhanden ist, die Terminaldienste und Remotezugriff zulassen.<br/>                                                                                                                                                  |
| \_ \_ \_ DOMÄNENALIAS-RID-DCOM-BENUTZER \_<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Eine lokale Gruppe, die Benutzer darstellt, die Distributed Component Object Model (DCOM) verwenden können.<br/>                                                                                                                                                                                      |
| \_ \_ \_ DOMÄNENALIAS-RID-IUSERS<br/>                            | 0X00000238<br/> | S-1-5-32-568<br/> | Eine lokale Gruppe, die Internetbenutzer darstellt.<br/>                                                                                                                                                                                                                                   |
| \_ \_ DOMÄNENALIAS-RID \_ \_ CRYPTO-OPERATOREN<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Eine lokale Gruppe, die den Zugriff auf Kryptografieoperatoren darstellt.<br/>                                                                                                                                                                                                                 |
| \_DOMÄNENALIAS \_ RID \_ CACHEABLE \_ PRINCIPALS \_ GROUP<br/>      | 0x0000023B<br/> | S-1-5-32-571<br/> | Eine lokale Gruppe, die Prinzipale darstellt, die zwischengespeichert werden können.<br/>                                                                                                                                                                                                                    |
| \_ \_ DOMÄNENALIAS-RID: \_ GRUPPE NICHT \_ \_ ZWISCHENSPEICHERBARER \_ PRINZIPALE<br/> | 0x0000023C<br/> | S-1-5-32-572<br/> | Eine lokale Gruppe, die Prinzipale darstellt, die nicht zwischengespeichert werden können.<br/>                                                                                                                                                                                                                 |
| GRUPPE "LESER \_ DES \_ DOMÄNENALIAS-RID-EREIGNISPROTOKOLLS" \_ \_ \_ \_<br/>        | 0x0000023D<br/> | S-1-5-32-573<br/> | Eine lokale Gruppe, die Ereignisprotokollleser darstellt.<br/>                                                                                                                                                                                                                                |
| DOMAIN \_ ALIAS \_ RID \_ CERTSVC \_ DCOM \_ ACCESS \_ GROUP<br/>      | 0x0000023E<br/> | S-1-5-32-574<br/> | Die lokale Gruppe von Benutzern, die mithilfe von Distributed Component Object Model (DCOM) eine Verbindung mit Zertifizierungsstellen herstellen können.<br/>                                                                                                                                                          |
| \_ \_ REMOTEZUGRIFFSSERVER FÜR \_ REMOTEZUGRIFF MIT \_ DOMÄNENALIAS-RID \_ \_<br />     | 0x0000023F<br/> | S-1-5-32-575<br/> | Eine lokale Gruppe, die RDS-Remotezugriffsserver darstellt.<br/> |
| \_ \_ \_ RDS-ENDPUNKTSERVER MIT \_ DOMÄNENALIAS-RID \_                 | 0x00000240<br/> | S-1-5-32-576<br/> | Eine lokale Gruppe, die Endpunktserver darstellt.<br/> |
| \_ \_ \_ RDS-VERWALTUNGSSERVER MIT \_ DOMÄNENALIAS-RID \_               | 0x00000241<br/> | S-1-5-32-577<br/> | Eine lokale Gruppe, die Verwaltungsserver darstellt. <br/>|
| \_ \_ DOMÄNENALIAS-RID \_ HYPER \_ \_ V-ADMINISTRATOREN                       | 0x00000242<br/> | S-1-5-32-578<br/> | Eine lokale Gruppe, die Hyper-V-Administratoren darstellt. <br/>|
| \_ \_ DOMÄNENALIAS-RID- \_ \_ \_ ZUGRIFFSSTEUERUNGSUNTERSTÜTZUNGS-OPS \_       | 0x00000243<br/> | S-1-5-32-579<br/> | Eine lokale Gruppe, die die Zugriffssteuerungsunterstützung OPS darstellt.<br/> |
| \_REMOTEVERWALTUNGSBENUTZER \_ DER \_ \_ DOMÄNENALIAS-RID \_              | 0x00000244<br/> | S-1-5-32-580<br/> | Eine lokale Gruppe, die Remoteverwaltungsbenutzer darstellt. <br/>|
| \_ \_ \_ DOMÄNENALIAS-RID-STANDARDKONTO \_                       | 0x00000245<br/> | S-1-5-32-581<br/> | Eine lokale Gruppe, die das Standardkonto darstellt. <br/>|
| \_ \_ \_ \_ DOMÄNENALIAS-RID-SPEICHERREPLIKATADMINISTRATOREN \_               | 0x00000246<br/> | S-1-5-32-582<br/> | Eine lokale Gruppe, die Speicherreplikatadministratoren darstellt. <br/>|
| \_ \_ \_ DOMÄNENALIAS-RID-GERÄTEBESITZER \_                            | 0x00000247<br/> | S-1-5-32-583<br/> | Eine lokale Gruppe, die darstellt, kann Einstellungen für Gerätebesitzer erwarten.<br/>|


 

Die [**WELL KNOWN SID \_ \_ \_ TYPE-Enumeration**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) definiert die Liste der häufig verwendeten SIDs. Darüber hinaus verwendet die [Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language,](security-descriptor-definition-language.md) SDDL) [SID-Zeichenfolgen,](sid-strings.md) um auf bekannte SIDs in einem Zeichenfolgenformat zu verweisen.

 

