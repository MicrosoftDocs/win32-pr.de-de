---
description: Listet die Schnittstellen in den Authentifizierungs-APIs auf.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Authentifizierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216544"
---
# <a name="authentication-interfaces"></a>Authentifizierungs Schnittstellen

Authentifizierungs Schnittstellen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Smartcardschnittstellen](#smart-card-interfaces)
-   [Identitäts Freigabe Schnittstellen](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Smartcardschnittstellen

Das Smartcard-SDK stellt die folgenden COM-Schnittstellen bereit. Die Methoden für eine bestimmte Schnittstelle werden im Inhaltsverzeichnis und auf der Referenzseite für diese Schnittstelle aufgelistet.



| Schnittstelle                                    | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ibytebuffer**](ibytebuffer.md)           | Verwaltet ein Stream-Objekt.                                                                                                                                                                 |
| [**Iscard**](iscard.md)                     | Öffnet und verwaltet eine Verbindung mit einer [*Smartcard*](/windows/desktop/SecGloss/s-gly).                                                                    |
| [**Iscardauth**](iscardauth.md)             | Authentifiziert eine Anwendung, eine Smartcard oder einen Benutzer.                                                                                                                                       |
| [**Iscardcmd**](iscardcmd.md)               | Erstellt und verwaltet eine Smartcard-APDU ( [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) ). |
| [**Iscarddatabase**](iscarddatabase.md)     | Führt Smartcard- [*Ressourcen-Manager*](/windows/desktop/SecGloss/r-gly) -Daten Bank Vorgänge aus                                              |
| [**Iscardfileaccess**](iscardfileaccess.md) | Führt allgemeine Dateidienste aus, z. b. suchen, auswählen, lesen, schreiben, erstellen und Löschen von Dateien.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Erstellt einen APDU-Befehl.                                                                                                                                                              |
| [**Iscardsuche**](iscardlocate.md)         | Es wird eine Smartcard angezeigt.                                                                                                                                                                    |
| [**Iscardmanage**](iscardmanage.md)         | Verwaltet das Smartcardsystem.                                                                                                                                                           |
| [**Iscardtypeconfiguration**](iscardtypeconv.md)     | Stellt Methoden zur Unterstützung anderer Smartcard-com-Schnittstellen bereit. Diese Schnittstelle wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und sollte nicht mehr verwendet werden.                               |
| [**Iscardverify**](iscardverify.md)         | Überprüft oder ändert die Richtlinie der Karteninhaber Überprüfung (CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Identitäts Freigabe Schnittstellen

Das Identitäts Freigabe-SDK stellt die folgenden COM-Schnittstellen bereit. Die Methoden für eine bestimmte Schnittstelle werden im Inhaltsverzeichnis und auf der Referenzseite für diese Schnittstelle aufgelistet.



| Schnittstelle                                                          | BESCHREIBUNG                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Iassociatedidentityprovider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Ermöglicht einem Identitäts Anbieter das Zuordnen von Identitäten zu lokalen Benutzerkonten.            |
| [**Iidentityrat**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Ermöglicht einem Identitäts Anbieter, eine aufrufende Anwendung zu benachrichtigen, wenn eine Identität aktualisiert wird. |
| [**Iidentityprovider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Stellt einen Identitätsanbieter dar.                                                         |
| [**Iidentitystore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Stellt Methoden zum Auflisten und Verwalten von Identitäten und Identitäts Anbietern bereit.              |



 

 

 
