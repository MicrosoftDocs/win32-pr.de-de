---
title: Netzwerk Verwaltungsfunktionen
description: Die Netzwerk Verwaltungsfunktionen können wie folgt gruppiert werden.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a169d097fbe86c95aa9aa3120c3f732a8edd2c0
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "106337272"
---
# <a name="network-management-functions"></a>Netzwerk Verwaltungsfunktionen

Die Netzwerk Verwaltungsfunktionen können wie folgt gruppiert werden.

## <a name="alert-functions"></a>Benachrichtigungsfunktionen



| Funktion                                   | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netzwerkertraise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Benachrichtigt alle registrierten Clients, dass ein bestimmtes Ereignis aufgetreten ist.                                                                                                                                  |
| [**"Ntalertraiseex"**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Vereinfacht das Benachrichtigen registrierter Clients, dass ein bestimmtes Ereignis aufgetreten ist, da " **nettalertraiseex** " im Gegensatz zu " **nettalertraise**" keine [**Std- \_**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) Warnungs Struktur erfordert. |



 

## <a name="api-buffer-functions"></a>API-pufferfunktionen



| Funktion                                                 | BESCHREIBUNG                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**"Ntapibuffer" zuordnen**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Belegt Speicher aus dem Heap. Wenn Sie die Kompatibilität mit der Funktion " **nettapibufferfree** " benötigen, können Sie diese Funktion aufrufen. |
| [**"Nettapibufferfree"**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Gibt Arbeitsspeicher frei, der von der Funktion " **nettapibufferbeleg;** " und anderen Netzwerk Verwaltungsfunktionen belegt wird                   |
| [**"Nettapibufferrezuordnen"**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Ändert die Größe eines Puffers, der durch einen Aufrufen der Funktion " **nettapibufferallo"** zugeordnet wird.                                |
| [**"Nettapibuffersize"**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Gibt die Größe eines Puffers in Bytes zurück, der durch einen Aufrufen der Funktion " **nettapibufferallo"** zugeordnet wird.                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Funktionen der Azure Active Directory Join-Informationen



| Funktion                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netfreeaadjoininformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Gibt den für die angegebene [**dsreg \_ Join \_ Info**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) -Struktur zugeordneten Arbeitsspeicher frei, der Joininformationen für einen Mandanten enthält und die Sie durch Aufrufen der [**netgetaadjoininformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) -Funktion abgerufen haben. |
| [**Netgetaadjoininformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Ruft die Joininformationen für den angegebenen Mandanten ab. Diese Funktion untersucht die Joininformationen für Microsoft Azure Active Directory und das Geschäftskonto, das der aktuelle Benutzer hinzugefügt hat.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Verzeichnisdienst-und Domänen joinfunktionen



| Funktion                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netaddalternativen Computername**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Fügt einen alternativen Namen für den angegebenen Computer hinzu.                                                                                                                                                                                                                      |
| [**Netkreateprovisioningpackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Stellt ein Computer Konto für die spätere Verwendung in einem Offline-Domänen Beitritts Vorgang bereit.                                                                                                                                                                                        |
| [**"Nettenreeratecomputernames"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Listet die Namen für den angegebenen Computer auf.                                                                                                                                                                                                                            |
| [**Netgetjoinableous**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Ruft eine Liste der Organisationseinheiten (OUs) ab, in denen ein Computer Konto erstellt werden kann.                                                                                                                                                                              |
| [**Netgetjoininformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Ruft joinstatusinformationen für den angegebenen Computer ab.                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Fügt einen Computer einer Arbeitsgruppe oder einer Domäne hinzu.                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Stellt ein Computer Konto für die spätere Verwendung in einem Offline-Domänen Beitritts Vorgang bereit.                                                                                                                                                                                       |
| [**"Nettremuvealternativen Computername"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Entfernt einen alternativen Namen für den angegebenen Computer.                                                                                                                                                                                                                   |
| [**"Nettrenamemachineindomain"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Ändert den Namen eines Computers in einer Domäne.                                                                                                                                                                                                                             |
| [**"Nettrequestofflinedomainjoin"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | Wird lokal auf einem Computer ausgeführt, um ein auf einem Volume eingebundenes Windows-Betriebssystem Abbild zu ändern. Die Registrierung wird für das Image geladen, und die Bereitstellungs-BLOB-Daten werden geschrieben, wo Sie während der Abschlussphase eines Offline-Domänen Beitritts Vorgangs abgerufen werden können.     |
| [**"Nettrequestprovisioningpackagein Stall"**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | Wird lokal auf einem Computer ausgeführt, um ein auf einem Volume eingebundenes Windows-Betriebssystem Abbild zu ändern. Die Registrierung wird aus dem Image geladen, und die Bereitstellungs Paketdaten werden dort geschrieben, wo Sie während der Abschlussphase eines Offline-Domänen Beitritts Vorgangs abgerufen werden können. |
| [**Netsetprimarycomputername**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Legt den Namen des primären Computers für den angegebenen Computer fest.                                                                                                                                                                                                              |
| [**Netunjoindomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Der Beitritt eines Computers zu einer Arbeitsgruppe oder einer Domäne wird von entfernt.                                                                                                                                                                                                                        |
| [**Netvalidatename**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Überprüft die Gültigkeit eines Computer namens, des Arbeitsgruppen namens oder des Domänen Namens.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Get-Funktionen



| Funktion                                                               | BESCHREIBUNG                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netgetanydcname**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Gibt den Namen eines beliebigen Domänen Controllers für eine Domäne zurück, die direkt von einem angegebenen Server als vertrauenswürdig eingestuft wird.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Gibt den Namen des primären Domänen Controllers (PDC) für die angegebene Domäne zurück.                                                        |
| [**Netgetdisplayinformationindex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Gibt den Index des ersten Anzeige Informations Eintrags zurück, dessen Name mit einer angegebenen Zeichenfolge beginnt oder alphabetisch auf die Zeichenfolge folgt. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Gibt Informationen zu Benutzern, Computern oder globalen Gruppenkonten zurück.                                                                             |



 

## <a name="group-functions"></a>Gruppenfunktionen



| Funktion                                     | BESCHREIBUNG                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**"NetGroupAdd"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Erstellt eine globale Gruppe.                                                           |
| [**Netgroupadduser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Fügt einer vorhandenen globalen Gruppe einen Benutzer hinzu.                                        |
| [**Netgroupdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Entfernt eine globale Gruppe, unabhängig davon, ob die Gruppe über Mitglieder verfügt.                  |
| [**Netgroupdelta User**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Entfernt einen Benutzernamen aus einer globalen Gruppe.                                        |
| [**Netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Listet alle globalen Gruppen auf einem Server auf.                                              |
| [**Netgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Gibt Informationen zu einer bestimmten globalen Gruppe zurück.                              |
| [**Netgroupgetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Listet alle Mitglieder einer bestimmten globalen Gruppe auf.                                   |
| [**Netgroupeintinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Legt allgemeine Informationen zu einer globalen Gruppe fest.                                    |
| [**Netgroupsetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Weist Mitglieder einer neuen globalen Gruppe zu. ersetzt die Mitglieder einer vorhandenen Gruppe. |



 

## <a name="local-group-functions"></a>Lokale Gruppenfunktionen



| Funktion                                                   | BESCHREIBUNG                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Erstellt eine lokale Gruppe.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Fügt einer vorhandenen lokalen Gruppe einen oder mehrere Benutzer oder globale Gruppen hinzu.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Löscht eine lokale Gruppe, wobei alle vorhandenen Mitglieder aus der Gruppe entfernt werden.    |
| [**Netlocalgroupdelta Members**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Entfernt mindestens ein Mitglied aus einer vorhandenen lokalen Gruppe.               |
| [**Netlocalgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Gibt Informationen zu den einzelnen lokalen Gruppenkonten auf einem Server zurück.         |
| [**Netlocalgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Gibt Informationen zu einem bestimmten lokalen Gruppenkonto auf einem Server zurück. |
| [**Netlocalgroupgetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Listet alle Mitglieder einer angegebenen lokalen Gruppe auf.                           |
| [**Netlocalgroupeintinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Legt allgemeine Informationen zu einer lokalen Gruppe fest.                           |
| [**Netlocalgroupsetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Weist Mitglieder einer lokalen Gruppe zu.                                       |



 

## <a name="message-functions"></a>Nachrichtenfunktionen



| Funktion                                               | BESCHREIBUNG                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Netmessagebuffersend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Sendet eine Nachricht an einen registrierten Nachrichtenalias.                                  |
| [**Netmessagenameadd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registriert einen Nachrichtenalias in der Nachrichten Namen Tabelle.                            |
| [**Netmessagenamedel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Löscht einen Nachrichtenalias aus der Nachrichten Namen Tabelle.                            |
| [**Netmessagenameenum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Listet alle in der Tabelle "Nachrichten Name" gespeicherten Nachrichten Aliase auf.                 |
| [**Netmessagenamegetinfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Gibt Informationen zu einem bestimmten Nachrichtenalias in der Nachrichten Namen Tabelle zurück. |



 

## <a name="netfile-functions"></a>Netfile-Funktionen



| Funktion                                | BESCHREIBUNG                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**Netfileclose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Erzwingt das Schließen einer Ressource.                                          |
| [**Netfileaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Gibt Informationen zu geöffneten Dateien auf einem Server zurück.                    |
| [**Netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Gibt Informationen zu einem bestimmten Öffnen einer Server Ressource zurück. |



 

## <a name="remote-utility-functions"></a>Remote Utility-Funktionen



| Funktion                                                       | BESCHREIBUNG                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**"Nettremotecomputerunter stützt"**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Fragt den Redirector ab, um die optionalen Features abzurufen, die von einem Remote System unterstützt werden. |
| [**"Nettremotetod"**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Ermöglicht Anwendungen den Zugriff auf die Uhrzeit Informationen auf einem Remote Server.          |



 

## <a name="schedule-functions"></a>Zeit Plan Funktionen



| Funktion                                                                     | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Sendet einen Auftrag, der zu einem bestimmten Zeitpunkt (Datum und Uhrzeit) ausgeführt wird.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Bricht einen Bereich von Aufträgen in der Warteschlange ab, die auf einem Computer ausgeführt werden.             |
| [**Netschedulejobenum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Listet die Aufträge auf einem angegebenen Computer auf.                   |
| [**Netschedulejobgetinfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Gibt Informationen zu einem bestimmten Auftrag auf einem Computer in der Warteschlange zurück. |
| [**Getnetscheduleaccountinformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Ruft den unter Dienst Kontonamen ab.                           |
| [**Setnetscheduleaccountinformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Legt den unter Dienst Kontonamen und das Kennwort fest.                   |



 

## <a name="server-functions"></a>Server Funktionen



| Funktion                                       | BESCHREIBUNG                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**Netserverdiskerum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Gibt eine Liste lokaler Laufwerke auf einem Server zurück.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Listet alle sichtbaren Server eines bestimmten Typs (oder Typen) in der angegebenen Domäne auf. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Gibt Konfigurationsinformationen zu einem angegebenen Server zurück.                        |
| [**Netserverabfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Legt die Betriebsparameter für einen Server fest.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Server-und Arbeitsstations Transport-Funktionen



| Funktion                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netservercomputernameadd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Bindet einen emulierten Servernamen an jedes Transportprotokoll, für das ein Server aktiv ist. (Kombiniert die Funktionalität der [**netservertransportenum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) -Funktion und der [**netservertransportaddex**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) -Funktion.)                                            |
| [**Netservercomputernamedel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Trennt jedes Netzwerk Transportprotokoll von einem emulierten Servernamen, der durch einen vorherigen-Befehl der **netservercomputernameadd** -Funktion festgelegt wurde.                                                                                                                                                                               |
| [**Netservertransportadd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Bindet den angegebenen Server an das Transportprotokoll. (Diese Funktion unterstützt nur die Informationsebene " [**Server \_ Transport \_ Info \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) ".)                                                                                                                                                |
| [**Netservertransportaddex**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Bindet den angegebenen Server an das Transportprotokoll. (Diese erweiterte Funktion unterstützt die Informationsebenen [**Server \_ Transport \_ Info \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**Server \_ Transport \_ Info \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)und [**Server \_ Transport \_ Info \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**Netservertransportdel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Trennt das Transportprotokoll vom Server.                                                                                                                                                                                                                                                                         |
| [**Netservertransportenum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Listet die vom Server verwalteten Transportprotokolle auf.                                                                                                                                                                                                                                                                   |
| [**Netwkstatus-Sportenum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Listet die Transportprotokolle auf, die vom Redirector verwaltet werden.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Verwenden von Funktionen



| Funktion                               | BESCHREIBUNG                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**"Nettuseadd"**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Erstellt eine Verbindung zwischen einem lokalen Computer und einem Server.                               |
| [**"Nettusedel"**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Beendet eine Verbindung mit einer freigegebenen Ressource.                                                   |
| [**"Nettuseenum"**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Listet alle aktuellen Verbindungen zwischen dem lokalen Computer und den Ressourcen auf Remote Servern. |
| [**"Nettusegetinfo"**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Gibt Informationen zu einer Verbindung mit einer freigegebenen Ressource zurück.                              |



 

## <a name="user-functions"></a>Benutzer Funktionen



| Funktion                                               | BESCHREIBUNG                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**"Nettuseradd"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Fügt ein Benutzerkonto hinzu und weist ein Kennwort und eine Berechtigungsebene zu.     |
| [**"Nettuserchangepassword"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Ändert das Kennwort eines Benutzers für einen angegebenen Netzwerkserver oder eine angegebene Domäne. |
| [**"Nettuserdel"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Löscht ein Benutzerkonto auf dem Server.                             |
| [**"Nettuserenum"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Listet alle Benutzerkonten auf einem Server auf.                                |
| [**"Nettusergetgroups"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Gibt eine Liste der globalen Gruppennamen zurück, zu denen ein Benutzer gehört.       |
| [**"Nettusergetinfo"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Gibt Informationen zu einem bestimmten Benutzerkonto auf einem Server zurück.    |
| [**"Nettusergetlocalgroups"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Gibt eine Liste der lokalen Gruppennamen zurück, zu denen ein Benutzer gehört.        |
| [**"Nettusersetgroups"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Legt globale Gruppenmitgliedschaften für ein angegebenes Benutzerkonto fest.         |
| [**"Nettusersetinfo"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Legt das Kennwort und andere Elemente eines Benutzerkontos fest.             |



 

## <a name="user-modals-functions"></a>Benutzermodals-Funktionen



| Funktion                                     | BESCHREIBUNG                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Nettusermodalsget"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Gibt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank zurück, bei der es sich um die SAM-Datenbank (Security Accounts Manager) handelt, oder, im Fall von Domänen Controllern, die Active Directory. |
| [**"Nettusermodalsset"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Legt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank fest.                                                                                                                       |



 

## <a name="validation-functions"></a>Validierungs Funktionen



| Funktion                                                               | BESCHREIBUNG                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netvalidatepasswordpolicyfree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Gibt den Arbeitsspeicher frei, der von der [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) -Funktion für den *outputarg* -Parameter zugewiesen wird.                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Ermöglicht es einer Anwendung, die Kenn Wort Konformität anhand einer von der Anwendung bereitgestellten Konto Datenbank zu überprüfen und zu überprüfen, ob Kenn Wörter die Anforderungen für die Wiederverwendung von Komplexität, Alterung, minimaler Länge und Verlauf der Kenn Wort |



 

## <a name="workstation-and-workstation-user-functions"></a>Benutzer Funktionen für Arbeitsstationen und Arbeitsstationen



| Funktion                                           | BESCHREIBUNG                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Netwkstagetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Gibt Informationen zu den Konfigurationselementen für eine Arbeitsstation zurück.             |
| [**Netwkstasetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Konfiguriert eine Arbeitsstation.                                                           |
| [**Netwkstauserereration**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Listet Informationen zu allen Benutzern, die zurzeit auf der Arbeitsstation angemeldet sind.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Gibt Informationen zu einem aktuell angemeldeten Benutzer zurück.                             |
| [**Netwkstauserot**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Legt die benutzerspezifischen Informationen für die Konfigurationselemente einer Arbeitsstation fest. |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

-   [**Netaccessadd**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**Network Access Check**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**Netaccessdel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**Netaccessenum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**Netaccessgetinfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**Netaccessgetuserperms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**Netaccesseintinfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**Netauditclear**](netauditclear.md)
-   [**Netauditread**](netauditread.md)
-   [**Netauditwrite**](netauditwrite.md)
-   [**Netconfigget**](netconfigget.md)
-   [**Netconfiggetall**](netconfiggetall.md)
-   [**Netconfigset**](netconfigset.md)
-   [**"Nterrorlogclear"**](neterrorlogclear.md)
-   [**"Netterrorlogread"**](neterrorlogread.md)
-   [**"Netterrorlogwrite"**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**Netlocalgroupdelta Member**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**Netserviceaufumum**](netserviceenum.md)
-   [**Netservicegetinfo**](netservicegetinfo.md)
-   [**Netserviceingestall**](netserviceinstall.md)
-   [**Netwkstaturansport**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**Netwkstaturansport**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Netzwerkfunktionen](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 