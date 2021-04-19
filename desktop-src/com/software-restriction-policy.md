---
title: Software Einschränkungs Richtlinie
description: Die SRP-Einstellungen (Software Einschränkungs Richtlinie) wurden mit der Veröffentlichung von Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichem Code zu schützen.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97bf42cd949127e9012580ec16379cf36a95353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341846"
---
# <a name="software-restriction-policy"></a>Software Einschränkungs Richtlinie

Die SRP-Einstellungen (Software Einschränkungs Richtlinie) wurden mit der Veröffentlichung von Windows XP eingeführt, um Systeme vor unbekanntem und möglicherweise gefährlichem Code zu schützen. Der SRP bietet einen Mechanismus, bei dem nur vertrauenswürdiger Code uneingeschränkten Zugriff auf die Berechtigungen eines Benutzers erhält. Unbekannter Code, der möglicherweise Viren oder Code enthält, der mit den derzeit installierten Programmen in Konflikt steht, darf nur in einer eingeschränkten Umgebung (häufig als *Sandbox* bezeichnet) ausgeführt werden, in der es nicht zulässig ist, auf sicherheitsrelevante Benutzerberechtigungen zuzugreifen. Durch die ordnungsgemäße Verwendung der SRP-Lösung kann Ihr Unternehmen flexibler werden, da es ein proaktives Framework zur Vermeidung von Problemen bietet, anstatt ein reaktives Framework zu verwenden, das sich auf die kostspielige Alternative zur Wiederherstellung eines Systems nach einem Problem stützt.

Der SRP-Code richtet sich nach dem Zuweisen von Vertrauens Ebenen zu dem Code, der auf einem System ausgeführt werden kann. Zurzeit sind zwei Vertrauens Ebenen vorhanden: uneingeschränkt und unzulässig. Code mit einer uneingeschränkten Vertrauens Ebene erhält uneingeschränkten Zugriff auf die Berechtigungen des Benutzers. diese Vertrauens Ebene sollte daher nur auf voll vertrauenswürdigen Code angewendet werden. Der Zugriff auf sicherheitsrelevante Benutzerberechtigungen ist für Code mit einer unzulässigen Vertrauens Ebene unzulässig und kann nur in einem Sandkasten ausgeführt werden, sodass der unzulässige Code nicht durch uneingeschränkten Code in seinen Adressraum geladen werden kann.

Die SRP-Konfiguration einzelner com-Anwendungen erfolgt über den [SRPTrustLevel](srptrustlevel.md) -Wert im [AppID](appid-key.md) -Schlüssel der Anwendung in der Registrierung. Wenn die SRP-Vertrauens Ebene für eine COM-Anwendung nicht angegeben wird, wird der Standardwert "nicht zulässig" verwendet. Eine COM-Anwendung mit einer uneingeschränkten Vertrauens Ebene hat uneingeschränkten Zugriff auf die Berechtigungen des Benutzers, kann jedoch nur Komponenten mit einer uneingeschränkten Vertrauens Ebene laden, während eine nicht zulässige com-Anwendung Komponenten mit jeder Vertrauens Ebene laden kann, aber nicht auf sicherheitsrelevante Benutzerberechtigungen zugreifen kann.

Zusätzlich zu den SRP-Vertrauens Ebenen einzelner com-Anwendungen bestimmen zwei weitere SRP-Eigenschaften, wie die SRP für alle com-Anwendungen verwendet wird. Wenn [srprunningobjectchecks](srprunningobjectchecks.md) aktiviert ist, werden Versuche, eine Verbindung mit laufenden Objekten herzustellen, auf die entsprechenden SRP-Vertrauens Ebenen überprüft. Das laufende Objekt kann nicht über eine weniger strenge SRP-Vertrauens Ebene verfügen als das Client Objekt. Beispielsweise kann das laufende Objekt nicht über eine unzulässige Vertrauens Ebene verfügen, wenn das Client Objekt eine uneingeschränkte Vertrauens Ebene aufweist.

Die zweite Eigenschaft bestimmt, wie das SRP Aktivierungs-as-activatorverbindungen behandelt. Wenn [srpactivateasactivatorchecks](srpactivateasactivatorchecks.md) aktiviert ist, wird die für das Server Objekt konfigurierte SRP-Vertrauens Ebene mit der SRP-Vertrauens Ebene des Client Objekts verglichen, und die strengere Vertrauens Ebene wird zum Ausführen des Server Objekts verwendet. Wenn **srpactivateasactivatorchecks** nicht aktiviert ist, wird das Server Objekt unabhängig von der SRP-Vertrauens Ebene, mit der es konfiguriert wurde, mit der SRP-Vertrauens Ebene des Client Objekts ausgeführt. Standardmäßig sind sowohl **srprunningobjectchecks** als auch **srpactivateasactivatorchecks** aktiviert.

 

 




