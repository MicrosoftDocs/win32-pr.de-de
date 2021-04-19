---
description: Die IPv6 \_ - \_ schutzebenensocketoption ermöglicht Entwicklern das Platzieren von Zugriffs Einschränkungen für IPv6-Sockets.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353065"
---
# <a name="ipv6_protection_level"></a>IPv6- \_ Schutz \_ Ebene

Die IPv6 \_ - \_ schutzebenensocketoption ermöglicht Entwicklern das Platzieren von Zugriffs Einschränkungen für IPv6-Sockets. Mit solchen Einschränkungen kann sich eine im privaten LAN ausgeführte Anwendung selbst einfach und stabil vor externen Angriffen schützen. Die IPv6 \_ - \_ schutzsebene Socketoption erweitert oder schränkt den Bereich eines Abhör Sockets ein, ermöglicht bei Bedarf den uneingeschränkten Zugriff von öffentlichen und privaten Benutzern oder schränkt den Zugriff nur auf denselben Standort ein, je nach Bedarf.

Die IPv6- \_ Schutz \_ Ebene verfügt zurzeit über drei definierte Schutz Ebenen.



| Schutzebene                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>\_uneingeschränkte Schutz Ebene \_<br/>       | Wird von Anwendungen verwendet, die für den Internet übergreifenden Betrieb entwickelt wurden, einschließlich Anwendungen, die die in Windows integrierten IPv6-NAT-Traversale-Funktionen nutzen (z. b. Teredo). Diese Anwendungen können IPv4-Firewalls umgehen und müssen daher vor Internetangriffen auf den geöffneten Anschluss geschützt werden.<br/> |
| <span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>\_ \_ edgerestrierte Schutz Ebene<br/> | Wird von Anwendungen verwendet, die für den Betrieb über das Internet konzipiert sind. Diese Einstellung lässt die NAT-Überquerung nicht zu, da die Teredo-Implementierung von Windows verwendet wird. Diese Anwendungen können IPv4-Firewalls umgehen und müssen daher vor Internetangriffen auf den geöffneten Anschluss geschützt werden.<br/>                                   |
| <span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>Schutz \_ Ebene \_ eingeschränkt<br/>             | Wird von Intranetanwendungen verwendet, die keine Internet Szenarios implementieren. Diese Anwendungen werden im Allgemeinen nicht getestet oder vor Internetangriffen geschützt.<br/> Diese Einstellung beschränkt den empfangenen Datenverkehr auf linklokalen Datenverkehr.<br/>                                                                             |



 

Im folgenden Codebeispiel werden die definierten Werte für die einzelnen Werte bereitstellt:

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

