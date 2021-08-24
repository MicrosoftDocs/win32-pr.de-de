---
description: Listet die Schnittstellen in Authentifizierungs-APIs auf.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Authentifizierungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843385004095499a59593bf548ff21998c4079e48667ea0e472e4a55d1f57ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141403"
---
# <a name="authentication-interfaces"></a>Authentifizierungsschnittstellen

Authentifizierungsschnittstellen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Smartcardschnittstellen](#smart-card-interfaces)
-   [Schnittstellen für die Identitätsfreigabe](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Smartcardschnittstellen

Das Smartcard-SDK stellt die folgenden COM-Schnittstellen bereit. Die Methoden für eine bestimmte Schnittstelle sind im Inhaltsverzeichnis und auf der Referenzseite für diese Schnittstelle aufgeführt.



| Schnittstelle                                    | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Verwaltet ein Streamobjekt.                                                                                                                                                                 |
| [**ISCard**](iscard.md)                     | Öffnet und verwaltet eine Verbindung mit einer [*Smartcard.*](/windows/desktop/SecGloss/s-gly)                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Authentifiziert eine Anwendung, eine Smartcard oder einen Benutzer.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Erstellt und verwaltet eine [*Smartcard-APDU (Application Protocol Data Unit).*](/windows/desktop/SecGloss/a-gly) |
| [**ISCardDatabase**](iscarddatabase.md)     | Führt [*Smartcard-Ressourcen-Manager-Datenbankvorgänge*](/windows/desktop/SecGloss/r-gly) aus.                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Führt allgemeine Dateidienste wie das Suchen, Auswählen, Lesen, Schreiben, Erstellen und Löschen von Dateien aus.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Erstellt einen APDU-Befehl.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Sucht eine Smartcard.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Verwaltet das Smartcardsystem.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Stellt Methoden bereit, die zur Unterstützung anderer Smartcard-COM-Schnittstellen verwendet werden. Diese Schnittstelle wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und sollte nicht mehr verwendet werden.                               |
| [**ISCardVerify**](iscardverify.md)         | Überprüft oder ändert die Richtlinie zur Überprüfung des Karteninhabers (Card Holder Verification, CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Schnittstellen für die Identitätsfreigabe

Das Identity Sharing SDK stellt die folgenden COM-Schnittstellen bereit. Die Methoden für eine bestimmte Schnittstelle sind im Inhaltsverzeichnis und auf der Referenzseite für diese Schnittstelle aufgeführt.



| Schnittstelle                                                          | BESCHREIBUNG                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Ermöglicht einem Identitätsanbieter das Zuordnen von Identitäten zu lokalen Benutzerkonten.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Ermöglicht es einem Identitätsanbieter, eine aufrufende Anwendung zu benachrichtigen, wenn eine Identität aktualisiert wird. |
| [**IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Stellt einen Identitätsanbieter dar.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Stellt Methoden zum Aufzählen und Verwalten von Identitäten und Identitätsanbietern bereit.              |



 

 

 
