---
title: Aktivieren von Gruppenrichtlinie
description: Erfahren Sie, wie Sie den Supplicant durch Aktivieren der Gruppenrichtlinie konfigurieren. Weitere Informationen finden Sie unter Überlegungen zu Supplicants und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391035"
---
# <a name="enabling-group-policy"></a>Aktivieren von Gruppenrichtlinie

In diesem Thema wird erläutert, wie Sie den Supplicant durch Aktivieren der Gruppenrichtlinie konfigurieren. EAPHost-Supplicants können an der Gruppenrichtlinie teilnehmen, damit ein Netzwerkadministrator seine Netzwerk Computer zentral konfigurieren kann.

Die genaue Methode und der Mechanismus, mit dem sich der Supplicant für die Teilnahme an der Gruppenrichtlinie entscheidet, liegt im Ermessen des Supplicant. Beispiele für Mechanismen für die Gruppenrichtlinien Beteiligung sind Client-/serverseitige Erweiterungen, administrative Vorlagen usw.

## <a name="considerations-when-enabling-group-policy"></a>Überlegungen beim Aktivieren von Gruppenrichtlinie

Dies sind die Überlegungen für Supplicants in Bezug auf die Gruppenrichtlinie und EAP.

1.  Die EAP-Konfiguration sollte immer als XML-Datei, wann immer möglich, und nicht im Binärformat gespeichert werden. Die Gruppenrichtlinie kann auf jeden Computer in der Domäne angewendet werden, und die EAP-Methoden Konfiguration und die Benutzerdaten sind nicht garantiert zwischen 32-Bit-und 64-Bit-Prozessorarchitekturen portabel. XML löst die Probleme der Prozessorarchitektur Grenzen auf, da der Supplicant den von der Prozessorarchitektur unabhängigen XML-Code zum Zeitpunkt der Authentifizierung lokal in die binäre Darstellung der Konfiguration konvertiert.

    Weitere Informationen finden Sie in den nachfolgenden Themen.

    -   [Allgemeine häufig gestellte Fragen](general-frequently-asked-questions.md)
    -   [Häufig gestellte Fragen zur EAP-Methode](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Wenn eine serverseitige Erweiterung für Gruppenrichtlinien verwendet wird, ruft die Erweiterung [**eaphostpeergetmethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) in der Regel auf, um die verfügbaren Methoden zu ermitteln und eine entsprechende EAP-Konfiguration für diese Richtlinie zu generieren. Die Richtlinie wird dann an geeignete Netzwerk Clients übertragen, auf denen die Richtlinie angewendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Benutzeroberfläche der EAP-Methode](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant-und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




