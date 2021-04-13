---
title: Übertragen von Daten zwischen den Supplicant-und EAP-Methoden
description: Weitere Informationen zum Übertragen von Daten zwischen den Supplicant-und EAP-Methoden. Das Übertragen von Daten zwischen Methoden erfolgt mithilfe von EAP-Attributen.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391026"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Übertragen von Daten zwischen den Supplicant-und EAP-Methoden

Die Verwendung von EAP-Attributen ermöglicht das Austauschen von Daten zwischen Supplicants und EAP-Methoden.

## <a name="attribute-consumption"></a>Attribut Verbrauch

[**Eaphostpeerbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) verwendet EAP-Attribute, die direkt an die konfigurierte EAP-Methode übermittelt werden. Ebenso können EAP-Methoden einen Aktions Code zurückgeben, der dem Supplicant angibt, dass Attribute verfügbar sind, und dass die Attribute mithilfe von [**eaphostpeergetresponseattribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes)erfasst werden sollen.

Weitere Informationen finden Sie in den nachfolgenden Themen.

-   Der [EAP-Peer-Supplicant-Aktions Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Grund Codes der EAP-Peer Supplicant](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Aktions Codes der EAP-Authenticator-Methode](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Supplicants wird erwartet, dass Attribute ignoriert werden, auf die Sie nicht reagieren oder nicht. Bei Verwendung von [**eaphostpeerablattribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) werden diese ignorierten Attribute zurück an EAPHost und die EAP-Methode gesendet.

## <a name="vendor-specific-attributes"></a>Anbieterspezifische Attribute

Durch die Verwendung des anbieterspezifischen EAP-Attributs können EAP-Methoden und Supplicants den Datenaustausch zu einem bestimmten Zweck einbinden. Anbieterspezifische Attribute werden von Supplicants und Methoden ignoriert, die das herstellerspezifische Attribut nicht unterstützen.

Weitere Informationen finden Sie in den nachfolgenden Themen.

-   [EAP-Attribute](about-eap-attributes.md).
-   [**EAP \_ \_Attributtyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Benutzeroberfläche der EAP-Methode](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Aktivieren von Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




