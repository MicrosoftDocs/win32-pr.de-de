---
description: Die ordnungsgemäße Verwendung der Richtlinie zur Softwareeinschränkung kann Ihr Unternehmen flexibler machen, da sie ein proaktives Framework zur Vermeidung von Problemen bietet, anstatt eines reaktiven Frameworks, das auf der kostspieligen Alternative zum Wiederherstellen eines Systems nach einem Problem basiert. Die Softwareeinschränkungsrichtlinie wurde mit der Veröffentlichung von Microsoft Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichen Code zu schützen. Die Einschränkungsrichtlinie bietet einen Mechanismus, bei dem nur vertrauenswürdiger Code uneingeschränkten Zugriff auf Benutzerberechtigungen erhält. Unbekannter Code, der Viren oder Code enthalten kann, der mit derzeit installierten Programmen in Konflikt steht, darf nur in einer eingeschränkten Umgebung (häufig als Sandbox bezeichnet) ausgeführt werden, in der der Zugriff auf sicherheitsempfindliche Benutzerberechtigungen nicht zulässig ist.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Verwenden der Softwareeinschränkungsrichtlinie in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e823d794cccf590ddf9ffd8fcb6f7982eb1543368e400ab3632601ec3a2b96e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304936"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Verwenden der Softwareeinschränkungsrichtlinie in COM+

Die ordnungsgemäße Verwendung der Richtlinie zur Softwareeinschränkung kann Ihr Unternehmen flexibler machen, da sie ein proaktives Framework zur Vermeidung von Problemen bietet, anstatt eines reaktiven Frameworks, das auf der kostspieligen Alternative zum Wiederherstellen eines Systems nach einem Problem basiert. Die Softwareeinschränkungsrichtlinie wurde mit der Veröffentlichung von Microsoft Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichen Code zu schützen. Die Einschränkungsrichtlinie bietet einen Mechanismus, bei dem nur vertrauenswürdiger Code uneingeschränkten Zugriff auf die Berechtigungen eines Benutzers erhält. Unbekannter Code, der Viren oder Code enthalten kann, der mit derzeit installierten Programmen in Konflikt steht, darf nur in einer eingeschränkten Umgebung (häufig als Sandbox *bezeichnet)* ausgeführt werden, in der der Zugriff auf sicherheitssensible Benutzerberechtigungen nicht zulässig ist.

Die Softwareeinschränkungsrichtlinie hängt davon ab, ob dem Code Vertrauensebenen zugewiesen werden, die auf einem System ausgeführt werden können. Derzeit gibt es zwei Vertrauensebenen: Unrestricted und Disallowed. Code mit einer uneingeschränkten Vertrauensebene erhält uneingeschränkten Zugriff auf die Berechtigungen des Benutzers, sodass diese Vertrauensebene nur auf vollständig vertrauenswürdigen Code angewendet werden sollte. Code mit einer nicht gewährten Vertrauensebene ist daran gehindert, auf sicherheitsempfindliche Benutzerberechtigungen zu zugreifen, und kann nur in einer Sandbox ausgeführt werden, die verhindert, dass uneingeschränkter Code den nicht gewährten Code in seinen Adressraum lädt.

Das Konfigurieren der Softwareeinschränkungsrichtlinie für ein System erfolgt über das Verwaltungstool Lokale Sicherheitsrichtlinie, während die Konfiguration der Einschränkungsrichtlinie einzelner COM+-Anwendungen entweder programmgesteuert oder über das Verwaltungstool komponentendienste erfolgt. Wenn die Vertrauensebene der Einschränkungsrichtlinie für eine COM+-Anwendung nicht angegeben ist, werden die systemweiten Einstellungen verwendet, um die Vertrauensebene der Anwendung zu bestimmen. Die COM+-Einschränkungsrichtlinie muss sorgfältig mit den systemweiten Einstellungen koordiniert werden, da eine COM+-Anwendung mit einer uneingeschränkten Vertrauensebene nur Komponenten mit einer uneingeschränkten Vertrauensebene laden kann. Eine nicht dürfene COM+-Anwendung kann Komponenten mit einer beliebigen Vertrauensebene laden, aber nicht auf alle Berechtigungen des Benutzers zugreifen.

Zusätzlich zu den Vertrauensebenen der Softwareeinschränkungsrichtlinie einzelner COM+-Anwendungen bestimmen zwei weitere Eigenschaften, wie die Einschränkungsrichtlinie für alle COM+-Anwendungen verwendet wird. Wenn [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) aktiviert ist, werden Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, auf geeignete Vertrauensebenen überprüft. Das ausgeführte Objekt darf keine weniger strenge Vertrauensebene als das Clientobjekt haben. Beispielsweise kann das ausgeführte Objekt keine Nicht gewährte Vertrauensebene haben, wenn das Clientobjekt über eine uneingeschränkte Vertrauensebene verfügt.

Die zweite Eigenschaft bestimmt, wie die Softwareeinschränkungsrichtlinie Activate-as-Activator-Verbindungen behandelt. Wenn [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) aktiviert ist, wird die für das Serverobjekt konfigurierte Vertrauensebene mit der Vertrauensebene des Clientobjekts verglichen, und die strengere Vertrauensebene wird zum Ausführen des Serverobjekts verwendet. Wenn SRPActivateAsActivatorChecks nicht aktiviert ist, wird das Serverobjekt mit der Vertrauensebene des Clientobjekts ausgeführt, unabhängig von der Vertrauensebene, mit der es konfiguriert wurde. Standardmäßig sind sowohl SRPRunningObjectChecks als auch SRPActivateAsActivatorChecks aktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client-Identitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Konfigurieren der Richtlinie für Softwareeinschränkung](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Sicherheit von Bibliotheksanwendung](library-application-security.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> </dl>

 

 
