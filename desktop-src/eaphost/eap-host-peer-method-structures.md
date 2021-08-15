---
title: EAPHost-Peermethodenstrukturen
description: Erfahren Sie mehr über EAPHost-Peermethoden-API-Strukturen wie EapCertificateCredential und EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56582c920536cabd294680df265d16ae51d8b4bd951f8efcdb988de677a2a2ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498619"
---
# <a name="eaphost-peer-method-structures"></a>EAPHost-Peermethodenstrukturen

Die EAPHost-Peermethoden-API-Strukturen sind wie folgt.



| Struktur                                                              | BESCHREIBUNG                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Enthält Informationen über das Zertifikat, das von der EAP-Methode für die Authentifizierung verwendet wird.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Enthält Informationen über den Anmeldeinformationstyp und die entsprechenden Anmeldeinformationen. Dies wird als Eingabe an die [**EapPeerGetConfigBlobAndUserBlob-API**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) übergeben. |
| [**\_ \_ EAP-PEERMETHODENROUTINEN \_**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Enthält eine Reihe von Funktionszeigern auf die EAPHost-Peermethoden-APIs.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Enthält die Aktionsinformationen, die von einer EAP-Peermethode zurückgegeben werden.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Enthält Ergebnisdaten, die von einer EAP-Methode während der Authentifizierung generiert werden.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Enthält Informationen über die SIM, die von der EAP-Methode für die Authentifizierung verwendet wird.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Enthält den Benutzernamen und das Kennwort, die von der EAP-Methode zum Authentifizieren des Benutzers verwendet werden.                                                                                                     |



 

 

 




