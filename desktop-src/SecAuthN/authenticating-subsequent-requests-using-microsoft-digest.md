---
description: Der Server sendet dem Client mithilfe der nicht transparenten Direktive der Digest-Herausforderung einen Verweis auf seinen freigegebenen Sicherheitskontext.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Authentifizieren nachfolgender Anforderungen mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25954612a99fa0a0a9710f5e8e0679948cc3bac5ceae669a06ec40bd5c22241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101424"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Authentifizieren nachfolgender Anforderungen mit Microsoft Digest

Der Server sendet dem Client [](/windows/desktop/SecGloss/s-gly) mithilfe der nicht transparenten Direktive der Digest-Herausforderung einen Verweis auf seinen freigegebenen Sicherheitskontext. Nach einer erfolgreichen Authentifizierung muss der Client diesen Wert in nachfolgenden Anforderungen an den Zielserver angeben. Durch das Hinzufügen des nicht transparenten Werts in Anforderungen für Ressourcen, auf die über den vorhandenen Sicherheitskontext zugegriffen werden kann, entfällt die Notwendigkeit einer erneuten Authentifizierung auf dem Domänencontroller. Solche Anforderungen werden auf dem Server erneut authentifiziert, indem der [*Digestsitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) verwendet wird, der nach der anfänglichen Authentifizierung zwischengespeichert wurde.

Das folgende Diagramm veranschaulicht die Schritte, die von Client und Server während einer nachfolgenden Anforderung für zugriffsgeschützte Ressourcen ausgeführt werden.

![Authentifizieren nachfolgender Anforderungen mithilfe des Microsoft-Digests](images/digest2.png)

Um nach einer erfolgreichen Authentifizierung zusätzliche Ressourcen anfordern, ruft der Client die Microsoft Digest [**MakeSignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-makesignature) auf, um eine Digest-Anforderungsantwort zu generieren. Der nicht transparente Wert ist in der nicht transparenten Direktive der Anforderantwort enthalten, die als Autorisierungsheader an den Server gesendet wird (als HTTP-Anforderung angezeigt).

Der Server ruft die [**Funktion AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) auf, um zu bestimmen, ob ein [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) für den Client vorhanden ist. Wenn ein vorhandener Kontext gefunden wird, gibt die Funktion SEC E COMPLETE NEEDED zurück, um anzugeben, dass der Server dann \_ \_ die \_ [**CompleteAuthToken-Funktion aufrufen**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) muss. Diese Funktion führt die Clientauthentifizierung mithilfe des [](/windows/desktop/SecGloss/s-gly) Digestsitzungsschlüssels aus, der während der anfänglichen Authentifizierung zwischengespeichert [wurde,](initial-authentication-using-microsoft-digest.md) anstatt sich auf dem Domänencontroller erneut zu authentifizieren.

 

 
