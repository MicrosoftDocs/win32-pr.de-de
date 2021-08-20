---
title: Übertragen von Daten zwischen den Supplicant- und EAP-Methoden
description: Erfahren Sie mehr über das Übertragen von Daten zwischen den Supplicant- und EAP-Methoden. Das Übertragen von Daten zwischen Methoden erfolgt mithilfe von EAP-Attributen.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7675cac2c7e147804bc4c5ec86304e75063964bdc54cd44519fe535e28783f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085651"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Übertragen von Daten zwischen den Supplicant- und EAP-Methoden

Die Verwendung von EAP-Attributen ermöglicht den Austausch von Daten zwischen Supplicants und EAP-Methoden.

## <a name="attribute-consumption"></a>Attributverbrauch

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) verwendet EAP-Attribute, die direkt an die konfigurierte EAP-Methode übergeben werden. Auf ähnliche Weise können EAP-Methoden einen Aktionscode zurückgeben, der dem Supplicant angibt, dass Attribute verfügbar sind und dass die Attribute mithilfe von [**EapHostPeerGetResponseAttributes gesammelt**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes)werden sollen.

Weitere Informationen finden Sie in den folgenden Themen.

-   [EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [EAP Authenticator Methodenaktionscodes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Es wird erwartet, dass Supplicants Attribute ignorieren, die sie nicht erkennen oder nicht verwenden können. Mit [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) werden diese ignorierten Attribute zurück an EAPHost und die EAP-Methode gesendet.

## <a name="vendor-specific-attributes"></a>Herstellerspezifische Attribute

Mithilfe des anbieterspezifischen EAP-Attributs können EAP-Methoden und -Supplicants für einen bestimmten Zweck in den Datenaustausch einschreiten. Anbieterspezifische Attribute werden von Unterstützungen und Methoden ignoriert, die das anbieterspezifische Attribut nicht unterstützen.

Weitere Informationen finden Sie in den folgenden Themen.

-   [EAP-Attribute](about-eap-attributes.md).
-   [**EAP \_ \_ATTRIBUTTYP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der EAP-Benutzeroberfläche](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Aktivieren Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




