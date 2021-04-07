---
description: Der Server sendet dem Client einen Verweis auf seinen gemeinsam genutzten Sicherheitskontext, indem er die nicht transparente Anweisung der Digest-Challenge verwendet.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Authentifizieren von nachfolgenden Anforderungen mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eecccc3be68fb541994e63cdfc5035187e04aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758400"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Authentifizieren von nachfolgenden Anforderungen mit Microsoft Digest

Der Server sendet dem Client einen Verweis auf seinen gemeinsam genutzten [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) , indem er die nicht transparente Anweisung der Digest-Challenge verwendet. Nach erfolgreicher Authentifizierung muss der Client diesen Wert in nachfolgenden Anforderungen an den Zielserver angeben. Das Einschließen des nicht transparenten Werts in Anforderungen für Ressourcen, die mithilfe des vorhandenen Sicherheits Kontexts zugänglich sind, entfällt, dass die erneute Authentifizierung auf dem Domänen Controller erforderlich ist. Diese Anforderungen werden auf dem Server erneut authentifiziert, wobei der Digest- [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) verwendet wird, der nach der anfänglichen Authentifizierung zwischengespeichert wird.

Das folgende Diagramm veranschaulicht die Schritte, die von Client und Server bei einer nachfolgenden Anforderung von Zugriffs geschützten Ressourcen durchgeführt werden.

![Authentifizieren von nachfolgenden Anforderungen mithilfe von Microsoft Digest](images/digest2.png)

Um nach einer erfolgreichen Authentifizierung zusätzliche Ressourcen anzufordern, ruft der Client die Microsoft Digest [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion auf, um eine digestaufforderungs-Antwort zu generieren. Der nicht transparente Wert ist in der opopanweisung der Challenge-Antwort enthalten, die als Autorisierungs Header an den Server gesendet wird (als HTTP-Anforderung angezeigt).

Der Server Ruft die Funktion " [**Accept-SecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " auf, um zu bestimmen, ob ein [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) für den Client vorhanden ist. Wenn ein vorhandener Kontext gefunden wird, gibt die Funktion sec \_ E Complete zurück, \_ \_ um anzugeben, dass der Server dann die [**completeauthtoken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) -Funktion aufruft. Diese Funktion führt die Client Authentifizierung mit dem Digest- [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) aus, der während der [anfänglichen Authentifizierung](initial-authentication-using-microsoft-digest.md) zwischengespeichert wird, anstatt erneut auf dem Domänen Controller zu authentifizieren.

 

 
