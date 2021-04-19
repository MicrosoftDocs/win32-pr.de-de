---
description: Mithilfe des Windows-Sicherheitsmodells können Sie den Zugriff auf den Dienststeuerungs-Manager (Service Control Manager, SCM) und die Dienst Objekte steuern.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Dienst Sicherheit und Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352698"
---
# <a name="service-security-and-access-rights"></a>Dienst Sicherheit und Zugriffsrechte

Mithilfe des Windows-Sicherheitsmodells können Sie den Zugriff auf den Dienststeuerungs-Manager (Service Control Manager, SCM) und die Dienst Objekte steuern. Die folgenden Abschnitte enthalten ausführliche Informationen:

-   [Zugriffsrechte für den Dienststeuerungs-Manager](#access-rights-for-the-service-control-manager)
-   [Zugriffsrechte für einen Dienst](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Zugriffsrechte für den Dienststeuerungs-Manager

Im folgenden finden Sie die spezifischen Zugriffsrechte für den SCM.



| Zugriffsrecht                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_ Manager für \_ alle \_ Zugriffe** (0xF 003F)         | Beinhaltet zusätzlich zu allen Zugriffsrechten in dieser Tabelle die **\_ \_ erforderlichen Standard Rechte**.                                                                                                                                                                                                                                                                                 |
| **SC \_ Manager \_ - \_ Dienst erstellen** (0x0002)      | Erforderlich, um die [**Funktion "**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) -Funktion" aufzurufen, um ein Dienst Objekt zu erstellen und es der Datenbank hinzuzufügen.                                                                                                                                                                                                                                              |
| **SC \_ Manager \_ Connect** (0x0001)              | Ist erforderlich, um eine Verbindung mit dem Dienststeuerungs-Manager herzustellen.                                                                                                                                                                                                                                                                                                                      |
| **SC \_ Manager \_ Enumerate \_ Service** (0x0004)   | Erforderlich, um die Funktion " [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) " oder " [**enumservicesstatusex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) " aufzurufen, um die Dienste aufzulisten, die in der Datenbank enthalten sind.<br/> Muss die [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) -Funktion aufrufen, um Benachrichtigungen zu empfangen, wenn ein Dienst erstellt oder gelöscht wird.<br/> |
| **SC \_ Manager \_ Sperre** (0x0008)                 | Erforderlich, um die [**lockservicedatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) -Funktion aufzurufen, um eine Sperre für die Datenbank zu erhalten.                                                                                                                                                                                                                                                      |
| **SC \_ Manager \_ Ändern der \_ Start \_ Konfiguration** (0x0020) | Erforderlich, um die [**notifybootconfigstatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) -Funktion aufzurufen.                                                                                                                                                                                                                                                                                  |
| **SC \_ Status der Manager- \_ Abfrage \_ Sperre \_** (0x0010)  | Ist erforderlich, um die [**queryservicelockstatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) -Funktion zum Abrufen der Sperr Statusinformationen für die Datenbank aufzurufen.                                                                                                                                                                                                                         |



 

Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für den SCM.



<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Ein Prozess mit den richtigen Zugriffsrechten kann ein Handle für den SCM öffnen, das in den Funktionen [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**enumservicesstatusex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)und [**queryservicelockstatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) verwendet werden kann. Nur Prozesse mit Administrator Rechten können Handles für den SCM öffnen, der von den Funktionen "up Service [**Service**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " und " [**lockservicedatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) " verwendet werden kann.

Das System erstellt die Sicherheits Beschreibung für den SCM. Um die Sicherheits Beschreibung für den SCM abzurufen oder festzulegen, verwenden Sie die Funktionen [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) und [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) mit einem Handle für das scmanager-Objekt.

**Windows Server 2003 und Windows XP:** Im Gegensatz zu den meisten anderen Sicherungs fähigen Objekten kann die Sicherheits Beschreibung für den SCM nicht geändert werden. Dieses Verhalten hat sich seit Windows Server 2003 mit Service Pack 1 (SP1) geändert.

Die folgenden Zugriffsrechte werden gewährt.



<table>
<thead>
<tr class="header">
<th>Konto</th>
<th>Zugriffsrechte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Remote authentifizierte Benutzer</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Lokale authentifizierte Benutzer (einschließlich "LocalService" und "Network Service")</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administratoren</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Beachten Sie, dass sich Remote Benutzer, die über das Netzwerk authentifiziert, aber nicht interaktiv angemeldet sind, mit dem SCM verbinden, aber keine Vorgänge ausführen müssen, die andere Zugriffsrechte erfordern. Um diese Vorgänge auszuführen, muss der Benutzer interaktiv angemeldet sein, oder der Dienst muss eines der Dienst Konten verwenden.

**Windows Server 2003 und Windows XP:** Remote authentifizierte Benutzer erhalten den **SC \_ Manager \_ Connect**-, **SC \_ Manager- \_ enumerationsdienst \_**, **SC-Manager- \_ \_ Abfrage \_ Sperr \_ Status** und **Standard \_ Rechte \_ Lese** Zugriffsrechte. Diese Zugriffsrechte werden wie in der vorherigen Tabelle unter Windows Server 2003 mit SP1 beschrieben eingeschränkt.

Wenn ein Prozess die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion verwendet, um ein Handle für eine Datenbank installierter Dienste zu öffnen, kann er Zugriffsrechte anfordern. Das System führt vor dem Erteilen der angeforderten Zugriffsrechte eine Sicherheitsüberprüfung für die Sicherheits Beschreibung für den SCM aus.

## <a name="access-rights-for-a-service"></a>Zugriffsrechte für einen Dienst

Im folgenden finden Sie die spezifischen Zugriffsrechte für einen Dienst.



| Zugriffsrecht                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dienst \_ Sämtlicher \_ Zugriff** (0xF 01FF)          | Enthält die Standard Rechte, die zusätzlich zu allen Zugriffsrechten in dieser Tabelle **\_ \_ erforderlich** sind.                                                                                                                                                                                                                                                                                              |
| **Dienst \_ Ändern der \_ Konfiguration** (0x0002)        | Erforderlich, um die [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) -oder [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion aufzurufen, um die Dienst Konfiguration zu ändern. Da dem Aufrufer das Recht erteilt wird, die ausführbare Datei zu ändern, die das System ausführt, sollte er nur Administratoren gewährt werden.                                                              |
| **Dienst \_ \_Abhängige Elemente aufzählen** (0x0008) | Ist erforderlich, um die [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) -Funktion aufzurufen, um alle vom Dienst abhängigen Dienste aufzuzählen.                                                                                                                                                                                                                                         |
| **Dienst \_ Abfrage** (0x0080)           | Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion aufzurufen, um den Dienst aufzufordern, seinen Status sofort zu melden.                                                                                                                                                                                                                                                          |
| **Dienst \_ \_Anhalten Fortsetzen** (0x0040)       | Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion aufzurufen, um den Dienst anzuhalten oder fortzusetzen.                                                                                                                                                                                                                                                                             |
| **Dienst \_ Abfrage \_ Konfiguration** (0x0001)         | Erforderlich, um die [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) -Funktion und die [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) -Funktion zum Abfragen der Dienst Konfiguration aufzurufen.                                                                                                                                                                                                           |
| **Dienst \_ Abfrage \_ Status** (0x0004)         | Ist erforderlich, um die Funktion [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) oder [**queryservicestatusex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) aufzurufen, um den Dienststeuerungs-Manager über den Status des Dienstanbieter zu Fragen.<br/> Muss die [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) -Funktion aufrufen, um Benachrichtigungen zu empfangen, wenn der Status eines Diensts geändert wird.<br/> |
| **Dienst \_ Start** (0x0010)                 | Erforderlich zum Aufrufen der [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) -Funktion zum Starten des Dienstanbieter.                                                                                                                                                                                                                                                                                             |
| **Dienst \_ Beendigung** (0x0020)                  | Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion zum Abbrechen des dienstandens aufzurufen.                                                                                                                                                                                                                                                                                          |
| **Dienst \_ Benutzer \_ definiertes \_ Steuer** Element (0x0100) | Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion aufzurufen, um einen benutzerdefinierten Steuerelement Code anzugeben.                                                                                                                                                                                                                                                                       |



 

Im folgenden finden Sie die [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) für einen Dienst.



| Zugriffsrecht                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zugreifen auf die \_ System \_ Sicherheit** | Erforderlich, um die [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) -oder [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion für den Zugriff auf die SACL aufzurufen. Die richtige Möglichkeit, um diesen Zugriff zu erhalten, besteht darin, die [**Berechtigung**](/windows/desktop/SecAuthZ/privileges) " **SE \_ Security \_ Name**" im aktuellen Zugriffs Token des Aufrufers zu aktivieren, das Handle für den **Zugriff auf \_ System \_ Sicherheits** Zugriff zu öffnen und die Berechtigung zu deaktivieren. |
| **Löschen**   (0x10000)       | Zum Aufrufen der Funktion " [**Delta**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) Service" erforderlich, um den Dienst zu löschen.                                                                                                                                                                                                                                                                                                                                                  |
| **Lesen Sie \_ Steuer**  Element (0x20000)    | Erforderlich, um die Funktion [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) aufzurufen, um die Sicherheits Beschreibung des Dienst Objekts abzufragen.                                                                                                                                                                                                                                                                                  |
| **Schreiben \_ DAC**  (0x40000)    | Zum Aufrufen der [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion erforderlich, um den **DACL** -Member der Sicherheits Beschreibung des Dienst Objekts zu ändern.                                                                                                                                                                                                                                                                   |
| **Schreiben \_ Besitzer** (0x80000)   | Erforderlich zum Aufrufen der [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion zum Ändern des **Besitzers** und der **Gruppen** Mitglieder der Sicherheits Beschreibung des Dienst Objekts.                                                                                                                                                                                                                                                   |



 

Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für einen Dienst.



<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Der SCM erstellt die Sicherheits Beschreibung eines Dienst Objekts, wenn der Dienst von der Funktion "| [**ateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " installiert wird. Die Standard Sicherheits Beschreibung eines Dienst Objekts gewährt den folgenden Zugriff.



<table>
<thead>
<tr class="header">
<th>Konto</th>
<th>Zugriffsrechte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Remote authentifizierte Benutzer</td>
<td>Standardmäßig nicht erteilt. <strong>Windows Server 2003 mit SP1: SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 und Windows XP:</strong> Die Zugriffsrechte für Remote authentifizierte Benutzer sind identisch mit denen für lokale authentifizierte Benutzer.<br/></td>
</tr>
<tr class="even">
<td>Lokale authentifizierte Benutzer (einschließlich "LocalService" und "Network Service")</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administratoren</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Zum Ausführen von Vorgängen muss der Benutzer interaktiv angemeldet sein, oder der Dienst muss eines der Dienst Konten verwenden.

Um die Sicherheits Beschreibung für ein Dienst Objekt abzurufen oder festzulegen, verwenden Sie die Funktionen [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) und [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Weitere Informationen finden Sie unter [Ändern der DACL für einen Dienst](modifying-the-dacl-for-a-service.md).

Wenn ein Prozess die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion verwendet, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Dienst Objekts.

Das erteilen bestimmter Zugriffsrechte für nicht vertrauenswürdige Benutzer (z. b. **\_ \_ Konfiguration von Dienst Änderungen** oder **Dienst \_ Stopps**) kann es Ihnen ermöglichen, die Ausführung des Dienstanbieter zu beeinträchtigen und möglicherweise das Ausführen von Anwendungen unter dem LocalSystem-Konto zuzulassen.

Wenn die [**enumservicesstatusex-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) aufgerufen wird und der Aufrufer nicht über das Zugriffsrecht des **Dienst \_ Abfrage \_ Status** für einen Dienst verfügt, wird der Dienst aus der Liste der an den Client zurückgegebenen Dienste im Hintergrund weggelassen.

 

