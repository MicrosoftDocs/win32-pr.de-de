---
title: Richtlinie für Softwareeinschränkung
description: Die Einstellungen der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) wurden mit der Veröffentlichung von Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichen Code zu schützen.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23176b23be5fcf4dc45f040f53e5d8f9dfbcdf05a8aee87feabd125d05c5372d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129802"
---
# <a name="software-restriction-policy"></a>Richtlinie für Softwareeinschränkung

Die Einstellungen der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) wurden mit der Veröffentlichung von Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichen Code zu schützen. Das SRP bietet einen Mechanismus, bei dem nur vertrauenswürdiger Code uneingeschränkten Zugriff auf die Berechtigungen eines Benutzers erhält. Unbekannter Code, der Viren oder Code enthalten kann, der mit derzeit installierten Programmen in Konflikt steht, darf nur in einer eingeschränkten Umgebung (häufig als Sandbox *bezeichnet)* ausgeführt werden, in der der Zugriff auf sicherheitssensible Benutzerberechtigungen nicht zulässig ist. Die ordnungsgemäße Verwendung des SRP kann Ihr Unternehmen flexibler machen, da es ein proaktives Framework zur Vermeidung von Problemen bietet, anstatt ein reaktives Framework, das auf der kostspieligen Alternative zum Wiederherstellen eines Systems nach einem Problem basiert.

Das SRP hängt von der Zuweisung von Vertrauensebenen zum Code ab, der auf einem System ausgeführt werden kann. Derzeit gibt es zwei Vertrauensebenen: Unrestricted und Disallowed. Code mit einer uneingeschränkten Vertrauensebene erhält uneingeschränkten Zugriff auf die Berechtigungen des Benutzers, sodass diese Vertrauensebene nur auf vollständig vertrauenswürdigen Code angewendet werden sollte. Code mit einer nicht gewährten Vertrauensebene ist für den Zugriff auf sicherheitssensible Benutzerberechtigungen nicht möglich und kann nur in einer Sandbox ausgeführt werden, sodass uneingeschränkter Code den nicht gewährten Code nicht in seinen Adressraum laden kann.

Die SRP-Konfiguration einzelner COM-Anwendungen erfolgt über den [SRPTrustLevel-Wert](srptrustlevel.md) im [AppID-Schlüssel](appid-key.md) der Anwendung in der Registrierung. Wenn die SRP-Vertrauensebene für eine COM-Anwendung nicht angegeben ist, wird der Standardwert Nicht verfügbar verwendet. Eine COM-Anwendung, die über eine uneingeschränkte Vertrauensebene verfügt, hat uneingeschränkten Zugriff auf die Berechtigungen des Benutzers, kann aber nur Komponenten mit einer uneingeschränkten Vertrauensebene laden, während eine Nicht gewährte COM-Anwendung Komponenten mit jeder Vertrauensebene laden kann, aber nicht auf sicherheitsempfindliche Benutzerberechtigungen zugreifen kann.

Zusätzlich zu den SRP-Vertrauensebenen einzelner COM-Anwendungen bestimmen zwei weitere SRP-Eigenschaften, wie das SRP für alle COM-Anwendungen verwendet wird. Wenn [SRPRunningObjectChecks](srprunningobjectchecks.md) aktiviert ist, werden Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, auf geeignete SRP-Vertrauensebenen überprüft. Das ausgeführte Objekt darf keine weniger strenge SRP-Vertrauensebene als das Clientobjekt haben. Beispielsweise kann das ausgeführte Objekt keine Nicht gewährte Vertrauensebene haben, wenn das Clientobjekt über eine uneingeschränkte Vertrauensebene verfügt.

Die zweite Eigenschaft bestimmt, wie das SRP Activate-as-Activator-Verbindungen verarbeitet. Wenn [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) aktiviert ist, wird die für das Serverobjekt konfigurierte SRP-Vertrauensebene mit der SRP-Vertrauensebene des Clientobjekts verglichen, und die strengere Vertrauensebene wird zum Ausführen des Serverobjekts verwendet. Wenn **SRPActivateAsActivatorChecks** nicht aktiviert ist, wird das Serverobjekt mit der SRP-Vertrauensebene des Clientobjekts ausgeführt, unabhängig von der SRP-Vertrauensebene, mit der es konfiguriert wurde. Standardmäßig sind **sowohl SRPRunningObjectChecks** als auch **SRPActivateAsActivatorChecks** aktiviert.

 

 




