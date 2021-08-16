---
title: Aktivieren Gruppenrichtlinie
description: Erfahren Sie, wie Sie das Bittsteller konfigurieren, indem Sie die Gruppenrichtlinie aktivieren. Weitere verfügbare Ressourcen finden Sie unter Überlegungen zu Unterstützungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2a388bf8dba155e42d5542c1379f7b0cc34d44579b92809387541d7e20cf65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784999"
---
# <a name="enabling-group-policy"></a>Aktivieren Gruppenrichtlinie

In diesem Thema wird erläutert, wie das -Supplicant durch Aktivieren der Gruppenrichtlinie konfiguriert wird. EAPHost-Administratoren können an gruppenrichtlinien teilnehmen, damit netzwerkadministratoren ihre Netzwerkcomputer zentral konfigurieren können.

Die genaue Methode und der Mechanismus, mit denen sich der Bittsteller für die Teilnahme an der Gruppenrichtlinie entscheidet, liegt im Ermessen des Bittstellers. Beispiele für Mechanismen für die Gruppenrichtlinienteilnahme sind client-/serverseitige Erweiterungen, administrative Vorlagen usw.

## <a name="considerations-when-enabling-group-policy"></a>Überlegungen beim Aktivieren Gruppenrichtlinie

Dies sind die Überlegungen zu Denk- und Annahmen in Bezug auf Gruppenrichtlinien und EAP.

1.  Die EAP-Konfiguration sollte nach Möglichkeit immer als XML und nicht im Binärformat gespeichert werden. Gruppenrichtlinien können auf jeden Computer in der Domäne angewendet werden, und die Konfiguration der EAP-Methode und die Benutzerdaten sind nicht garantiert portierbar zwischen 32-Bit- und 64-Bit-Prozessorarchitekturen. XML löst die Probleme mit der Prozessorarchitekturgrenze, da die bittliche -Struktur die prozessorarchitekturunabhängige XML-Datei zur Authentifizierungszeit lokal in die binäre Darstellung der Konfiguration konvertiert.

    Weitere Informationen finden Sie in den folgenden Themen.

    -   [Allgemeine häufig gestellte Fragen](general-frequently-asked-questions.md)
    -   [Häufig gestellte Fragen zur EAP-Methode](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Wenn eine serverseitige Gruppenrichtlinienerweiterung verwendet wird, wird die Erweiterung in der Regel [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) aufrufen, um verfügbare Methoden zu bestimmen und eine entsprechende EAP-Konfiguration für diese Richtlinie zu generieren. Die Richtlinie wird dann an die entsprechenden Netzwerkclients pushen, auf denen die Richtlinie angewendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der EAP-Benutzeroberfläche](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren von NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant- und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




