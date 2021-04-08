---
description: Bei einem Systemspeicher handelt es sich um eine Sammlung, die aus einem oder mehreren physischen gleich geordneten speichern besteht.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: System Speicherorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959867"
---
# <a name="system-store-locations"></a>System Speicherorte

Bei einem Systemspeicher handelt es sich um eine Sammlung, die aus einem oder mehreren physischen gleich geordneten speichern besteht. Für jeden Systemspeicher sind vordefinierte physische neben geordnete Speicher vorhanden. Nachdem Sie einen Systemspeicher geöffnet haben, z. b. "My at \_ System \_ Store \_ Current \_ User", ruft der Speicher Anbieter " [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) " auf, um jeden physischen Speicher in der Sammlung "Systemspeicher" zu öffnen. Im geöffneten Prozess wird jeder dieser physischen Speicher mithilfe von [**certaddstoretocollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)der Systemspeicher Sammlung hinzugefügt. Alle Zertifikate in diesen physischen Speichern sind über die Sammlung logischer Systemspeicher verfügbar.

Die vordefinierten Systemspeicher Orte für jeden System Speicherort sind:

-   MY
-   Root
-   Vertrauensstellung
-   CA

In CERT \_ System \_ Store \_ aktueller \_ Benutzer gibt es auch einen vordefinierten userds-Speicher. Für diesen Standort ist ein smartcardspeicher geplant.

Im folgenden finden Sie die Systemspeicher, auf die weitere Hinweise folgt:

