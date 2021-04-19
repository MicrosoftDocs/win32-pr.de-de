---
title: EAPHost-Peer Methoden Strukturen
description: Erfahren Sie mehr über EAPHost-Peer Methoden-API-Strukturen wie eapcertifikatecredential und eapsimcredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339099"
---
# <a name="eaphost-peer-method-structures"></a>EAPHost-Peer Methoden Strukturen

Die API-Strukturen der EAPHost-Peer Methode lauten wie folgt.



| Struktur                                                              | BESCHREIBUNG                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eapcertifialisiecredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Enthält Informationen über das Zertifikat, das von der EAP-Methode für die Authentifizierung verwendet wird.                                                                                                            |
| [**Eapcredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Enthält Informationen zum Typ der Anmelde Informationen und den entsprechenden Anmelde Informationen. Dies wird als Eingabe an die [**eappeergetconfigblobanduserblob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) -API übermittelt. |
| [**EAP- \_ Peer \_ Methoden \_ Routinen**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Enthält einen Satz von Funktions Zeigern für die EAPHost-Peer Methoden-APIs.                                                                                                                               |
| [**Eappeermethodoutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Enthält die Aktions Informationen, die von einer EAP-Peer Methode zurückgegeben werden.                                                                                                                                    |
| [**Eappeermethodresult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Enthält Ergebnisdaten, die während der Authentifizierung von einer EAP-Methode generiert wurden.                                                                                                                             |
| [**Eapsimcredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Enthält Informationen über die SIM-Daten, die von der EAP-Methode für die Authentifizierung verwendet werden.                                                                                                              |
| [**Eapusernamepasswordcredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Enthält den Benutzernamen und das Kennwort, die von der EAP-Methode zum Authentifizieren des Benutzers verwendet werden.                                                                                                     |



 

 

 




