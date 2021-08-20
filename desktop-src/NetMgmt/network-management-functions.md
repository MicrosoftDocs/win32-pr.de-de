---
title: Netzwerkverwaltungsfunktionen
description: Die Netzwerkverwaltungsfunktionen können wie folgt gruppiert werden.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e9aba93607e3609f0d20f7208184f169fb871ee67f5f2917445683f70e4f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796961"
---
# <a name="network-management-functions"></a>Netzwerkverwaltungsfunktionen

Die Netzwerkverwaltungsfunktionen können wie folgt gruppiert werden.

## <a name="alert-functions"></a>Warnungsfunktionen



| Funktion                                   | Beschreibung                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRais**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Benachrichtigt alle registrierten Clients, dass ein bestimmtes Ereignis aufgetreten ist.                                                                                                                                  |
| [**NetAlertR generationsex**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Vereinfacht die Benachrichtigung registrierter Clients, dass ein bestimmtes Ereignis aufgetreten ist, da **netAlertR** dll im Gegensatz zu **NetAlertR dllEx** keine [**STD \_ ALERT-Struktur**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) erfordert. |



 

## <a name="api-buffer-functions"></a>API-Pufferfunktionen



| Funktion                                                 | Beschreibung                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Belegt Arbeitsspeicher aus dem Heap. Rufen Sie diese Funktion auf, wenn Sie Kompatibilität mit der **NetApiBufferFree-Funktion** benötigen. |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Gibt von der **NetApiBufferAllocate-Funktion** und anderen Netzwerkverwaltungsfunktionen belegten Arbeitsspeicher frei.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Ändert die Größe eines Puffers, der durch einen Aufruf der **NetApiBufferAllocate-Funktion** zugeordnet wird.                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Gibt die Größe eines Puffers in Bytes zurück, der durch einen Aufruf der **NetApiBufferAllocate-Funktion** zugeordnet wird.                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Azure Active Directory Joininformationsfunktionen



| Funktion                                                       | Beschreibung                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetFreeAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Gibt den für die angegebene [**DSREG \_ JOIN \_ INFO-Struktur**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) belegten Arbeitsspeicher frei, der Joininformationen für einen Mandanten enthält und die Sie durch Aufrufen der [**NetGetAadJoinInformation-Funktion**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) abgerufen haben. |
| [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Ruft die Joininformationen für den angegebenen Mandanten ab. Diese Funktion untersucht die Joininformationen für Microsoft Azure Active Directory und das Arbeitskonto, das der aktuelle Benutzer hinzugefügt hat.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Verzeichnisdienst- und Domänen join-Funktionen



| Funktion                                                                             | Beschreibung                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Fügt einen alternativen Namen für den angegebenen Computer hinzu.                                                                                                                                                                                                                      |
| [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Gibt ein Computerkonto für die spätere Verwendung in einem Offlinedomänen-Joinvorgang an.                                                                                                                                                                                        |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Listet Namen für den angegebenen Computer auf.                                                                                                                                                                                                                            |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Ruft eine Liste von Organisationseinheiten (OUs) ab, in denen ein Computerkonto erstellt werden kann.                                                                                                                                                                              |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Ruft Joinstatusinformationen für den angegebenen Computer ab.                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Verbindet einen Computer mit einer Arbeitsgruppe oder Domäne.                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Gibt ein Computerkonto für die spätere Verwendung in einem Offlinedomänen-Joinvorgang an.                                                                                                                                                                                       |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Entfernt einen alternativen Namen für den angegebenen Computer.                                                                                                                                                                                                                   |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Ändert den Namen eines Computers in einer Domäne.                                                                                                                                                                                                                             |
| [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | Wird lokal auf einem Computer ausgeführt, um ein Windows Betriebssystemimage zu ändern, das auf einem Volume eingebunden ist. Die Registrierung wird für das Image geladen, und die Bereitstellung von Blobdaten wird dort geschrieben, wo sie während der Abschlussphase eines Offlinedomänenbeitritts abgerufen werden können.     |
| [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | Wird lokal auf einem Computer ausgeführt, um ein Windows Betriebssystemimage zu ändern, das auf einem Volume eingebunden ist. Die Registrierung wird aus dem Image geladen, und Bereitstellungspaketdaten werden dort geschrieben, wo sie während der Abschlussphase eines Offlinedomänenbeitritts abgerufen werden können. |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Legt den Namen des primären Computers für den angegebenen Computer fest.                                                                                                                                                                                                              |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Entpackt einen Computer aus einer Arbeitsgruppe oder einer Domäne.                                                                                                                                                                                                                        |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Überprüft die Gültigkeit eines Computernamens, Arbeitsgruppennamens oder Domänennamens.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Get Functions



| Funktion                                                               | Beschreibung                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Gibt den Namen eines beliebigen Domänencontrollers für eine Domäne zurück, die von einem angegebenen Server direkt als vertrauenswürdig eingestuft wird.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Gibt den Namen des primären Domänencontrollers (PDC) für die angegebene Domäne zurück.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Gibt den Index des ersten Anzeigeinformationseintrags zurück, dessen Name mit einer angegebenen Zeichenfolge beginnt oder alphabetisch auf die Zeichenfolge folgt. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Gibt Benutzer-, Computer- oder globale Gruppenkontoinformationen zurück.                                                                             |



 

## <a name="group-functions"></a>Gruppenfunktionen



| Funktion                                     | Beschreibung                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Erstellt eine globale Gruppe.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Fügt einer vorhandenen globalen Gruppe einen Benutzer hinzu.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Entfernt eine globale Gruppe, unabhängig davon, ob die Gruppe Mitglieder hat.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Entfernt einen Benutzernamen aus einer globalen Gruppe.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Listet alle globalen Gruppen auf einem Server auf.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Gibt Informationen zu einer bestimmten globalen Gruppe zurück.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Listet alle Mitglieder einer bestimmten globalen Gruppe auf.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Legt allgemeine Informationen zu einer globalen Gruppe fest.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Weist einer neuen globalen Gruppe Mitglieder zu. ersetzt die Mitglieder einer vorhandenen Gruppe. |



 

## <a name="local-group-functions"></a>Lokale Gruppenfunktionen



| Funktion                                                   | Beschreibung                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Erstellt eine lokale Gruppe.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Fügt einer vorhandenen lokalen Gruppe einen oder mehrere Benutzer oder globale Gruppen hinzu.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Löscht eine lokale Gruppe und entfernt alle vorhandenen Mitglieder aus der Gruppe.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Entfernt mindestens ein Mitglied aus einer vorhandenen lokalen Gruppe.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Gibt Informationen zu jedem lokalen Gruppenkonto auf einem Server zurück.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Gibt Informationen zu einem bestimmten lokalen Gruppenkonto auf einem Server zurück. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Listet alle Mitglieder einer angegebenen lokalen Gruppe auf.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Legt allgemeine Informationen zu einer lokalen Gruppe fest.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Weist einer lokalen Gruppe Mitglieder zu.                                       |



 

## <a name="message-functions"></a>Nachrichtenfunktionen



| Funktion                                               | Beschreibung                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Sendet eine Nachricht an einen registrierten Nachrichtenalias.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registriert einen Nachrichtenalias in der Meldungsnamentabelle.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Löscht einen Nachrichtenalias aus der Meldungsnamentabelle.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Listet alle In der Meldungsnamentabelle gespeicherten Nachrichtenaliase auf.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Gibt Informationen zu einem bestimmten Nachrichtenalias in der Meldungsnamentabelle zurück. |



 

## <a name="netfile-functions"></a>NetFile-Funktionen



| Funktion                                | Beschreibung                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Erzwingt das Schließen einer Ressource.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Gibt Informationen zu geöffneten Dateien auf einem Server zurück.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Gibt Informationen zu einer bestimmten Öffnung einer Serverressource zurück. |



 

## <a name="remote-utility-functions"></a>Remote-Hilfsprogrammfunktionen



| Funktion                                                       | Beschreibung                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**NetRemoteComputerSupports**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Fragt den Redirector ab, um die optionalen Features abzurufen, die ein Remotesystem unterstützt. |
| [**NetRemoteTOD**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Ermöglicht Anwendungen den Zugriff auf die Informationen zur Tageszeit auf einem Remoteserver.          |



 

## <a name="schedule-functions"></a>Zeitplanfunktionen



| Funktion                                                                     | Beschreibung                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Übermittelt einen Auftrag, der zu einem bestimmten zukünftigen Datum und einer bestimmten Uhrzeit ausgeführt werden soll.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Bricht einen Bereich von Aufträgen in der Warteschlange ab, die auf einem Computer ausgeführt werden.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Listet die Aufträge in der Warteschlange auf einem angegebenen Computer auf.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Gibt Informationen zu einem bestimmten Auftrag zurück, der auf einem Computer in die Warteschlange gestellt wurde. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Ruft den Namen des AT-Dienstkontos ab.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Legt den Namen und das Kennwort des AT-Dienstkontos fest.                   |



 

## <a name="server-functions"></a>Serverfunktionen



| Funktion                                       | Beschreibung                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Gibt eine Liste der lokalen Laufwerke auf einem Server zurück.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Listet alle sichtbaren Server eines bestimmten Typs (oder Typs) in der angegebenen Domäne auf. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Gibt Konfigurationsinformationen zu einem angegebenen Server zurück.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Legt die Betriebsparameter für einen Server fest.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Server- und Arbeitsstationstransportfunktionen



| Funktion                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Bindet einen emulierten Servernamen an jedes der Transportprotokolle, in denen ein Server aktiv ist. (Kombiniert die Funktionen der [**NetServerTransportEnum-Funktion**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) und der [**NetServerTransportAddEx-Funktion.)**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Trennt jedes Netzwerktransportprotokoll von einem emulierten Servernamen, der durch einen vorherigen Aufruf der **NetServerComputerNameAdd-Funktion festgelegt** wurde.                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Bindet den angegebenen Server an das Transportprotokoll. (Diese Funktion unterstützt nur die [**SERVER \_ TRANSPORT INFO \_ \_ 0-Informationsebene.)**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Bindet den angegebenen Server an das Transportprotokoll. (Diese erweiterte Funktion unterstützt die [**Informationsebenen SERVER \_ TRANSPORT \_ INFO \_ 1,**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1) [**SERVER TRANSPORT INFO \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)und [**SERVER TRANSPORT INFO \_ \_ \_ 3.)**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Trennt das Transportprotokoll vom Server.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumeriert die vom Server verwalteten Transportprotokolle.                                                                                                                                                                                                                                                                   |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Listet die Transportprotokolle auf, die vom Redirector verwaltet werden.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Verwenden von Funktionen



| Funktion                               | Beschreibung                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Erstellt eine Verbindung zwischen einem lokalen Computer und einem Server.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Beendet eine Verbindung mit einer freigegebenen Ressource.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Listet alle aktuellen Verbindungen zwischen dem lokalen Computer und Ressourcen auf Remoteservern auf. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Gibt Informationen zu einer Verbindung mit einer freigegebenen Ressource zurück.                              |



 

## <a name="user-functions"></a>Benutzerfunktionen



| Funktion                                               | Beschreibung                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Fügt ein Benutzerkonto hinzu und weist ein Kennwort und eine Berechtigungsstufe zu.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Ändert das Kennwort eines Benutzers für einen angegebenen Netzwerkserver oder eine bestimmte Domäne. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Löscht ein Benutzerkonto vom Server.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Listet alle Benutzerkonten auf einem Server auf.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Gibt eine Liste der globalen Gruppennamen zurück, zu denen ein Benutzer gehört.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Gibt Informationen zu einem bestimmten Benutzerkonto auf einem Server zurück.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Gibt eine Liste lokaler Gruppennamen zurück, zu denen ein Benutzer gehört.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Legt globale Gruppenmitgliedschaften für ein angegebenes Benutzerkonto fest.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Legt das Kennwort und andere Elemente eines Benutzerkontos fest.             |



 

## <a name="user-modals-functions"></a>Benutzer modale Funktionen



| Funktion                                     | Beschreibung                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Gibt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank zurück, bei denen es sich um die SAM-Datenbank (Security Accounts Manager) oder im Fall von Domänencontrollern um Active Directory handelt. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Legt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank fest.                                                                                                                       |



 

## <a name="validation-functions"></a>Validierungsfunktionen



| Funktion                                                               | Beschreibung                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Gibt den Arbeitsspeicher frei, den die [**NetValidatePasswordPolicy-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) für den *OutputArg-Parameter* zuweist.                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Ermöglicht es einer Anwendung, die Kennwortkonformität für eine von der Anwendung bereitgestellte Kontodatenbank zu überprüfen und zu überprüfen, ob Kennwörter die Anforderungen an Komplexität, Fälligkeit, Mindestlänge und Verlaufswiederverwendung einer Kennwortrichtlinie erfüllen. |



 

## <a name="workstation-and-workstation-user-functions"></a>Benutzerfunktionen für Arbeitsstationen und Arbeitsstationen



| Funktion                                           | Beschreibung                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Gibt Informationen zu den Konfigurationselementen für eine Arbeitsstation zurück.             |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Konfiguriert eine Arbeitsstation.                                                           |
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Listet Informationen zu allen Benutzern auf, die derzeit bei der Arbeitsstation angemeldet sind.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Gibt Informationen zu einem derzeit angemeldeten Benutzer zurück.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Legt die benutzerspezifischen Informationen für die Konfigurationselemente einer Arbeitsstation fest. |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

-   [**NetAccessAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**NetAccessCheck**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**NetAccessDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**NetAccessEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**NetAccessGetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**NetAccessGetUserPerms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**NetAccessSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**NetAuditClear**](netauditclear.md)
-   [**NetAuditRead**](netauditread.md)
-   [**NetAuditWrite**](netauditwrite.md)
-   [**NetConfigGet**](netconfigget.md)
-   [**NetConfigGetAll**](netconfiggetall.md)
-   [**NetConfigSet**](netconfigset.md)
-   [**NetErrorLogClear**](neterrorlogclear.md)
-   [**NetErrorLogRead**](neterrorlogread.md)
-   [**NetErrorLogWrite**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**NetLocalGroupDelMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**NetServiceEnum**](netserviceenum.md)
-   [**NetServiceGetInfo**](netservicegetinfo.md)
-   [**NetServiceInstall**](netserviceinstall.md)
-   [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Netzwerkfunktionen](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 