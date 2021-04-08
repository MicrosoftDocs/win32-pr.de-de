---
description: Es gibt zwei Faktoren bei der Ermittlung des Verhaltens des Identitäts Wechsels der Zertifizierungsstelle, die der Client dem Server explizit über eine Identitätswechsel Ebene zuweist, und die Fähigkeit der Server, seine eigene Identität zu maskieren, wenn Aufrufe im Auftrag des Clients durchgeführt werden.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Cloaking (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748081"
---
# <a name="cloaking-component-services"></a>Cloaking (Komponenten Dienste)

Beim Festlegen des Verhaltens des Identitäts Wechsels gibt es zwei Komponenten: die Autorität, die der Client dem Server explizit über eine Identitätswechsel Ebene zuweist, und die Fähigkeit des Servers, seine eigene Identität zu maskieren, wenn Aufrufe im Auftrag des Clients durchgeführt werden. Diese letztere Funktion wird als " *Cloaking*" bezeichnet. Das Cloaking muss mit der Sicherheitsidentität durchzuführen sein, unter der der Server Aufrufe ausführt.

Wenn der Server die Identität des Clients annimmt, hat er direkten Zugriff auf die Sicherheits Anmelde Informationen des Clients. In einem sehr lokalen Sinne übernimmt der Server Thread die Identität des Clients. Wenn der Server jedoch Aufrufe außerhalb des Prozesses durchführt, wird die Client Identität nicht notwendigerweise als Identität, unter der der Aufruf erfolgt, projiziert.

Wenn das Cloaking aktiviert ist, können Aufrufe von dem Server, der die Identität des Clients annimmt, unter der Identität des Clients vorgenommen werden. Wenn das Cloaking deaktiviert ist, werden Aufrufe durch den Server unter der Identität des Servers vorgenommen.

Darüber hinaus gibt es zwei Arten von Verstopfungen, *statischem* und *dynamischem* Cloaking, die wie folgt beschrieben werden können:

-   Identitätswechsel mit statischem Cloaking. Die ursprüngliche Client Identität (die als Server Thread Token implementiert wurde) kann bei einem Aufruf mithilfe von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)einmal an einen Downstreamserver präsentiert werden, wobei die ursprüngliche Client Identität einmal auf dem Proxy festgelegt wird, und dass das Thread Token bei nachfolgenden Methoden aufrufen verwendet wird.
-   Identitätswechsel mit dynamischem Cloaking. Die ursprüngliche Client Identität wird bei jedem Methodenaufrufe des Downstreamservers als Server Thread Token erkannt. Tatsächlich kann die Identität, die angezeigt wird, dynamisch bestimmt werden. Der Aufwand, der dazu erforderlich ist, kann deutlich teurer werden.

Für COM+-Anwendungen ist die Standardkonfiguration für die Funktion für dynamisches durchsuchen. Dies kann Programm gesteuert und administrativ geändert werden. Während das dynamische Cloaking einen Leistungs Aufwand verursachen kann, bietet es die Flexibilität, die normalerweise für Umstände erforderlich ist, die die Verwendung von Identitätswechsel an erster Stelle erfordern.

Weitere Details zu den Zusammenhang und genauen Beschreibungen möglicher Verhalten finden Sie unter " [Cloaking](/windows/desktop/com/cloaking) " in der com-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Client seitige Anforderungen für Identitätswechsel](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Server seitige Anforderungen für Identitätswechsel](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