-   [Zertifikat \_ System \_ Speicher \_ aktueller \_ Benutzer](#cert_system_store_current_user)
-   [\_lokaler Zertifikat System \_ Speicher- \_ \_ Computer](#cert_system_store_local_machine)
-   [\_ \_ \_ Aktueller Dienst des Zertifikat System Stores \_](#cert_system_store_current_service)
-   [Zertifikat- \_ System \_ Speicher \_ Dienste](#cert_system_store_services)
-   [Zertifikat \_ System \_ Speicher- \_ Benutzer](#cert_system_store_users)
-   [\_ \_ \_ Richtlinie zur aktuellen \_ Benutzer \_ Gruppe des Zertifikat Systems](#cert_system_current_user_group_policy)
-   [\_ \_ \_ \_ Gruppen \_ Richtlinie für den lokalen Zertifikat System Computer](#cert_system_local_machine_group_policy)
-   [\_Enterprise-Zertifikat System \_ Speicher \_ lokaler \_ Computer \_](#cert_system_store_local_machine_enterprise)
-   [Anmerkungen](#remarks)

### <a name="cert_system_store_current_user"></a>Zertifikat \_ System \_ Speicher \_ aktueller \_ Benutzer

\_ \_ Systemspeicher für Systemspeicher im Zertifikat Systemspeicher \_ \_ befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.



| System Speicher | Physischer Speicher                                           |
|--------------|----------------------------------------------------------|
| MY           | . Vorgegebene                                                 |
| Root         | . Default. LocalMachine<br/> . Smartcard<br/>   |
| Vertrauensstellung        | . Default. GroupPolicy<br/> . LocalMachine<br/> |
| CA           | . Default. GroupPolicy<br/> . LocalMachine<br/> |
| Userds       | . UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>\_lokaler Zertifikat System \_ Speicher- \_ \_ Computer

\_ \_ \_ Systemspeicher des lokalen Zertifikat System Speichers \_ befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Die vordefinierten physischen Speicher sind diesen System speichern folgendermaßen zugeordnet.



| System Speicher | Physischer Speicher                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Vorgegebene                                                                                          |
| Root         | . Default. AuthRoot<br/> . GroupPolicy<br/> . Fangen<br/> . Smartcard<br/> |
| Vertrauensstellung        | . Default. GroupPolicy<br/> . Fangen<br/>                                            |
| CA           | . Default. GroupPolicy<br/> . Fangen <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>\_ \_ \_ Aktueller Dienst des Zertifikat System Stores \_

\_ \_ \_ \_ Die aktuellen Dienst System Speicher des Zertifikat System Speichers befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.



| System Speicher | Physischer Speicher                   |
|--------------|----------------------------------|
| MY           | . Vorgegebene                         |
| Root         | . Default. LocalMachine<br/> |
| Vertrauensstellung        | . Default. LocalMachine<br/> |
| CA           | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>Zertifikat- \_ System \_ Speicher \_ Dienste

Systemspeicher für Zertifikat \_ System \_ Speicher \_ Dienste befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.



| System Speicher       | Physischer Speicher                   |
|--------------------|----------------------------------|
| Dienst Name \\ My    | . Vorgegebene                         |
| Dienst \\ Name Stamm  | . Default. LocalMachine<br/> |
| ServiceName- \\ Vertrauensstellung | . Default. LocalMachine<br/> |
| Dienst Name ( \\ ca)    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>Zertifikat \_ System \_ Speicher- \_ Benutzer

\_Systemspeicher für Zertifikat System \_ Speicher- \_ Benutzer befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.



| System Speicher  | Physischer Speicher                   |
|---------------|----------------------------------|
| Benutzer-ID \\ My    | . Default. LocalMachine<br/> |
| UserID \\ -Stamm  | . Default. LocalMachine<br/> |
| UserID- \\ Vertrauensstellung | . Default. LocalMachine<br/> |
| UserID- \\ ca    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>\_ \_ \_ Richtlinie zur aktuellen \_ Benutzer \_ Gruppe des Zertifikat Systems

\_ \_ \_ \_ Systemspeicher der aktuellen Benutzergruppen Richtlinien für Zertifikat Systeme \_ befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>\_ \_ \_ \_ Gruppen \_ Richtlinie für den lokalen Zertifikat System Computer

\_ \_ \_ \_ \_ Systemspeicher für die Gruppenrichtlinien-Systemspeicher des Zertifikat Systems befinden sich am folgenden Registrierungs Speicherort:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>\_Enterprise-Zertifikat System \_ Speicher \_ lokaler \_ Computer \_

\_ \_ \_ \_ \_ Enterprise Enterprise Enterprise Computer Enterprise enthält Zertifikate, die Domänen übergreifend im Unternehmen freigegeben und aus dem globalen Unternehmensverzeichnis heruntergeladen wurden Um den Unternehmens Speicher des Clients zu synchronisieren, wird das Unternehmensverzeichnis alle acht Stunden abgerufen, und Zertifikate werden automatisch im Hintergrund heruntergeladen.

Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher sind wie folgt.



| System Speicher | Physischer Speicher |
|--------------|----------------|
| MY           | . Vorgegebene       |
| Root         | . Vorgegebene       |
| Vertrauensstellung        | . Vorgegebene       |
| CA           | . Vorgegebene       |



 

### <a name="remarks"></a>Bemerkungen

Weitere physische Speicher können einem Systemspeicher mithilfe von [**certregisterphysicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)zugeordnet werden.

Die \_ Speicher des Zertifikats System \_ Speicher \_ Dienstanbieter-und Zertifikat \_ System \_ Speichers \_ werden geöffnet, indem der Name des Speichers in der Zeichenfolge, die an *pvpara* übergeben wird, mit dem Dienst-oder Benutzernamen, wie z. b. *ServiceName* \\ **Trust** oder, **Standardeinstellung** \\ **My**. Der Speicherort des Zertifikats Systemspeicher Diensts oder des Zertifikats \_ \_ \_ \_ Systemspeicher Benutzers \_ \_ kann denselben Speicher im Zertifikat \_ System \_ Current \_ Service oder CERT \_ System \_ Store \_ Current \_ User mithilfe der [*textsicherheits*](../secgloss/s-gly.md) -ID (SID) des aktuellen Diensts oder Benutzers öffnen.

Filialen in \_ der System \_ Speicher \_ \_ -Benutzergruppen \_ Richtlinie und der Zertifikat \_ System- \_ Gruppenrichtlinie für den lokalen \_ \_ \_ Computer in einer Netzwerk Einstellung werden beim Computer Start oder bei der Benutzeranmeldung von der Gruppenrichtlinie Vorlage (GPT) auf den Client Computer heruntergeladen. Diese Speicher können nach dem Start oder der Anmeldung auf dem Client Computer aktualisiert werden, wenn der GPT von einem Administrator auf dem Domänen Server geändert wird. Mit der [**certcontrolstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) -Funktion kann eine Anwendung benachrichtigt werden, wenn sich die Filialen an einem dieser Standorte geändert haben.

Die folgenden Systemspeicher Orte können Remote geöffnet werden:

-   \_lokaler Zertifikat System \_ Speicher- \_ \_ Computer
-   \_ \_ \_ \_ \_ Gruppen \_ Richtlinie für den lokalen Zertifikat System Speicher
-   Zertifikat- \_ System \_ Speicher \_ Dienste
-   Zertifikat \_ System \_ Speicher- \_ Benutzer

System Speicherorte werden Remote geöffnet, indem der Speicher Name in der Zeichenfolge, die an *pvpara* übergeben wird, mit dem Computernamen vorangestellt wird. Beispiele für Remote System-Speicher Namen:

-   *Computername* \\  Zertifizierungsstelle
-   \\\\*Computername* \\  Zertifizierungsstelle
-   *Computername* \\ *Dienst Name* \\ **Vertrauens** Stellung
-   \\\\*Computername* \\ *Dienst Name* \\ **Vertrauens** Stellung

 

 
