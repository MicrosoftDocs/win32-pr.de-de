---
description: Bekannte Sicherheits-IDs (SIDs) identifizieren generische Gruppen und generische Benutzer.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: Bekannte SIDs
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 1fdde933b3e4f844e63785ff130aaf89204fe0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349990"
---
# <a name="well-known-sids"></a>Bekannte SIDs

Bekannte [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) identifizieren generische Gruppen und generische Benutzer. Beispielsweise gibt es bekannte SIDs, um die folgenden Gruppen und Benutzer zu identifizieren:

-   Jeder oder jede Welt, eine Gruppe, die alle Benutzer enthält.
-   Ersteller- \_ Besitzer, der in einem vererbbaren ACE als Platzhalter verwendet wird. Wenn der ACE geerbt wird, ersetzt das System die Ersteller \_ -Besitzer-SID durch die SID des Erstellers des Objekts.
-   Die Gruppe "Administratoren" für die integrierte Domäne auf dem lokalen Computer.

Es gibt [*universelle, Bekannte SIDs*](/windows/desktop/SecGloss/u-gly), die für alle sicheren Systeme mit diesem Sicherheitsmodell von Bedeutung sind, einschließlich anderer Betriebssysteme als Windows. Außerdem gibt es bekannte SIDs, die nur auf Windows-Systemen sinnvoll sind.

Die Windows-API definiert einen Satz von Konstanten für bekannte Bezeichnerautorität und RID-Werte ( [*relative Identifier*](/windows/desktop/SecGloss/r-gly) ). Sie können diese Konstanten verwenden, um bekannte SIDs zu erstellen. Im folgenden Beispiel werden die Security \_ World \_ sid \_ Authority und Security \_ World \_ RID Konstanten kombiniert, um die universelle, bekannte sid für die spezielle Gruppe, die alle Benutzer repräsentiert (alle oder Welt), anzuzeigen:

S-1-1-0

In diesem Beispiel wird die Zeichen folgen Notation für SIDs verwendet, bei der S die Zeichenfolge als SID identifiziert, der erste 1 die Revisions Ebene der SID und die verbleibenden zwei Ziffern die \_ Security \_ World \_ -sid-Autorität und Security \_ World \_ RID-Konstanten.

Sie können die Funktion " [**indecateandinitializesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) " verwenden, um eine SID zu erstellen, indem Sie einen bezeichnerautoritäts Wert mit bis zu acht subautoritäts Werten kombinieren. Um z. b. zu ermitteln, ob der angemeldete Benutzer Mitglied einer bestimmten bekannten Gruppe ist, müssen Sie die **Zuordnung von "Zuordnungs-initializesid** " durchführen, um eine sid für die bekannte Gruppe zu erstellen, und mit der [**equalsid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) -Funktion diese SID mit den Gruppen-SIDs im [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)des Benutzers vergleichen. Ein Beispiel finden Sie unter [Suchen nach einer SID in einem Zugriffs Token in C++](searching-for-a-sid-in-an-access-token-in-c--.md). Sie müssen die [**freesid-**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) Funktion aufrufen, um eine von " **zuordcateandinitializesid**" zugewiesene SID freizugeben.

Im restlichen Teil dieses Abschnitts sind Tabellen bekannter SIDs und Tabellen der bezeichnerzertifizierungs stellen-und subautoritäts Konstanten enthalten, die Sie verwenden können, um bekannte SIDs zu erstellen.

Im folgenden finden Sie einige [*universelle, Bekannte SIDs*](/windows/desktop/SecGloss/u-gly).



| Universelle, bekannte sid    | Zeichenfolgenwert       | Aufzeigt                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL-sid<br/>         | S-1-0-0<br/> | Eine Gruppe ohne Mitglieder. Dies wird häufig verwendet, wenn ein SID-Wert nicht bekannt ist.<br/>                                                                    |
| World<br/>            | S-1-1-0<br/> | Eine Gruppe, die alle Benutzer enthält.<br/>                                                                                                              |
| Lokal<br/>            | S-1-2-0<br/> | Benutzer, die sich lokal (physisch) an [*Terminals*](/windows/desktop/SecGloss/t-gly) anmelden, die mit dem System verbunden sind.<br/> |
| Ersteller Besitzer-ID<br/> | S-1-3-0<br/> | Eine Sicherheits-ID, die durch die Sicherheits-ID des Benutzers ersetzt werden soll, der ein neues-Objekt erstellt hat. Diese SID wird in vererbbaren ACEs verwendet.<br/>   |
| Ersteller Gruppen-ID<br/> | S-1-3-1<br/> | Eine Sicherheits-ID, die durch die primäre Gruppen-SID des Benutzers ersetzt werden soll, der ein neues-Objekt erstellt hat. Verwenden Sie diese SID in vererbbaren ACEs.<br/>         |



 