Diese Werte schließen sich gegenseitig aus und können nicht in einem einzelnen [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktions aufzurufen kombiniert werden. Andere Werte für diese Socketoption sind reserviert. Diese Schutz Ebenen gelten nur für eingehende Verbindungen. Das Festlegen dieser Socketoption hat keine Auswirkung auf ausgehende Pakete oder Verbindungen.

Unter Windows 7 und Windows Server 2008 R2 ist der Standardwert für die \_ IPv6 \_ -Schutz Ebene nicht angegeben, und der Standardwert der **Schutz \_ Ebene \_** wird auf-1 festgelegt. Dies ist ein ungültiger Wert für die IPv6- \_ Schutz \_ Ebene.

Unter Windows Vista und Windows Server 2008 ist der Standardwert für die \_ IPv6 \_ -Schutz Ebene die **Schutz \_ Ebene \_ uneingeschränkt** und der Standardwert der **Schutz \_ Ebene \_** wird auf-1 festgelegt, ein unzulässiger Wert für die IPv6- \_ Schutz \_ Ebene.

Unter Windows Server 2003 und Windows XP ist der Standardwert für die \_ IPv6 \_ -Schutz Ebene die **Schutz \_ Ebene \_ edgerestrihiert** , und der **Schutz \_ Grad \_ default** ist als **Schutz \_ Ebene \_ edgerestrihiert** definiert.

> [!Note]  
> Die IPv6 \_ - \_ schutzsebene-Socketoption sollte festgelegt werden, bevor der Socket gebunden ist. Andernfalls entsprechen Pakete, die zwischen [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Aufrufen empfangen werden, der **Schutz \_ Ebene \_ edgerestrihiert** und können an die Anwendung übermittelt werden.

 

In der folgenden Tabelle werden die Auswirkungen der Anwendung der einzelnen Schutz Ebenen auf einen Abhör Socket beschrieben.

Schutzebene

Eingehender Datenverkehr zulässig

Gleiche Website

Extern

NAT-Durchlauf (Teredo)

Schutz \_ Ebene \_ eingeschränkt

Ja

Nein

Nein

\_ \_ edgerestrierte Schutz Ebene

Ja

Ja

Nein

\_uneingeschränkte Schutz Ebene \_

Ja

Ja

Ja



 

In der obigen Tabelle ist die **gleiche Website** Spalte eine Kombination aus folgendem:

-   Lokale Adressen verknüpfen
-   Lokale Standort Adressen
-   Globale Adressen, die bekanntermaßen zu demselben Standort gehören (übereinstimmende Präfix Tabelle)

Unter Windows 7 und Windows Server 2008 R2 ist der Standardwert für die IPv6- \_ Schutz \_ Ebene nicht angegeben. Wenn auf dem lokalen Computer keine auf der Edgeausnahme kompatible Firewallsoftware installiert ist (die Windows-Firewall ist deaktiviert oder eine andere Firewall installiert ist, die Teredo-Datenverkehr ignoriert), empfangen Sie Teredo-Datenverkehr nur, wenn Sie die IPv6- \_ \_ schutzebenensocketoption auf die **Schutz \_ Ebene " \_ uneingeschränkt**" festlegen. Die Windows-Firewall oder eine beliebige Edge-Traversal-fähige Firewall-Richtlinie kann diese Option jedoch aufgrund der Richtlinien Einstellungen für die Firewall ignorieren. Wenn Sie diese Socketoption auf die **Schutz \_ Ebene \_ uneingeschränkt** festlegen, kommuniziert die Anwendung mit ihrer expliziten Absicht, von der auf dem lokalen Computer installierten Host Firewall den von Edge durchsuchten Datenverkehr zu empfangen. Wenn also eine Host Firewall installiert ist, die auf Edgeausnahme basiert, wird die endgültige Entscheidung getroffen, ein Paket zu akzeptieren. Standardmäßig ohne festgelegte Socketoption:

-   o Wenn die Windows-Firewall aktiviert ist (oder eine andere Edgeausnahme unterstützende Host Firewall installiert ist), wird auf dem lokalen Computer das beliebige, was Sie erzwingt, beobachtet. Die typische Edge-Traversal-fähige Host Firewall blockiert standardmäßig Teredo-Datenverkehr. Daher beobachten Anwendungen den Standard, als ob es sich um eine **\_ \_ edgerestrierte Schutz Ebene** handelt.
-   o Wenn die Windows-Firewall nicht aktiviert ist und keine andere auf dem lokalen System unterstützende Host Firewall installiert ist, wird standardmäßig die **Schutz \_ Ebene \_ edgerestrihiert**.

Unter Windows Vista und Windows Server 2008 ist der Standardwert für die IPv6- \_ Schutz \_ Ebene die **Schutz \_ Ebene \_ uneingeschränkt**. Der effektive Wert hängt jedoch davon ab, ob die Windows-Firewall aktiviert ist. Die Windows-Firewall ist Edge-Traversal-fähig (Teredo-fähig), unabhängig davon, welcher Wert für die IPv6-Schutz Ebene festgelegt ist, \_ \_ und ignoriert, ob die IPv6- \_ Schutz \_ Ebene **\_ \_ uneingeschränkt geschützt** ist. Der effektive Wert hängt also von der Firewallrichtlinie ab. Wenn die Windows-Firewall deaktiviert ist und keine andere auf dem lokalen Computer unterstützende Firewall installiert ist, lautet der Standardwert für die IPv6- \_ Schutz \_ Ebene **\_ \_ uneingeschränkt**.

Unter Windows Server 2003 und Windows XP lautet der Standardwert für die IPv6- \_ Schutz \_ Ebene die **Schutz \_ Ebene \_ edgerestrihiert**. Sie erhalten keinen Teredo-Datenverkehr, es sei denn, Sie haben die IPv6- \_ \_ Option "socketschutzstufe" auf "nicht **\_ \_** eingeschränkt" festgelegt.

Abhängig von der IPv6- \_ Schutz \_ Ebene kann eine Anwendung, die nicht angeforderten Datenverkehr aus dem Internet benötigt, möglicherweise nicht angeforderten Datenverkehr empfangen. Diese Anforderungen sind jedoch nicht erforderlich, um angeforderten Datenverkehr über die Teredo-Schnittstelle von Windows zu empfangen. Weitere Informationen zur Interaktion mit Teredo finden Sie unter [empfangen von angeforderten Datenverkehr über Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).

Wenn eingehende Pakete oder Verbindungen aufgrund der festgelegten Schutz Ebene abgelehnt werden, wird die Ablehnung so behandelt, als ob keine Anwendung an diesem Socket lauscht.

> [!Note]
>
> Die IPv6 \_ - \_ schutzsetobjekt-Option fügt nicht notwendigerweise Zugriffs Einschränkungen für IPv6-Sockets ein oder schränkt die NAT-Überquerung mit einer anderen Methode als Windows Teredo oder sogar mit einer anderen Implementierung von Teredo durch einen anderen Anbieter ein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[Empfangen von angeforderten Datenverkehr über Teredo](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
