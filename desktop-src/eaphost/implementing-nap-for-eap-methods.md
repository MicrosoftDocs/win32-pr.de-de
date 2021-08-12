---
title: Implementieren von NAP-Unterstützung für EAP-Methoden
description: Erfahren Sie, wie Sie NAP-Unterstützung für ein EAPHost-Supplicant implementieren. Weitere verfügbare Ressourcen finden Sie unter EAPHost-bezogene NAP-Themen.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff84c24aeb475b83146f2c56e9e139fd930eac27656349c594f05d91c1036fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273314"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementieren von NAP-Unterstützung für EAP-Methoden

In diesem Thema wird erläutert, wie NAP für ein EAPHost-Supplicant implementiert wird. In Windows Vista und Windows Server 2008 ist ein NAP-Erzwingungsclient (NAP EC) für [authentifizierte 802.1X-Verbindungen](/previous-versions/windows/embedded/ms890287(v=msdn.10)) verfügbar.

## <a name="implementing-network-access-protection-nap"></a>Implementieren des Netzwerkzugriffsschutzes (Network Access Protection, NAP)

Zur Unterstützung von NAP implementiert ein EAPHost-Supplicant [](/previous-versions/windows/desktop/api) eine Rückruffunktion, die dem NotificationHandler-Rückrufprototyp entspricht, und muss beim Aufrufen von [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)einen Zeiger auf diese Rückruffunktion bereitstellen.

Die Rückruffunktion verwendet zwei Parameter.

-   Eine GUID, die die der Authentifizierung zugeordnete Schnittstelle eindeutig identifiziert.
-   Ein VOID-Zeiger auf eine nicht transparente Datenstruktur, die vom Supplicant bereitgestellt wird.

EAPHost wird die von supplicant bereitgestellte Rückruffunktion mit der eindeutigen Schnittstellen-GUID und dem VOID-Zeiger aufrufen, wenn sich der Quarantänezustand des Computers ändert. Wenn EAPHost die vom Supplicant bereitgestellte Rückruffunktion aufruft, antwortet der Supplicant, indem die logische Netzwerkverbindung, die durch den GUID/VOID-Zeiger der Schnittstelle identifiziert wird, geschlossen wird und die Authentifizierung mithilfe von **EapHostPeerBeginSession** erneut beginnt.

EAPHost kann die von der Supplicant bereitgestellte Rückruffunktion jederzeit aufrufen: vor, während einer aktiven Authentifizierung oder nach Abschluss der Authentifizierung (nachdem [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) aufgerufen wurde, jedoch nicht vor dem Aufruf von [**EapHostPeerClearConnection).**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) Der Supplicant sollte immer reagieren, indem er die logische Netzwerkverbindung abfängt und sich erneut authentifiziert.

Wenn der Supplicant heruntergefahren wird oder keine Benachrichtigungen mehr über Isolationszustandsänderungen erhält, sollte der Supplicant [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) aufrufen und die entsprechende Schnittstellen-GUID angeben. Wenn der Supplicant die Isolation der logischen Netzwerkverbindung bestimmen möchte, kann der Supplicant diese Informationen aus **EapHostPeerMethodResult.isolationState** abrufen, wenn [**das EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) von [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)erhalten wird.

## <a name="eaphost-related-nap-information"></a>EAPHost-bezogene NAP-Informationen

Informationen zur EAPHost-API finden Sie in den folgenden Themen.

-   [**\_EAP-ATTRIBUTTYP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**\_EAP-FEHLER**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Häufig gestellte Fragen zu EAPHost Supplicant](eaphost-supplicant-frequently-asked-questions.md)
-   [**EAP-Methodeneigenschaften**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Fehler- und Informationskonst constants im Zusammenhang mit EAP**](eap-related-error-and-information-constants.md)
-   [**\_ISOLATIONSSTATUS**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Weitere Ressourcen


-   Eine Liste der NAP-Ressourcen finden Sie unter [Netzwerkzugriffsschutz](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Informationen zur Integritätserlädung finden Sie unter [SoH-Meldungen (Network Access Protection, NAP).](https://go.microsoft.com/fwlink/p/?linkid=83918)
-   Die Webseite Enterprise Netzwerkgruppe und den Blog finden Sie unter [Netzwerkzugriffsschutz (Network Access Protection, NAP).](https://go.microsoft.com/fwlink/p/?linkid=83845)
-   Informationen zur NAP-API finden Sie unter [Netzwerkzugriffsschutz.](/windows/desktop/NAP/network-access-protection-start-page)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der EAP-Benutzeroberfläche](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Aktivieren Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant- und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 