In der folgenden Tabelle sind die vordefinierten bezeichnerzertifizierungs stellen-Konstanten aufgeführt. Die ersten vier Werte werden mit universellen, bekannten SIDs verwendet. der letzte Wert wird bei Windows-bekannten SIDs verwendet.



| Bezeichnerautorität                         | Wert        | Zeichenfolgenwert |
|----------------------------------------------|--------------|-------------------|
| Sicherheits- \_ NULL- \_ sid- \_ Autorität<br/>    | 0<br/> | S-1-0<br/>  |
| Security \_ World \_ sid \_ Authority<br/>   | 1<br/> | S-1-1<br/>  |
| Lokale Sicherheits- \_ \_ sid- \_ Autorität<br/>   | 2<br/> | S-1-2<br/>  |
| Sicherheits \_ Ersteller- \_ sid- \_ Autorität<br/> | 3<br/> | S-1-3<br/>  |
| Sicherheits- \_ NT- \_ Autorität<br/>           | 5<br/> | S-1-5<br/>  |



 

Die folgenden [*RID*](/windows/desktop/SecGloss/r-gly) -Werte werden für [*universelle, Bekannte SIDs*](/windows/desktop/SecGloss/u-gly)verwendet. In der Spalte Bezeichnerautorität wird das Präfix der bezeichnerbehörde angezeigt, mit der Sie die RID zum Erstellen einer universellen, bekannten SID kombinieren können.



| Relative Bezeichnerautorität            | Wert        | Zeichenfolgenwert |
|------------------------------------------|--------------|----------------------|
| Sicherheits- \_ NULL \_ Rid<br/>           | 0<br/> | S-1-0<br/>     |
| Security \_ World \_ Rid<br/>          | 0<br/> | S-1-1<br/>     |
| Lokale Sicherheits- \_ \_ Rid<br/>          | 0<br/> | S-1-2<br/>     |
| \_Lokale Sicherheits \_ Anmelde- \_ Rid<br/>   | 1<br/> | S-1-2<br/>     |
| Sicherheits \_ Ersteller- \_ Besitzer \_ Rid<br/> | 0<br/> | S-1-3<br/>     |
| Sicherheits \_ Ersteller- \_ Gruppe \_ Rid<br/> | 1<br/> | S-1-3<br/>     |



 

Die \_ \_ vordefinierte bezeichnerbehörde der Sicherheits-NT-Autorität (S-1-5) erzeugt SIDs, die nicht universell sind, aber nur für Windows-Installationen von Bedeutung sind. Sie können die folgenden Rid-Werte mit der \_ Sicherheits \_ -NT-Autorität verwenden, um bekannte SIDs zu erstellen.



