---
description: Durch die ordnungsgemäße Verwendung der Software Einschränkungs Richtlinie kann Ihr Unternehmen flexibler werden, da es ein proaktives Framework zur Vermeidung von Problemen bietet, anstatt ein reaktives Framework zu verwenden, das auf der kostspieligen Alternative zur Wiederherstellung eines Systems basiert, nachdem ein Problem aufgetreten ist. Die Software Einschränkungs Richtlinie wurde mit der Veröffentlichung von Microsoft Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichem Code zu schützen. Die Einschränkungs Richtlinie bietet einen Mechanismus, bei dem nur vertrauenswürdiger Code uneingeschränkten Zugriff auf Benutzerberechtigungen erhält. Unbekannter Code, der möglicherweise Viren oder Code enthält, der mit den derzeit installierten Programmen in Konflikt steht, darf nur in einer eingeschränkten Umgebung (häufig als Sandbox bezeichnet) ausgeführt werden, in der es nicht zulässig ist, auf sicherheitsrelevante Benutzerberechtigungen zuzugreifen.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Verwenden der Richtlinie für Software Einschränkung in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3620aba8cce2859d76ba07c2fa9655dd9036bdbb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483406"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Verwenden der Richtlinie für Software Einschränkung in com+

Durch die ordnungsgemäße Verwendung der Software Einschränkungs Richtlinie kann Ihr Unternehmen flexibler werden, da es ein proaktives Framework zur Vermeidung von Problemen bietet, anstatt ein reaktives Framework zu verwenden, das auf der kostspieligen Alternative zur Wiederherstellung eines Systems basiert, nachdem ein Problem aufgetreten ist. Die Software Einschränkungs Richtlinie wurde mit der Veröffentlichung von Microsoft Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichem Code zu schützen. Die Einschränkungs Richtlinie stellt einen Mechanismus bereit, bei dem nur vertrauenswürdiger Code uneingeschränkten Zugriff auf die Berechtigungen eines Benutzers erhält. Unbekannter Code, der möglicherweise Viren oder Code enthält, der mit den derzeit installierten Programmen in Konflikt steht, darf nur in einer eingeschränkten Umgebung (häufig als *Sandbox* bezeichnet) ausgeführt werden, in der es nicht zulässig ist, auf sicherheitsrelevante Benutzerberechtigungen zuzugreifen.

Die Software Einschränkungs Richtlinie hängt davon ab, ob dem Code, der auf einem System ausgeführt werden kann, Vertrauens Ebenen zugewiesen werden. Zurzeit sind zwei Vertrauens Ebenen vorhanden: uneingeschränkt und unzulässig. Code mit einer uneingeschränkten Vertrauens Ebene erhält uneingeschränkten Zugriff auf die Berechtigungen des Benutzers. diese Vertrauens Ebene sollte daher nur auf voll vertrauenswürdigen Code angewendet werden. Der Zugriff auf sicherheitsrelevante Benutzerberechtigungen ist für Code mit einer unzulässigen Vertrauens Ebene nicht zulässig. er kann nur in einem Sandkasten ausgeführt werden, um zu verhindern, dass unzulässiger Code den unzulässigen Code in seinen Adressraum lädt.

Das Konfigurieren der Software Einschränkungs Richtlinie für ein System erfolgt über das Verwaltungs Tool "lokale Sicherheitsrichtlinie", während die Einschränkungs Richtlinien Konfiguration einzelner com+-Anwendungen entweder Programm gesteuert oder über das Verwaltungs Programmkomponenten Dienste ausgeführt wird. Wenn für eine COM+-Anwendung die Vertrauens Ebene der Einschränkungs Richtlinie nicht angegeben wird, werden die systemweiten Einstellungen verwendet, um die Vertrauens Ebene der Anwendung zu bestimmen. Die Einstellungen der com+-Einschränkungs Richtlinie müssen sorgfältig mit den systemweiten Einstellungen koordiniert werden, da eine COM+-Anwendung mit einer uneingeschränkten Vertrauens Ebene nur Komponenten mit einer uneingeschränkten Vertrauens Ebene laden kann. eine unzulässige com+-Anwendung kann Komponenten mit jeder Vertrauens Ebene laden, aber nicht auf alle Berechtigungen des Benutzers zugreifen.

Zusätzlich zu den Vertrauens Ebenen der Software Einschränkungs Richtlinie einzelner com+-Anwendungen bestimmen zwei andere Eigenschaften, wie die Einschränkungs Richtlinie für alle com+-Anwendungen verwendet wird. Wenn [srprunningobjectchecks](/windows/desktop/com/srprunningobjectchecks) aktiviert ist, werden Versuche, eine Verbindung mit laufenden Objekten herzustellen, auf die entsprechenden Vertrauens Ebenen überprüft. Das laufende Objekt kann nicht eine weniger strenge Vertrauens Ebene aufweisen als das Client Objekt. Beispielsweise kann das laufende Objekt nicht über eine unzulässige Vertrauens Ebene verfügen, wenn das Client Objekt eine uneingeschränkte Vertrauens Ebene aufweist.

Die zweite Eigenschaft bestimmt, wie die Software Einschränkungs Richtlinie aktivierte Aktivierungs Verbindungen behandelt. Wenn [srpactivateasactivatorchecks](/windows/desktop/com/srpactivateasactivatorchecks) aktiviert ist, wird die Vertrauens Ebene, die für das Server Objekt konfiguriert ist, mit der Vertrauens Ebene des Client Objekts verglichen, und die strengere Vertrauens Ebene wird zum Ausführen des Server Objekts verwendet. Wenn srpactivateasactivatorchecks nicht aktiviert ist, wird das Server Objekt unabhängig von der Vertrauens Ebene, mit der es konfiguriert wurde, mit der Vertrauens Ebene des Client Objekts ausgeführt. Standardmäßig sind sowohl srprunningobjectchecks als auch srpactivateasactivatorchecks aktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Konfigurieren der Software Einschränkungs Richtlinie](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> </dl>

 

 
