---
title: Implementieren der NAP-Unterstützung für EAP-Methoden
description: Erfahren Sie, wie Sie die NAP-Unterstützung für einen EAPHost-Supplicant implementieren. Weitere Informationen finden Sie unter EAPHost-bezogene NAP-Themen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104039879"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementieren der NAP-Unterstützung für EAP-Methoden

In diesem Thema wird erläutert, wie NAP für einen EAPHost-Supplicant implementiert wird. In Windows Vista und Windows Server 2008 ist ein NAP-Erzwingungs Client (NAP EC) für authentifizierte [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Verbindungen verfügbar.

## <a name="implementing-network-access-protection-nap"></a>Implementieren von Netzwerk Zugriffsschutz (Network Access Protection, NAP)

Zur Unterstützung von NAP implementiert ein EAPHost-Supplicant eine Rückruffunktion, die mit dem [**notificationhandler**](/previous-versions/windows/desktop/api) -Rückruf Prototyp übereinstimmt und einen Zeiger auf diese Rückruffunktion bereitstellen muss, wenn [**eaphostpeer erbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)aufgerufen wird.

Die Rückruffunktion nimmt zwei Parameter an.

-   Eine GUID, die die der Authentifizierung zugeordnete-Schnittstelle eindeutig identifiziert.
-   Ein void-Zeiger auf eine nicht transparente Datenstruktur, die vom Supplicant bereitgestellt wird.

EAPHost Ruft die vom Supplicant bereitgestellte Rückruffunktion mit der eindeutigen Schnittstellen-GUID und dem void-Zeiger auf, wenn sich der Quarantäne Zustand des Computers ändert. Wenn EAPHost die von Supplicant bereitgestellte Rückruffunktion aufruft, antwortet der Supplicant, indem er die vom Schnittstellen-GUID/void-Zeiger identifizierte logische Netzwerkverbindung abbricht und die Authentifizierung mit **eaphostpeer erbeginsession** erneut startet.

EAPHost kann die vom Supplicant bereitgestellte Rückruffunktion jederzeit aufrufen: vor, während einer aktiven Authentifizierung oder nach Abschluss der Authentifizierung (nachdem [**eaphostpeer-EndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) aufgerufen wurde, aber nicht vor dem Aufrufen von [**eaphostpeer-clearconnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ). Der Supplicant sollte immer Antworten, indem er die logische Netzwerkverbindung abbricht und erneut authentifiziert.

Wenn der Supplicant heruntergefahren oder nicht mehr benachrichtigt wird, dass der Isolations Status nicht mehr empfangen werden kann, sollte der Supplicant [**eaphostpeer-clearconnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) aufrufen und die entsprechende Schnittstellen-GUID angeben. Wenn der Supplicant die Isolation der Verbindung des logischen Netzwerks ermitteln möchte, kann der Supplicant diese Informationen von **eaphostpeer. isolationstate** abrufen, wenn [**eaphostpeer-methodresult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) von [**eaphostpeer ergetresult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)abgerufen wird.

## <a name="eaphost-related-nap-information"></a>EAPHost Verwandte NAP-Informationen

Informationen zu NAP-Informationen für die EAPHost-API finden Sie in den folgenden Themen.

-   [**EAP \_ - \_ Attributtyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**EAP- \_ Fehler**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Häufig gestellte Fragen zu EAPHost-Supplicant](eaphost-supplicant-frequently-asked-questions.md)
-   [**Eigenschaften der EAP-Methode**](eap-method-properties.md)
-   [**Eaphosteterbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**EAP-bezogene Fehler-und Informations Konstanten**](eap-related-error-and-information-constants.md)
-   [**Isolations \_ Status**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**Notificationhandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Weitere Ressourcen


-   Eine Liste der NAP-Ressourcen finden Sie unter [Netzwerk Zugriffsschutz](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Informationen zum Statement of Health finden Sie unter [Network Access Protection (NAP)-SoH (Statement of Health)-Nachrichten](https://go.microsoft.com/fwlink/p/?linkid=83918).
-   Informationen zur Unternehmensnetzwerk-Gruppen Webseite und zum Blog finden Sie unter [Netzwerk Zugriffsschutz (Network Access Protection, NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Informationen zur NAP-API finden Sie unter [Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Benutzeroberfläche der EAP-Methode](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Aktivieren von Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant-und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 