| Konstante                                          | Zeichenfolgenwert               | Aufzeigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sicherheits- \_ \_ dialuprid<br/>                  | S-1-5-1<br/>         | Benutzer, die sich mit einem DFÜ-Modem bei [*Terminals*](/windows/desktop/SecGloss/t-gly) anmelden. Dies ist ein Gruppen Bezeichner.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| Sicherheits \_ Netzwerk- \_ Rid<br/>                 | S-1-5-2<br/>         | Benutzer, die sich über ein Netzwerk anmelden. Dies ist eine Gruppen-ID, die dem Token eines Prozesses hinzugefügt wurde, als er über ein Netzwerk angemeldet war. Der entsprechende Anmeldetyp ist LOGON32 \_ Logon \_ Network.<br/>                                                                                                                                                                                                                                                                                                                      |
| Sicherheits \_ Batch \_ Rid<br/>                   | S-1-5-3<br/>         | Benutzer, die sich mit einer Batch Warteschlangen Funktion anmelden. Dies ist eine Gruppen-ID, die dem Token eines Prozesses beim Protokollieren als Batch Auftrag hinzugefügt wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ Logon \_ Batch.<br/>                                                                                                                                                                                                                                                                                                                 |
| \_interaktive \_ RID-Sicherheit<br/>             | S-1-5-4<br/>         | Benutzer, die sich für den interaktiven Vorgang anmelden. Dies ist eine Gruppen-ID, die dem Token eines Prozesses hinzugefügt wurde, als Sie interaktiv angemeldet wurde. Der entsprechende Anmeldetyp ist LOGON32 \_ Logon \_ Interactive.<br/>                                                                                                                                                                                                                                                                                                            |
| Sicherheits \_ Anmelde- \_ IDs \_ Rid<br/>              | S-1-5-5-*X* - *Y*<br/> | Eine Anmelde Sitzung. Dadurch wird sichergestellt, dass nur [*Prozesse*](/windows/desktop/SecGloss/p-gly) in einer bestimmten Anmelde Sitzung auf die Fenster Station-Objekte für diese Sitzung zugreifen können. Die *X* -und *Y* -Werte für diese SIDs unterscheiden sich für jede Anmelde Sitzung. Der Wert der \_ RID-Anzahl der Wert Sicherheits Anmelde- \_ IDs \_ \_ ist die Anzahl der RIDs in diesem Bezeichner (5-*X* - *Y*).<br/>                                                                                                                   |
| Sicherheits \_ Dienst- \_ Rid<br/>                 | S-1-5-6<br/>         | Konten, die zum Anmelden als Dienst autorisiert sind. Dies ist eine Gruppen-ID, die dem Token eines Prozesses beim Protokollieren als Dienst hinzugefügt wurde. Der entsprechende \_ \_ Anmeldetyp ist LOGON32 Logon Service.<br/>                                                                                                                                                                                                                                                                                                                    |
| Sicherheits \_ anonyme \_ Anmelde- \_ Rid<br/>        | S-1-5-7<br/>         | Anonyme Anmeldung oder Anmeldung bei Null-Sitzungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Sicherheits \_ Proxy- \_ Rid<br/>                   | S-1-5-8<br/>         | Proxy.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Security \_ Enterprise \_ Controllers \_ Rid<br/> | S-1-5-9<br/>         | Unternehmens Controller.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Self-Rid-Sicherheits \_ Prinzipal \_ \_<br/>         | S-1-5-10<br/>        | Die eigen Sicherheits-ID des \_ Prinzipals kann in der ACL eines Benutzer-oder Gruppen Objekts verwendet werden. Während einer Zugriffs Überprüfung ersetzt das System die SID durch die SID des Objekts. Die Prinzipal- \_ Self-sid ist nützlich für die Angabe eines vererbbaren ACE, der für das Benutzer-oder Gruppen Objekt gilt, das den ACE erbt. Dies ist die einzige Möglichkeit zur Darstellung der SID eines erstellten Objekts in der Standard [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des Schemas.<br/> |
| Benutzer-Rid für Sicherheits \_ authentifizierte \_ Benutzer \_<br/>     | S-1-5-11<br/>        | Die authentifizierten Benutzer.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Rid-Code für Sicherheits \_ Einschränkung \_ \_<br/>        | S-1-5-12<br/>        | Eingeschränkter Code.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Sicherheits \_ Terminal \_ Server- \_ Rid<br/>        | S-1-5-13<br/>        | Terminal Dienste. Wird dem Sicherheits Token eines Benutzers, der sich an einem Terminal Server anmeldet, automatisch hinzugefügt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_Rid des lokalen \_ Systems \_ für Sicherheit<br/>           | S-1-5-18<br/>        | Ein spezielles Konto, das vom Betriebssystem verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Sicherheit \_ NT \_ nicht \_ eindeutig<br/>              | S-1-5-21<br/>        | SIDs sind nicht eindeutig.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Sicherheits- \_ BuiltIn \_ Domäne \_ Rid<br/>         | S-1-5-32<br/>        | Die integrierte System Domäne.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ \_ Code Rid mit eingeschränktem Sicherheits Schreibvorgang \_<br/> | S-1-5-33<br/>        | Schreiben Sie eingeschränkten Code.<br/> |


 

Die folgenden RIDs sind relativ zu den einzelnen Domänen.



| RID                                                                | Wert       | Aufzeigt                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Domänenalias \_ RID \_ CertSvc- \_ DCOM- \_ Zugriffs \_ Gruppe<br/>              | 0x0000023e | Die Gruppe von Benutzern, die eine Verbindung mit Zertifizierungsstellen mithilfe verteilter Component Object Model (DCOM) herstellen können.<br/>                                                                                                                          |
| Domänen \_ Benutzer- \_ RID- \_ Administrator<br/>                                      | 0x000001, f 4 | Das Administrator Benutzerkonto in einer Domäne.<br/>                                                                                                                                                                                              |
| Domänen \_ Benutzer- \_ RID- \_ Gast<br/>                                      | 0x000001, f-5 | Das Gastbenutzer Konto in einer Domäne. Benutzer, die kein Konto besitzen, können sich automatisch bei diesem Konto anmelden.<br/>                                                                                                                            |
| Domänen Gruppen-Rid-Administratoren \_ \_ \_<br/>                                    | 0x00000200 | Die Gruppe der Domänen Administratoren. Dieses Konto ist nur auf Systemen vorhanden, auf denen Server Betriebssysteme ausgeführt werden.<br/>                                                                                                                                   |
| Domänen \_ Gruppen- \_ RID- \_ Benutzer<br/>                                     | 0x00000201 | Eine Gruppe, die alle Benutzerkonten in einer Domäne enthält. Alle Benutzer werden dieser Gruppe automatisch hinzugefügt.<br/>                                                                                                                                     |
| Domänen \_ Gruppen- \_ RID- \_ Gäste<br/>                                    | 0x00000202 | Das Gastgruppen Konto in einer Domäne.<br/>                                                                                                                                                                                                      |
| Domänen \_ Gruppen- \_ RID- \_ Computer<br/>                                 | 0x00000203 | Die Gruppe der Domänen Computer. Alle Computer in der Domäne sind Mitglieder dieser Gruppe.<br/>                                                                                                                                                       |
| Domänen \_ Gruppen- \_ RID- \_ Controller<br/>                               | 0x00000204 | Die Gruppe der Domänen Controller. Alle DCS in der Domäne sind Mitglieder dieser Gruppe.<br/>                                                                                                                                                           |
| Domänen \_ Gruppen- \_ RID- \_ CERT \_ -Administratoren<br/>                              | 0x00000205 | Die Gruppe der Zertifikat Herausgeber. Computer, auf denen Zertifikat Dienste ausgeführt werden, sind Mitglieder dieser Gruppe.<br/>                                                                                                                                      |
| Domänen \_ Gruppe \_ RID Enterprise-schreibgeschützte \_ \_ \_ Domänen \_ Controller<br/> | 0x000001, f 2 | Die Gruppe von schreibgeschützten Domänen Controllern für Unternehmen.<br/>                                                                                                                                                                                     |
| Domänen \_ Gruppen- \_ RID- \_ Schema \_ Administratoren<br/>                            | 0x00000206 | Die Gruppe "Schema Administratoren". Mitglieder dieser Gruppe können das Active Directory-Schema ändern.<br/>                                                                                                                                           |
| Domänen \_ Gruppe \_ RID \_ Enterprise \_ -Administratoren<br/>                        | 0x00000207 | Die Gruppe "Unternehmens Administratoren". Mitglieder dieser Gruppe verfügen über Vollzugriff auf alle Domänen in der Active Directory Gesamtstruktur. Unternehmens Administratoren sind für Vorgänge auf Gesamtstruktur Ebene zuständig, z. b. das Hinzufügen oder entfernen neuer Domänen.<br/> |
| Domänen \_ Gruppen- \_ RID- \_ Richtlinien- \_ Administratoren<br/>                            | 0x00000208 | Die Gruppe der Richtlinien Administratoren.<br/>                                                                                                                                                                                                         |
| Domänen Gruppen-Rid-schreibgeschützte \_ \_ \_ \_ Controller<br/>                     | 0x00000209 | Die Gruppe Schreib geschützter Domänen Controller.<br/>                                                                                                                                                                                                |                                             
| Domänen \_ Gruppen- \_ RID- \_ klonbare \_ Controller<br />                   | 0x0000020a | Die Gruppe der klonbaren Domänen Controller.<br/>                                                                                                                                                                                                |
| Domänen \_ Gruppen- \_ RID- \_ CDC \_ reserviert<br />                            | 0x0000020c | Die reservierte CDC-Gruppe.<br/>                                                                                                                                                                                                                   |
| Domänen Gruppe, für die \_ \_ \_ geschützte \_ Benutzer<br />                         | 0x0000020d | Die Gruppe der geschützten Benutzer.</br>                                                                                                                                                                                                                |
| Domänen \_ Gruppen- \_ RID- \_ Schlüssel \_ Administratoren<br />                              | 0x0000020e | Die Gruppe "Schlüssel-Administratoren".<br/>                                                                                                                                                                                                                     |
| Domänen \_ Gruppe \_ RID \_ Enterprise \_ Key \_ -Administratoren<br />                  | 0x0000020f | Organisations-Administratoren-Gruppe</br>                                                                                                                                                                                                           |



 

Die folgenden RIDs werden zum Angeben der obligatorischen Integritäts Stufe verwendet.



| RID                                                     | Wert                                               | Aufzeigt                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| Sicherheits \_ verbindliche \_ nicht vertrauenswürdige \_ Rid<br/>          | 0x00000000<br/>                               | Nicht vertrauenswürdigen.<br/>             |
| Sicherheits \_ Pflicht \_ niedrige \_ Rid<br/>                | 0x00001000<br/>                               | Niedrige Integrität.<br/>         |
| erforderliche Sicherheits \_ Pflicht \_ Medium \_ Rid<br/>             | 0x00002000<br/>                               | Mittlere Integrität.<br/>      |
| erforderliche Sicherheits \_ Pflicht \_ Medium \_ Plus \_ Rid<br/>       | Erforderliche Sicherheits \_ obligatorische \_ mittlere \_ RID + 0x100<br/> | Mittlere hohe Integrität.<br/> |
| Sicherheits \_ obligatorisch, \_ hohe \_ Rid<br/>               | 0x00003000<br/>                               | Hohe Integrität.<br/>        |
| Sicherheits \_ verbindliche \_ System- \_ Rid<br/>             | 0x00004000<br/>                               | System Integrität.<br/>      |
| Sicherheits \_ verbindliche \_ geschützte \_ Prozess- \_ Rid<br/> | 0x00005000<br/>                               | Geschützter Prozess.<br/>     |



 

In der folgenden Tabelle finden Sie Beispiele für Domänen relative RIDs, die Sie verwenden können, um bekannte SIDs für lokale Gruppen (Aliase) zu bilden. Weitere Informationen zu lokalen und globalen Gruppen finden Sie unter [lokale Gruppenfunktionen](/windows/desktop/NetMgmt/local-group-functions) und [Gruppenfunktionen](/windows/desktop/NetMgmt/group-functions).



| RID                                                              | Wert                 |Zeichenfolgenwert  | Aufzeigt                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Domänen \_ Alias \_ RID \_ -Administratoren<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Eine lokale Gruppe, die für die Verwaltung der Domäne verwendet wird.<br/>                                                                                                                                                                                                                            |
| Benutzer der Domäne \_ Alias \_ RID \_<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Eine lokale Gruppe, die alle Benutzer in der Domäne darstellt.<br/>                                                                                                                                                                                                                          |
| Domänen- \_ Alias \_ RID- \_ Gäste<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Eine lokale Gruppe, die die Gäste der Domäne darstellt.<br/>                                                                                                                                                                                                                             |
| Domänen \_ Alias- \_ \_ \_ Poweruser für Rid<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Eine lokale Gruppe, die einen Benutzer oder eine Gruppe von Benutzern darstellt, die davon ausgehen, dass ein System so behandelt werden soll, als wäre es der persönliche Computer und nicht als Arbeitsstation für mehrere Benutzer.<br/>                                                                                                      |
| Domäne \_ Alias \_ RID- \_ Konto \_ Ops<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Eine lokale Gruppe, die nur auf Systemen vorhanden ist, auf denen Server Betriebssysteme ausgeführt werden. Diese lokale Gruppe ermöglicht die Kontrolle über nicht-Administrator Konten.<br/>                                                                                                                                    |
| \_RID- \_ \_ System \_ Ops für Domänen Alias<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Eine lokale Gruppe, die nur auf Systemen vorhanden ist, auf denen Server Betriebssysteme ausgeführt werden. Diese lokale Gruppe führt Systemverwaltungsfunktionen aus, ohne Sicherheitsfunktionen. Es richtet Netzwerkfreigaben ein, steuert Drucker, entsperrt Arbeitsstationen und führt andere Vorgänge aus.<br/> |
| Domänen \_ Alias- \_ RID- \_ Druck \_ Ops<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Eine lokale Gruppe, die nur auf Systemen vorhanden ist, auf denen Server Betriebssysteme ausgeführt werden. Diese lokale Gruppe steuert Drucker und Druck Warteschlangen.<br/>                                                                                                                                                |
| Domänenalias- \_ \_ RID- \_ Sicherung \_<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Eine lokale Gruppe, die zum Steuern der Zuweisung von Berechtigungen zum Sichern und Wiederherstellen von Dateien verwendet wird.<br/>                                                                                                                                                                                            |
| Domänen \_ Alias- \_ RID- \_ Replikator<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Eine lokale Gruppe, die für das Kopieren von Sicherheitsdatenbanken vom primären Domänen Controller auf die Sicherungs Domänen Controller zuständig ist. Diese Konten werden nur vom System verwendet.<br/>                                                                                                       |
| Domänen- \_ Alias- \_ RAS- \_ \_ Server<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Eine lokale Gruppe, die RAS-und IAS-Server darstellt. Diese Gruppe ermöglicht den Zugriff auf verschiedene Attribute von Benutzer Objekten.<br/>                                                                                                                                                             |
| Domäne \_ Alias \_ RID \_ PREW2KCOMPACCESS<br/>                  | 0x0000022a<br/> | S-1-5-32-554<br/> | Eine lokale Gruppe, die nur auf Systemen mit Windows 2000 Server vorhanden ist. Weitere Informationen finden Sie unter [Zulassen des anonymen Zugriffs](allowing-anonymous-access.md).<br/>                                                                                                                    |
| Domäne \_ Alias \_ \_ Remote \_ Desktop \_ Benutzer<br/>            | 0x0000022b<br/> | S-1-5-32-555<br/> | Eine lokale Gruppe, die alle Remote Desktop Benutzer darstellt.<br/>                                                                                                                                                                                                                         |
| Domänen- \_ Alias \_ RID \_ Netzwerk \_ Konfiguration \_ Ops<br/>       | 0x0000022c<br/> | S-1-5-32-556<br/> | Eine lokale Gruppe, die die Netzwerkkonfiguration darstellt. <br/>                                                                                                                                                                                                                       |
| Domänen \_ Alias \_ RID für \_ eingehende Gesamt \_ \_ Struktur-Vertrauens \_ Generatoren<br/> | 0x0000022d<br/> | S-1-5-32-557<br/> | Eine lokale Gruppe, die alle Gesamtstruktur-Vertrauensstellungs Benutzer darstellt.<br/>                                                                                                                                                                                                                           |
| benutzerbenutzerbenutzerbenutzer \_ \_ \_ \_<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Eine lokale Gruppe, die alle überwachten Benutzer darstellt.<br/>                                                                                                                                                                                                                        |
| \_ \_ \_ \_ Benutzer<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Eine lokale Gruppe, die zum Protokollieren von Benutzern zuständig ist<br/>                                                                                                                                                                                                                                    |
| Domäne \_ Alias \_ RID \_ authorizationaccess<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Eine lokale Gruppe, die den gesamten autorisierten Zugriff darstellt.<br/>                                                                                                                                                                                                                            |
| Domänen \_ Alias \_ RID \_ TS- \_ Lizenz \_ Server<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Eine lokale Gruppe, die nur auf Systemen mit Server Betriebssystemen vorhanden ist, die Terminaldienste und Remote Zugriff zulassen.<br/>                                                                                                                                                  |
| Domänen \_ Alias \_ RID \_ DCOM- \_ Benutzer<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Eine lokale Gruppe, die Benutzer darstellt, die verteilte Component Object Model (DCOM) verwenden können.<br/>                                                                                                                                                                                      |
| Domäne \_ Alias \_ - \_ iusers<br/>                            | 0x00000238<br/> | S-1-5-32-568<br/> | Eine lokale Gruppe, die Internet Benutzer darstellt.<br/>                                                                                                                                                                                                                                   |
| Domänen \_ Alias- \_ RID- \_ Crypto \_<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Eine lokale Gruppe, die den Zugriff auf kryptografieoperatoren darstellt.<br/>                                                                                                                                                                                                                 |
| Domänenalias-Gruppe für zwischen speicherbare \_ \_ \_ \_ Prinzipale \_<br/>      | 0x0000023b<br/> | S-1-5-32-571<br/> | Eine lokale Gruppe, die Prinzipale darstellt, die zwischengespeichert werden können.<br/>                                                                                                                                                                                                                    |
| Domäne \_ Alias \_ RID \_ nicht zwischen speicherbare \_ \_ Prinzipale- \_ Gruppe<br/> | 0x0000023c<br/> | S-1-5-32-572<br/> | Eine lokale Gruppe, die Prinzipale darstellt, die nicht zwischengespeichert werden können.<br/>                                                                                                                                                                                                                 |
| Domänen \_ Alias- \_ RID- \_ Ereignisprotokoll- \_ \_ Leser \_ Gruppe<br/>        | 0x0000023d<br/> | S-1-5-32-573<br/> | Eine lokale Gruppe, die Ereignisprotokoll Leser darstellt.<br/>                                                                                                                                                                                                                                |
| \_Domänenalias \_ RID \_ CertSvc- \_ DCOM- \_ Zugriffs \_ Gruppe<br/>      | 0x0000023e<br/> | S-1-5-32-574<br/> | Die lokale Gruppe von Benutzern, die eine Verbindung mit Zertifizierungsstellen mithilfe verteilter Component Object Model (DCOM) herstellen können.<br/>                                                                                                                                                          |
| Domänen \_ Alias \_ RID \_ RDS- \_ Remote \_ Zugriffs \_ Server<br />     | 0x0000023f<br/> | S-1-5-32-575<br/> | Eine lokale Gruppe, die RDS-Remote Zugriffs Server darstellt.<br/> |
| Domänen Aliase- \_ \_ RDS- \_ \_ Endpunkt \_ Server                 | 0x00000240<br/> | S-1-5-32-576<br/> | Eine lokale Gruppe, die Endpunkt Server darstellt.<br/> |
| Domänen \_ Alias \_ RID \_ RDS- \_ Verwaltungs \_ Server               | 0x00000241<br/> | S-1-5-32-577<br/> | Eine lokale Gruppe, die Verwaltungs Server darstellt. <br/>|
| \_Domänenalias \_ RID \_ Hyper \_ V \_ Admins                       | 0x00000242<br/> | S-1-5-32-578<br/> | Eine lokale Gruppe, die Hyper-v-Administratoren darstellt <br/>|
| \_Unterstützung für die RID- \_ \_ Zugriffs \_ Steuerung \_ \_ in Domänen Alias       | 0x00000243<br/> | S-1-5-32-579<br/> | Eine lokale Gruppe, die die Unterstützung für die Zugriffs Steuerungs Unterstützung darstellt.<br/> |
| Benutzer der Domänen \_ Alias- \_ \_ Remote \_ Verwaltung \_              | 0x00000244<br/> | S-1-5-32-580<br/> | Eine lokale Gruppe, die Remote Verwaltungs Benutzer darstellt. <br/>|
| Standardkonto für Domänen \_ Alias \_ RID \_ \_                       | 0x00000245<br/> | S-1-5-32-581<br/> | Eine lokale Gruppe, die das Standardkonto darstellt. <br/>|
| Domänenalias- \_ \_ RID- \_ Speicher \_ Replikat \_ Administratoren               | 0x00000246<br/> | S-1-5-32-582<br/> | Eine lokale Gruppe, die Speicher Replikat Administratoren darstellt. <br/>|
| Domäne \_ Alias \_ RID- \_ Geräte \_ Besitzer                            | 0x00000247<br/> | S-1-5-32-583<br/> | Eine lokale Gruppe, die darstellt, kann Einstellungen für Gerätebesitzer erwarten.<br/>|


 

Die [**bekannte \_ \_ sid- \_ Typenumeration**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) definiert die Liste der häufig verwendeten SIDs. Außerdem verwendet die [Security Descriptor Definition Language](security-descriptor-definition-language.md) (SDDL) [sid](sid-strings.md) -Zeichen folgen, um auf bekannte SIDs in einem Zeichen folgen Format zu verweisen.

 

