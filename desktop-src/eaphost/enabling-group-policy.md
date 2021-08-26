---
title: Aktivieren von Gruppenrichtlinie
description: Erfahren Sie, wie Sie die Unterstützung durch Aktivieren der Gruppenrichtlinie konfigurieren. Weitere Informationen finden Sie unter Überlegungen zu Supplikationen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a36d2d464ef4f29c1f021f5ee7d1fad4d820e5
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812726"
---
# <a name="enabling-group-policy"></a>Aktivieren von Gruppenrichtlinie

In diesem Thema wird erläutert, wie sie durch Aktivieren der Gruppenrichtlinie konfiguriert wird. EAPHost-Supplikationen können an Gruppenrichtlinien teilnehmen, damit ein Netzwerkadministrator seine Netzwerkcomputer zentral konfigurieren kann.

Die genaue Methode und der Mechanismus, mit der die Supplizierung sich für die Teilnahme an gruppenrichtlinien entscheidet, liegt im Ermessen der Unterstützung. Beispiele für Mechanismen für die Teilnahme an Gruppenrichtlinien sind client-/serverseitige Erweiterungen, administrative Vorlagen usw.

## <a name="considerations-when-enabling-group-policy"></a>Überlegungen zum Aktivieren von Gruppenrichtlinie

Dies sind die Überlegungen zu Unterstützungen in Bezug auf Gruppenrichtlinien und EAP.

1.  Die EAP-Konfiguration sollte immer als XML gespeichert werden, wann immer dies möglich ist, und nicht im Binärformat. Gruppenrichtlinien können auf jeden Computer in der Domäne angewendet werden, und es ist nicht garantiert, dass die Konfiguration und die Benutzerdaten der EAP-Methode zwischen 32-Bit- und 64-Bit-Prozessorarchitekturen portiert sind. XML löst die Begrenzungsprobleme der Prozessorarchitektur, da die Supplizierung das prozessorarchitekturunabhängige XML zur Authentifizierungszeit lokal in die binäre Darstellung der Konfiguration konvertiert.

    Weitere Informationen finden Sie in den folgenden Themen.

    -   [Allgemeine häufig gestellte Fragen](general-frequently-asked-questions.yml)
    -   [Häufig gestellte Fragen zur EAP-Methode](eap-method-frequently-asked-questions.yml).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Wenn eine serverseitige Erweiterung für gruppenrichtlinien verwendet wird, ruft die Erweiterung in der Regel [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) auf, um verfügbare Methoden zu ermitteln und die entsprechende EAP-Konfiguration für diese Richtlinie zu generieren. Die Richtlinie wird dann an die entsprechenden Netzwerkclients gepusht, auf denen die Richtlinie angewendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der EAP-Methode Benutzeroberfläche](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen suppliplipli und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplikationen](eaphost-supplicants.md)
</dt> </dl>

 

 




